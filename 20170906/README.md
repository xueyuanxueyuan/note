# 日志
## Servlet
### 1. Request（请求对象）
    客户端请求中的信息：
        1. 请求协议
        2. 请求来自哪个IP
        3. 请求来自哪个域名
        4. 请求的方式
        5. 请求的资源（做过滤器时使用）
        6. 请求中传递的参数数据
    方法：
        getProtocol() ; // 获取请求中的协议
        getMethod() ； // 获取请求中的方法
        getContextPath(); // 
        getServletPath();
        getRequestUri();
        
        常用方法：
        getParameter();
        //获取获取POST/GET传递的参数值； 
        //用于客户端重定向时，即点击了链接或提交按扭时传值用，
        //即用于在用表单或url重定向传值时接收数据用。 
        getParameterNames();
        //将发送请求页面中form表单里所有具有name属性的表单对象获取(包括button).
        //返回一个Enumeration类型的枚举.
        //通过Enumeration的hasMoreElements()方法遍历.再由nextElement()方法获得枚举的值.
        //此时的值是form表单中所有控件的name属性的值.
        //最后通过request.getParameter()方法获取表单控件的value值.
        getRemoteAddr();
        getRemoteHost();
        getAttribute(); 
        setAttribute();
        removeAttribute();
### 生命周期 
> load-on:   
        loadOnStartup = int值
        该值越小，越早启动，该Servlet的生命周期则在Tomcat服务器启动时创建，而不是普通的Servlet在第一次访问时启动
### 传参数
### response 响应
### 转发和重定向
## JSP 
> HTML + Java   
Html + targ标签   
运行在服务器上的Java代码+HTML代码    
### JSP语法：
> <%   %>中写Java代码段    
<%=  %> 中写语句
### EL（表达式语言）
> ${变量名}相当于request.getAttribute("变量名")
## 转发和重定向的区别
### 什么是转发？  
> 参考答案：  
一个web组件(jsp/servlet)将未完成的处理转交给另一个web组件继续处理。转发的各个组件会共享request和response对象。   
### 什么是重定向?  
> 参考答案：  
服务器向浏览器发送一个状态码302及一个消息头location，浏览器收到后，会立即向location所指向的地址发送请求。  
### 转发与重定向的区别。  
> 参考答案：  
重定向和转发的区别如下：    
    1）地址  转发的地址必须是同一个应用内部的某个组件（不能跨应用，不能跨服务器），重定向的地址没有限制。  
    2）能否共享request转发可以，重定向不行。原因是转发是一次请求，重定向为两次请求，Request的生命周期只能在一次请求内， 请求结束，Request 被删除;  
    3）浏览器地址栏的地址是否变化 转发不变，重定向会变。    
    4）事件是否处理完毕  转发是一件事未做完，重定向是一件事已经做完。 
    
###  转发的特点
> a. 页面跳转之后地址栏的地址是不变的，会是请求的页面的地址。    
b. 请求的参数是可以传递到后面的页面的。    
c. 转发是服务器行为，无法访问外部站点。    
### 重定向的特点
 a. 重定向页面跳转完之后，地址栏中的地址是最后一个页面的地址。   
b. 请求的参数是无法向后传递的，也就是说先前的请求的参数无法传递到后面的页面。    
c. 重定向是可以跳转到外部的站点。   
