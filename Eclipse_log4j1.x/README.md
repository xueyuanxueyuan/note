# Eclipse配置Log4j
## 1. 从零开始
 
> a). 新建Java Project>>新建package>>新建java类；    
b). import jar包（一个就够），这里我用的是log4j-1.2.14.jar，   
c). 新建log4j.properties，置于project根目录下；    
log4j.rootLogger=info, ServerDailyRollingFile, stdout     
log4j.appender.ServerDailyRollingFile=org.apache.log4j.DailyRollingFileAppender    
log4j.appender.ServerDailyRollingFile.DatePattern='.'yyyy-MM-dd    
log4j.appender.ServerDailyRollingFile.File=C://logs/notify-subscription.log    
log4j.appender.ServerDailyRollingFile.layout=org.apache.log4j.PatternLayout    
log4j.appender.ServerDailyRollingFile.layout.ConversionPattern=%d - %m%n
log4j.appender.ServerDailyRollingFile.Append=true   
log4j.appender.stdout=org.apache.log4j.ConsoleAppender    
log4j.appender.stdout.layout=org.apache.log4j.PatternLayout    
log4j.appender.stdout.layout.ConversionPattern=%d{yyyy-MM-dd HH:mm:ss} %p [%c] %m%n   
d). 在main()中，加载log4j：   
PropertyConfigurator.configure("log4j.properties");     
e). 写个小程序测试下，好了，我们看下效果：    
  ![image](http://images.cnblogs.com/cnblogs_com/alipayhutu/201206/201206212136409811.png)    
1). 用绝对路径，真心不推荐啊，太不优雅了；    
2). 将log4j文件置于bin/目录下：    
        
        
    a). 代码中，PropertyConfigurator.configure("bin/log4j.properties");
        
    b). 代码中，PropertyConfigurator.configure(ClassLoader.getSystemResource("log4j.properties"));
       
       
    c). 注意，必须位于bin直接目录下，不可位于bin更深层的目录当中。可是这究竟是为神马捏？

> 可参考： http://blog.sina.com.cn/s/blog_3f4755c70100jco1.html    
> 3) 必杀技：    
private static void initLog4j() {     
Properties prop = new Properties();   
prop.setProperty("log4j.rootLogger", "DEBUG, CONSOLE");   
prop.setProperty("log4j.appender.CONSOLE","org.apache.log4j.ConsoleAppender");     
prop.setProperty("log4j.appender.CONSOLE.layout","org.apache.log4j.PatternLayout");     
prop.setProperty("log4j.appender.CONSOLE.layout.ConversionPattern","%d{HH:mm:ss,SSS} [%t] %-5p %C{1} : %m%n");      
PropertyConfigurator.configure(prop);      
}
## 2. Log4j 格式详解

**log4j.rootLogger=日志级别，appender1, appender2, ….**

    日志级别：ALL<DEBUG<INFO<WARN<ERROR<FATAL<OFF，不区分大小写
    注意，需在控制台输入，只需将其中一个appender定义为stdout即可
    注意，rootLogger默认是对整个工程生效
    注意，如果只想对某些包操作，那么：log4j.logger.com.hutu=info, stdout，表示该日志对package com.hutu生效
    注意，这样做可以区分dev/线上，也可以减小性能影响：if(log.isDebugEnabled()){log.debug();}
**log4j.appender.appender1=org.apache.log4j.日志输出到哪儿**

    ConsoleAppender（控制台）
    FileAppender（文件）
    DailyRollingFileAppender（每天产生一个日志文件）
    RollingFileAppender（文件大小到达指定尺寸时产生一个新的文件）
    WriteAppender（将日志信息以流格式发送到任意指定的地方）
    JDBCAppender（将日志信息保存到数据库中）
**log4j.appender.appender1.File=文件目录及文件${user.home}/logs/...**

**log4j.appender.appender1.MaxFileSize=最大文件大小**

**log4j.appender.appender1.MaxBackupIndex=备份文件个数**

    其中，appender1是在第一行定义过的；
    文件目录及文件，例如，/home/admin/logs/hutudan.log
    最大文件大小，例如，100KB
    备份文件个数，例如，1
**log4j.appender.ServerDailyRollingFile.DatePattern=日志后缀格式**
    
    例如，'.'yyyy-MM-dd
**log4j.appender.appender1.layout=org.apache.log4j.日志布局格式**

    HTMLLayout（以HTML表格形式布局）
    SimpleLayout（包含日志信息的级别和信息字符串）
    TTCCLayout（包含日志产生的时间，执行绪，类别等信息）
    PatternLayout（可以灵活的指定布局格式，常用）
**log4j.appender.appender1.layout.ConversionPattern=日志输出格式**

    例如，%d - %m%n或%d{yyyy-MM-dd HH:mm:ss} %p [%c] %m%n
    %c 输出日志信息所属的类的全名
    %d 输出日志时间点的日期或时间，默认格式为ISO8601，也可以在其后指定格式，比如：%d{yyy-M-dd HH:mm:ss }，输出类似：2002-10-18- 22：10：28
    %f 输出日志信息所属的类的类名
    %l 输出日志事件的发生位置，即输出日志信息的语句处于它所在的类的第几行
    %m 输出代码中指定的信息，如log(message)中的message
    %n 输出一个回车换行符，Windows平台为“rn”，Unix平台为“n”
    %p 输出优先级，即DEBUG，INFO，WARN，ERROR，FATAL。如果是调用debug()输出的，则为DEBUG，依此类推
    %r 输出自应用启动到输出该日志信息所耗费的毫秒数
    %t 输出产生该日志事件的线程名
    可参考：http://blog.sina.com.cn/s/blog_4e4dd5570100qowy.html
**log4j.appender.ServerDailyRollingFile.Append=true**

    例如，不解释，追加往后写便是
**红唇 总结一下：**

    Logger类：完成日志记录，设置日志信息级别
    Appender类：决定日志去向，终端、DB、硬盘
    Layout类：决定日志输出的样式，例如包含当前线程、行号、时间
