
# Windows安装配置Tomcat
## 1. 下载Tomcat 
> 在官网下载Tomcat     
http://tomcat.apache.org/  
在Download选择Tomcat8   
![image](http://note.youdao.com/yws/api/personal/file/969BDD123ABE4A8992BEC7BAD130E3B3?method=download&shareKey=8dde8108eba4b6921022f50e32501e80)   
点进去选择
![image](http://note.youdao.com/yws/api/personal/file/3D5F7873458C4906B34CED589BF0B7E5?method=download&shareKey=e46dca455c33efd016824241bc80f8ec)   
下载Tomcat解压到指定目录；我的在D:\Tomcat\apache-tomcat-8.0.46
![image](http://note.youdao.com/yws/api/personal/file/0BD2CE5ACA144E6380BAB8923C2B8F08?method=download&shareKey=57ddc40aaf972efcb2fb16d6475c08c1)  
---
## 2. 配置Tomcat环境变量
> 打开电脑系统设置高级设置选择环境变量设置新建    
变量名：CATALINA_HOME    
变量值：D:\Tomcat\apache-tomcat-8.0.46   
![image](http://note.youdao.com/yws/api/personal/file/11CD92C9484E4C3FBC0AB4886D8DD93A?method=download&shareKey=57ddc40aaf972efcb2fb16d6475c08c1) 设置Path变量，双击Path然后点击新建添加    
D:\Tomcat\apache-tomcat-8.0.46\bin   
![image](http://note.youdao.com/yws/api/personal/file/245B5A11CDB847E988D444C867932898?method=download&shareKey=57ddc40aaf972efcb2fb16d6475c08c1)
---
## 3. 使用Tomcat
> 窗口加R输入cmd打开终端，输入startup启动Tomcat   
![image](http://note.youdao.com/yws/api/personal/file/AC59FAC87F584F13AAF20109D621C8FA?method=download&shareKey=57ddc40aaf972efcb2fb16d6475c08c1)
在任意浏览器地址栏输入localhost:8080出现Tomcat主页，Tomcat成功安装配置并启动 ![image](http://note.youdao.com/yws/api/personal/file/89C00C957746406780B35F9ABAD2D25A?method=download&shareKey=57ddc40aaf972efcb2fb16d6475c08c1)    
关闭Tomcat：在终端输入shutdown回车即可关闭Tomcat服务器

