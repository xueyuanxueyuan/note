### 常见Web服务器
1.  Apache服务器

 
    Apache仍然是世界上用得最多的Web服务器，市场占有率达60%左右。它源于NCSAhttpd服务器，在NCSA WWW服务器项目停止后，那些使用NCSA WWW服务器的人们开始交换用于此服务器的补丁，这也是Apache名称的由来(pache补丁)。世界上很多著名的网站都是Apache的用户，它的优势主要在于源代码开放、有一支开放的开发队伍、支持跨平台的应用(可以运行在几乎所有的Unix, Windows. Linux系统平台上)，以及其可移植性等。Apache的模块支持非常丰富，虽在速度、性能上不及其他轻量级W eb服务器，但是属于重量级产品，所消耗的内存也比其他Web服务器要高。
官方网站:http://httpd.apache.org/
 
2.  Nginx服务器
 
Nginx ("engine x") 是一个高性能的 HTTP 和 反向代理 服务器，也是一个IMAP/POP3/SMTP 代理服务器。 Nginx 是由 Igor Sysoev 为俄罗斯访问量第二的 Rambler.ru 站点开发的，第一个公开版本0.1.0发布于2004年10月4日。其将源代码以类BSD许可证的形式发布，因它的稳定性、丰富的功能集、示例配置文件和低系统资源的消耗而闻名。2011年6月1日，nginx 1.0.4发布。
Nginx（发音同 engine x）是一款轻量级的Web 服务器/反向代理服务器及电子邮件（IMAP/POP3）代理服务器，并在一个BSD-like协议下发行。由俄罗斯的程序设计师Igor Sysoev所开发，供俄国大型的入口网站及搜索引擎Rambler（俄文：Рамблер）使用。其特点是占有内存少，并发能力强，是目前市面上唯一能和kangleweb server比拼的web server，事实上nginx的并发能力确实在同类型的网页服务器中表现较好，中国大陆使用nginx网站用户有：新浪、网易、腾讯等。
 
官方网站:http://nginx.org/
 
3.  Tomcat服务器
 
    Tomcat是一个开放源代码、运行servlet和JSP Web应用软件的基于Java的W eb应用软件容器。Tomcat Server是根据servlet和JSP规范执行的，因此也可以说Tomcat Server实行了Apache-Jakarta规范，且比绝大多数商业应用软件服务器要好。但是，Tomcat对静态文件、高并发的处理比较弱。
官方网站:http://tomcat.apache.org
 
 
4.  Lighttpd服务器
 
   Lighttpd是由一个德国人写的开源软件，其目标是提供一个专门针对高性能网站，安全、快速、兼容性好并且灵活的Web  Server环境。它具有内存开销低、CPU占用率低、效能好，以及模块丰富等特点。支持FastCGI、CGI. Auth、输出压缩(output compress )、URL重写及Alias等重要功能。Lighttpd跟Nginx一样，也是一款轻量级Web服务器，是Nginx的竞争对手之一。
    官方网站:http://www.lighttpd.net/
 
 
5.  Microsoft IIS 服务器


    Microsoft的W eb服务器产品为Internet Information Server C IIS ) .  IIS是允许在公共Intranet或Internet上发布信息的Web服务器。它是目前最流行的Web服务器产品，很多著名的网站都是建立在IIS平台上的。IIS提供了一个图形界面的管理工具，称为Internet服务管理器，可用于监视配置和控制Internet服务。
   IIS是一种Web服务组件，其中包括Web服务器、FTP服务器、NNTP服务器和SMTP服务器，分别用于网页浏览、文件传输、新闻服务和邮件发送等方面，它使得在网络(包括互联网和局域网)上发布信息成了一件很容易的事。它提供ISAPI ( Intranet Server API)作为扩展Web服务器功能的编程接口;同时，它还提供一个Internet数据库连接器，可以实现对数据库的查询和更新。
    IIS只能运行在Microsoft Windows平台、LinuxNnix平台上，因此须要购买商业的Windows Server操作系统。
演示网站：http://www.yangyufei.com
 
 
6.  IBM WebSphere服务器
 
    WebSphere Application Server是一种T}}能完善、开放的Web应用程序服务器，是IBM电子商务计}}J的核心部分，它基于Java的应用环境，建立、部署和管理Internet和Intranet Web应用程序。这一整套产品目前己进行了扩展，以适应Web应用程序服务器的需要，范围从简单到高级，直到企业级。据IBM官方网站介绍，有10 000多个企业正在使用IBM WebSphere，相对于其他流行的Web服务器而言，应用的数量很少。
 
官方网站:http://www.ibm.com/developerworks/cn/websphere
 
7.  Oracle Weblogic服务器

WebLogic是美商Oracle的主要产品之一，系并购得来。是商业市场上主要的Java（J2EE）应用服务器软件（applicationserver）之一，是世界上第一个成功商业化的J2EE应用服务器, 已推出到12c(12.1.1) 版。而此产品也延伸出WebLogic Portal, WebLogic Integration等企业用的中间件（但当下Oracle主要以Fusion Middleware融合中间件来取代这些WebLogic Server之外的企业包），以及OEPE(Oracle Enterprise Pack for Eclipse)开发工具。
WebLogic最早由 WebLogic Inc. 开发，后并入BEA 公司，最终BEA公司又并入 Oracle公司。
webserver是用来构建网站的必要软件。可用来解析、发布网页等功能，它是用纯java开发的。weblogic本来不是由bea发明的，是它从别人手中买过来，然后再加工扩展。BEA已经被Oracle收购，目前Weblogic最新版本为Oracle Weblogic Server 12c(12.1.1)。其他J2EE Application Server还有IBM的websphere、Sun(Sun公司已经被ORACLE公司收购)的Glassfish、resin等。Apache Tomcat也是常用的Servlet/JSP Container。国内厂商生产的还有像中创软件的Loong AS 9.0(达四级等保,全面支持国产)、东方通的Tongweb、金蝶Apusic应用服务器等。
BEA WebLogicServer拥有处理关键Web应用系统问题所需的性能、可扩展性和高可用性。
与BEA WebLogic Commerce ServerTM配合使用，BEA WebLogic Server可为部署适应性个性化电子商务应用系统提供完善的解决方案。
WebLogic长期以来一直被认为是市场上最好的J2EE工具之一。像数据库或邮件服务器一样，WebLogic Server 对于客户是不可见的，为连接在它上面的客户提供服务。WebLogic 最常用的使用方式是为在internet 或intranet 上的Web 服务提供安全、数据驱动的应用程序。WebLogic对J2EE 架构的支持：WebLogic Server 提供了对SUN J2EE 架构的支持。SUN公司的J2EE 架构是为企业级提供的一种支持分布式应用的整体框架。为集成后端系统，如ERP系统，CRM系统，以及为实现企业级计算提供了一个简易的，开放的标准。
官方网站：http://www.oracle.com/us/corporate/acquisitions/bea/index.html
 
8.  Boa服务器


BOA 服务器是一个小巧高效的web服务器，是一个运行于unix或linux下的，支持CGI的、适合于嵌入式系统的单任务的http服务器，源代码开放、性能高。由于它是一个单任务的Web服务器,只能一次完成用户的请求,而不会fork出新的进程来处理并发的链接请求。但是Boa支持Cgi,能够为Cgi程序fork出一个进程来执行相应的客户请求。
 
官方网站：http://www.boa.org/
  
9.  W3C  Jigsaw服务器



Jigsaw是W3C推出的开源的Web服务器平台，使用Java语言编写，可以安装在有Java运行环境的系统上。做为W3C（World WideWeb Consortium）开发的服务器产品，其作用主要是对新技术的实现做一个示例，而非全功能的商业服务器产品。
不过就Jigsaw 2.0版本而言，它的功能还是超过了目前Web服务器的平均水平。最重要的是，它体现了未来HTTP协议和基于对象的Web服务器技术的发展。如果你希望你的平台支持所有下一代技术，Jigsaw是一个好的选择。
 
官方网站：http://www.w3.org/Jigsaw/
