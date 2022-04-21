# 0 Java EE目录



1. JDBC技术

2. 1. JDBC实现【添加、修改、删除】
   2. JDBC实现查询
   3. DAO（数据访问对象、数据库层开发的模式）

3. Servlet和JSP技术

4. 1. 基本环境配置
   2. Servlet技术
   3. JSP技术
   4. MVC设计模式

5. SSM项目 配置

6. 1. 建工程前准备
   2. 新建Spring工程
   3. Pom.xml文件配置
   4. 主配置文件application.properties配置
   5. 启动类配置
   6. 测试类配置
   7. dao层映射配置

7. SpringBoot 和 Spring

8. 1. 整体说明：

   2. 1. Java技术说明
      2. 项目说明
      3. 框架说明

   3. 实际操作 与 理解

   4. 1. SpringBoot项目（环境配置）
      2. Spring框架

9. Mybatis框架

10. 1. 主配置文件配置 及 实体类实现

    2. DAO层使用Mybatis框架

    3. 业务层调用DAO层

    4. 通过Junit测试

    5. 补充

    6. 1. Mybatis实现分页功能
       2. Mybatis传递多参写法
       3. Mybatis多表查询

11. Spring MVC

12. 1. SpringMVC框架（编写控制器的步骤）
    2. 控制器获取前台数据的方式
    3. 控制器相应前台数据的方式

13. Postman测试接口

14. 1. 发送参数测试接口
    2. 发送JSON对象测试接口









# 1 Java EE框架及技术说明



Java语言->Java技术->Java框架->Java项目





SSM：Spring + SpringMVC + Mybatis



SSH：Spring + Struts2 + Hibernate









## SpringBoot说明：

- 默认单实例，多线程







## 单实例实现：

1. 将构造方法私有化
2. 通过一个方法给一个对象

- 好处：内存中只有一个实例，减少内存开销；频繁的创建销毁，如控制层，SpringBoot进行了私有化。配合多线程，使用同步，避免并发操作下可能会产生的问题





## Spring说明：

- IoC：控制反转，配合DI（注入）
- AOP：面向切片，如事物和日志的声明式处理







## Maven说明：

- 项目管理工具
- 包含一个项目对象模型（Project Object Model），即pom.xml文件
- 包含一组标准集合
- 包含一个项目生命周期
- 包含一个依赖管理系统
- 包含用来运行定义在生命周期阶段（phase）中插件（plugin）目标（goal）的逻辑
- 使用原理：明确定义一个项目对象模型来描述项目，Maven应用横切的逻辑，这些逻辑来自一组共享的（或自定义的）插件
- 目前项目所需的jar包大部分都是基于maven平台管理







## Spring常见注解：

- @ComponentScan：自动扫描类并注册为bean

- @Controller：应用在控制层

- @Service：应用在业务层

- @Reponsitory：应用在dao层

- @SpringBootApplication：@Configuration加@EnableAutoConfiguration加@ComponentScan

- @Configuration：相当于传统的xml文件，即配置文件

- @EnableAutoConfiguration：SpringBoot自动配置（auto-configuration）尝试根据添加的jar包自动配置Spring项目，及自动配置

- Component：一个元注解，注册成为Spring管理的bean

- @Autowired：DI依赖注入用

- @Bean：方法上方使用，声明返回一个bean，返回的bean对应的类中，可以定义init方法和destroy方法，即@Bean(initMethod="init",destroyMethod="destroy")，在构造之后执行init，在销毁前执行destroy

- @Transactional：声明事务，应用在批量修改数据库数据的业务，所有异常都回滚@Transactional(rollbackFor = Exception.class)，Excel导入时能用上

- @RequestMapping：用来映射web请求（访问路径和参数），用在类或方法上方。方法上方的注解会继承在类上的路径。

- - 也支持Servlet的request和response作为参数，也支持对request和response的媒体类型进行配置。包含value（路径），produces（返回媒体类型和字符集），method（请求方式）等属性
  - @GetMappring、@DeleteMapping、@PutMapping、@PostMapping都是特殊的@RequestMapping，只处理一种请求

- @ResponseBody：将返回值放在response体内，供前端接收，返回的是前端需要的数据，而非页面

- @RequestBody：允许request的参数在request体中，而不是在url后。用在参数前

- @RestController：组合注解，组合了@Controller和@ResponseBody，当该控制层只需要交互数据时使用





## Java Web三大器

- 即过滤器、监听器、拦截器

- 过滤器：

- - 对请求进行检测和修改，常用设置编码、敏感词汇过滤、压缩响应信息
  - 通过回调函数
  - 依赖servlet容器
  - 系统级

- 监听器：

- - 常用监听Session、监听request、response等的状态
  - 通过事件
  - 系统级

- 拦截器：

- - 拦截未登录用户、审计日志
  - 通过Java反射机制
  - 不依赖servlet容器
  - 非系统级







# 2 JDBC技术

**20200819**	 



- JDBC概念：Java数据库连接标准。JDBC API。是JavaEE平台核心技术之一。



可以去官网下载jar包



- 手动配置环境

- 1. 工程下新建lib文件夹

  2. 将上面的mysql驱动jar包复制到lib下

  3. 把jar包添加到类路径中

  4. - 第一种：jar包右键-build path
     - 第二种：工程右键-属性-build path





## （01）JDBC实现【添加、修改、删除】

- 需要先手动配置环境

- 步骤：（7步）

- 1. 加载驱动
  2. 获取连接
  3. 设置事务（添加、修改、删除）
  4. 获取语句
  5. 执行SQL
  6. 提交事务（添加、修改、删除）
  7. 关闭连接

- 需要导包：JDBC API

- 1. **import** java.sql.Connection;
  2. **import** java.sql.DriverManager;
  3. **import** java.sql.PreparedStatement;
  4. **import** java.sql.ResultSet;
  5. **import** java.sql.SQLException;

- 手动配置环境

- 1. 工程下新建lib文件夹

  2. mysql驱动jar包复制到lib下

  3. 把jar包添加到类路径中

  4. - 第一种：jar包右键-build path
     - 第二种：工程右键-属性-build path



**Statement说明：**

​	●**用于执行静态 SQL 语句并返回它所生成结果的对象。**

​	●**在默认情况下，同一时间每个 Statement 对象在只能打开一个 ResultSet 对象。因此，如果读取一个 ResultSet 对象与读取另一个交叉，则这两个对象必须是由不同的 Statement 对象生成的。**



**PreparedStatement说明：**

​	●**为Statement子接口；**

​	●**表示预编译的 SQL 语句的对象。SQL 语句被预编译并存储在 PreparedStatement 对象中。然后可以使用此对象高效地执行该语句。**





**第一步：加载驱动、实现类**

- JDBC mysql 连接参数

Class.*forName*("com.mysql.cj.jdbc.Driver");





**第二步：获取数据库连接**

- 参数：

- - url：数据库访问地址
  - user：用户名
  - password：密码

Connection conn = DriverManager.*getConnection*("jdbc:mysql://127.0.0.1:3306/mysql0819?useUnicode=true&characterEncoding=UTF-8&serverTimezone=UTC", "root", "123321"); 





**第三步：设置事务为非自动提交（手动提交：开发人员决定何时提交）**

conn.setAutoCommit(**false**);





**第四步：获取语句对象**

- 注意：SQL语句的句式和数据分离
- 原因：预编译 后传参 的原理，防止注入攻击、效率高。可百度



**？：表示占位**



**增加的**SQL：

String sql = "insert into person values(null,'tom',12.34,'20200819'";

String sql = "insert into person values(?,?,?,now())";

String sql = "insert into person values(?,?,?,?)";

**修改的**SQL：

String sql = "update person set name = ? where id = ? ";

**删除的**SQL：

String sql = "delete from person where id = ? ";



**添加**SQL语句到PerparedStatement对象：

PreparedStatement ps = conn.prepareStatement(sql);



**装填参数值：（第一个参数代表第几个？）**

**添加操作：**

ps.setInt(1, 9);

ps.setString(2, "哈哈");

ps.setDouble(3, 3000.23);

ps.setString(4, "20200819");

**修改操作：**

ps.setString(1, "张三");

ps.setInt(2, 1);

**删除操作：**

ps.setInt(1, 1);





**第五步：执行**

- 返回的整数表示 添加、修改、删除的个数

**int** count = ps.executeUpdate();

System.***out\***.println(count);





**第六步：提交事务**

conn.commit();





**第七步：关闭连接**

conn.close();





**补充注意：选中前七步，添加捕获异常**



##  

## 补充：

**注入攻击**

- 登录功能

- - 页面

  - - 用户 abc
    - 密码 ' or '1' = '1

- 登录功能

- - 正确的SQL：”select * from person where name = 'abc' and password = '123' "
  - 注入攻击下的SQL：”select * from person where name = 'abc' and password = '' or '1' = '1' “

- **结果导致：无论账号密码对不对都能登录，后台会被监控！！！**



##  

## （02）JDBC实现【查询】

- 需要先手动配置环境		

- JDBC技术实现查询的5个步骤

- 1. 加载驱动
  2. 获取连接
  3. 获取语句
  4. 执行SQL
  5. 关闭连接

​		



**第一步：加载驱动**

Class.*forName*("com.mysql.cj.jdbc.Driver");





**第二步：获取数据库连接**

Connection conn = DriverManager.*getConnection*("jdbc:mysql://127.0.0.1:3306/mysql0819?useUnicode=true&characterEncoding=UTF-8&serverTimezone=UTC", "root", "root"); 





**第三步：获取语句对象**

String sql = "select * from person where name like ? and money between ? and ? ";



PreparedStatement ps = conn.prepareStatement(sql);



**查询操作参数：**

ps.setString(1, "%小%");

ps.setDouble(2, 300);

ps.setDouble(3, 4000);





**第四步：** 执行SQL语句

ResultSet rs = ps.executeQuery();

**while**(rs.next()) {

​	System.***out\***.println(rs.getInt("id") + rs.getString("name") + rs.getDouble("money") +rs.getString("bir"));

}





**第五步：关闭连接**

conn.close();





**补充注意：选中全五步，添加捕获异常**





##  

##  

## （03）DAO（数据访问对象、数据库层开发的模式）

- 理解：DAO（思想）+JDBC（技术）
- DAO：数据访问对象。项目数据层开发的设计模式、指导思想。
- ORM：对象关系映射
- 映射关系如下图：

| Java语言（面向对象的语言 | Mysql数据库（关系行数据库） |
| ------------------------ | --------------------------- |
| 类                       | 表                          |
| 变量                     | 字段                        |
| 对象                     | 记录                        |

- 步骤：

- - 先建包：哪个都行

  - - com.wyh.bean
    - com.wyh.entity
    - com.wyh.pojo

  - 实体类：映射表结构，在上面任意一个包中，写一个对应的实体类，如：Person.java

  - DAO接口

  - - com.wyh.dao.PersonDAO（设计功能的接口）

  - DAO实现

  - - com.wyh.dao.PersonDAOImpl（实现接口的类）

# 3 Servlet



Servlet的前世今生、JavaWeb三大件、如何编写一个Servlet： https://www.zhihu.com/question/21416727/answer/690289895

# 3 Servlet和JSP技术

**20200820**



**知乎 浅析JSP：**[**https://zhuanlan.zhihu.com/p/42343690**](https://zhuanlan.zhihu.com/p/42343690)



**servlet原理：**[**https://www.zhihu.com/question/21416727?sort=created**](https://www.zhihu.com/question/21416727?sort=created)



1. request 请求对象　 类型 javax.servlet.ServletRequest 作用域 Request
2. response 响应对象 类型 javax.servlet.SrvletResponse 作用域 Page
3. pageContext 页面上下文对象 类型 javax.servlet.jsp.PageContext 作用域 Page
4. session 会话对象 类型 javax.servlet.http.HttpSession 作用域 Session
5. application 应用程序对象 类型 javax.servlet.ServletContext 作用域 Application
6. out 输出对象 类型 javax.servlet.jsp.JspWriter 作用域 Page
7. config 配置对象 类型 javax.servlet.ServletConfig 作用域 Page
8. page 页面对象 类型 javax.lang.Object 作用域 Page
9. exception 例外对象 类型 javax.lang.Throwable 作用域 page



# forward与sendRedirect区别

https://blog.csdn.net/m0_37550986/article/details/81989592







- 基本环境配置

- - 配置Tomcat服务器

1. 新建Server工程

2. - 修改配置文件：

   - - Server工程->Tomcat->server.xml 修改port=“8082”

3. 创建web工程

4. - WebContent下新建html文件

5. 发布运行停止

6. - 发布

   - - 服务器视图
     - 右键add and remove
     - 窗口选中工程add

   - 运行

   - - 服务器视图
     - Tomcat右键start
     - 出现 Server startup in 多少 ms 服务器启动成功
     - 访问本机：http://127.0.0.1:8080/web01/a.html

   - 停止

   - - 服务器视图
     - Tomcat右键stop



通信方式

| 浏览器       | <-Tomcat服务器->           | Mysql服务器 |
| ------------ | -------------------------- | ----------- |
| JavaScript-> | <- Java语言->              | SQL语句     |
| JSP技术->    | <- Servlet技术/JDBC技术 -> | SQL语句     |





## （01）Servlet技术

- 介绍：Servlet技术是JavaEE平台核心技术之一。控制层的技术标准API。

- 注意：

- 1. 控制层的对象 由 Tomcat服务器来实例化
  2. 控制层的方法 由 Tomcat服务器来调用
  3. Tomcat服务器（容器）提供Java组件的运行环境，并管理组件的生命周期



**（**1）Servlet生命周期（编写控制器）

- 第一阶段：初始化阶段：init方法

- - 当请求第一次到达的时候 被调用，只调用一次

- 第二阶段：处理业务阶段：service方法

- - 当请求每次到达的时候 被调用，调用多次

- 第三阶段：销毁阶段：destroy方法

- - 当服务器停止的时候 被调用，只调用一次



**配置控制器：**

1. src中新建包：com.wyh.controller

2. 包下建控制器类：Action01，继承HttpServlet

3. 1. 用来接收前台请求、和前台进行交互

4. 类打开右键，Source->Override/Implement Methods

5. 1. ->勾选爷爷类中的init()->ok

   2. - init()：初始化方法

   3. ->勾选父类中的service()->ok

   4. - service(ServletRequest , ServletResponse)：处理业务方法

      - - ServletRequest请求对象
        - ServletReaponse回应对象

   5. ->勾选父类中的destroy()->ok

   6. - destroy()：销毁方法



**（**2）web.xml文件中配置（配置控制器）

**配置**servlet控制器：

**WebContent->WEB-INF->web.xml** 中：

- servlet标签中：注册Servlet组件

- - servlet-class标签中写：com.wyh.controller.Action01
  - servlet-name标签中写：随便起名

- servlet-mapping标签中：配置Servlet请求映射

- - servlet-name标签中写：随便起名（和上面相同，用来映射控制器）
  - url-pattern标签中写：/b（用来被访问）



**测试：访问**127.0.0.1:8080/web01/b

- 后台控制台中会显示调用init和service方法 输出的结果









## （02）JSP技术

- 介绍：JSP技术是JavaEE平台核心技术之一，视图层的技术 标准API

- JSP运行原理：Tomcat将 *.jsp页面 -> *.java -> *.class -> 运 行

- JSP技术本质：JSP = HTML语言 + Java语言（都写在<% Java语言 %>中) + CSS语言 + JavaScript语言

- 需要掌握

- - JSP基础语言入门：掌握在JSP中嵌入简单点Java代码即可

  - - <% Java语言 %>

  - EL表达式语言：用来 获取并显示 后台发送到前台的Java数据用的

  - - ${ EL表达式 }

- 各个技术的说明

| 视图层  | 控制层      | 业务层   | 数据层   | 企业信息系统层 |
| ------- | ----------- | -------- | -------- | -------------- |
| View    | Controller  | Service  | DAO      | EIS            |
| JSP技术 | Servlet技术 | Java语言 | JDBC技术 | Mysql（SQL）   |

- 建文件：WebContent->page->a.jsp（选HTML5模版），jsp页面中加点内容
- 改eclipse属性：Web->JSP Files->Encoding 选第一个UTF-8
- 访问：localhost:8080/web01/page/a.jsp



**补充举例说明：**

**Servlet**后台发送数据、JSP EL表达式接收数据方式：

- 后端Action01.java的**service方法**中：

- 1. Servlet控制器发送数据到前端的方法(参数一：字符串，参数二：任何类型数据都行)

  2. 1. 发送字符串：req.getSession().setAttribute(“key1”,”你好”);
     2. 发送对象：req.getSession().setAttribute(“key2”, new Person(“ 张三” , 23 ) );

  3. 跳转页面：resp.sendRedirect(“page/a.jsp)”;

- 前端a.jsp中接收显示数据：

- 1. 取字符串：${ key1 }
  2. 取对象：${ key2.name } ${ key2.name }



## JSP内置对象：

- 说明：https://blog.csdn.net/u014199143/article/details/80620571



| **对象**        | **描述**                                                     |
| --------------- | ------------------------------------------------------------ |
| **application** | **ServletContext****类的实例，与应用上下文有关，应用对象**   |
| **pageContext** | **PageContext****类的实例，提供对****JSP****页面所有对象以及命名空间的访问，实例对象** |
| **page**        | **类似于****Java****类中的****this****关键字，页面对象**     |
| **session**     | **HttpSession****类的实例，回话对象**                        |
| **request**     | **HttpServletRequest****接口的实例，请求对象**               |
| **response**    | **HttpServletResponse** **接口的实例****,****相应对象**      |
| **out**         | **JspWriter****类的实例，用于把结果输出至网页上****,****输出对象** |
| **config**      | **ServletConfig****类的实例****,****配置对象**               |
| **exception**   | **Exception****类的对象，代表发生错误的****JSP****页面中对应的异常对象****,****异常对** |









# 转发 和 重定向：



## 转发（forward）

●**地址栏：不发生变化，显示的是上一个页面的地址**

●**请求次数：只有1次请求**

●**根目录：http://localhost:8080/项目地址/，包含了项目的访问地址**

●**请求域中数据不会丢失**

##  

## 重定向（sendRedirect）

●**地址栏：显示新的地址**

●**请求次数：2次**

●**根目录：http://localhost:8080/ 没有项目的名字**

●**请求域中的数据会丢失，因为是2次请求**













## （03）MVC设计模式

- web层 = 视图层（web前台） + 控制层（web后台）

- 概念：MVC是web层开发的设计模式

- - **模型M：Model** 
  - **页面V：View** 
  - **控制器C：Controler** 



| M    | Model      | 模型层 | 后台发往前台的数据 |
| ---- | ---------- | ------ | ------------------ |
| V    | View       | 视图层 | 页面               |
| C    | Controller | 控制层 | 控制器             |



**登录**MVC案例：

- 登录页面：login.jsp

- - 写一个表单，action=“web.xml中的url-pattner标签中写的路径，即/login”

- 成功页面：main.jsp

- 登录控制器：

- - 写一个LoginAction继承HttpServlet接口

  - 生成service方法，在该方法中处理请求业务

  - 1. 获取帐号、密码：

    2. 1. String username = req.getParameter(“username”);
       2. String password = req.getParameter(“password”);

    3. 验证是否合法，设置跳转页面

    4. 1. String path = “”;

       2. if语句判断帐号密码

       3. 1. 成功：path = “page/main.jsp”;
          2. 失败：path = “page/login.jsp”;

    5. 跳转页面

    6. 1. resp.sendRedirect(path);

    7. 配置LoginAction控制器，前端WEB-INF文件夹的web.xml中

    8. 1. name -> login
       2. class -> com.wyh.controller.LoginAction 
       3. name -> login
       4. url -> /login （与前端表单的action属性必须相同）

# 9 Druid 连接池



- Spring默认数据连接池

![Screen Shot 2020-09-25 at 21.59.40.png](/blob:file:/a46c19fc-7149-4dc7-9a4d-a112f0abd454)

- Druid是阿里巴巴开发的
- 现阶段最好的连接池
- 用来控制并发





## pom.xml文件中引入Druid：



​    <dependency>

​      <groupId>com.alibaba</groupId>

​      <artifactId>druid-spring-boot-starter</artifactId>

​      <version>1.1.21</version>

​    </dependency>







## 主文件中配置如下：



\#Druid

spring.datasource.druid.url=jdbc:mysql://127.0.0.1:3306/test3?characterEncoding=utf-8&allowMultiQueries=true&zeroDateTimeBehavior=convertToNull&serverTimezone=Asia/Shanghai

spring.datasource.druid.username=root

spring.datasource.druid.password=123456

spring.datasource.druid.driver-class-name=com.mysql.cj.jdbc.Driver

\#初始化时建立物理连接的个数

spring.datasource.druid.initial-size=5



\#最小连接池数量

spring.datasource.druid.min-idle=5



\#最大连接池数量 maxIdle已经不再使用

spring.datasource.druid.max-active=20



\#获取连接时最大等待时间，单位毫秒

spring.datasource.druid.max-wait=60000



\#申请连接的时候检测，如果空闲时间大于timeBetweenEvictionRunsMillis，执行validationQuery检测连接是否有效。

spring.datasource.druid.test-while-idle=true



\#既作为检测的间隔时间又作为testWhileIdel执行的依据

spring.datasource.druid.time-between-eviction-runs-millis=60000



\#销毁线程时检测当前连接的最后活动时间和当前时间差大于该值时，关闭当前连接

spring.datasource.druid.min-evictable-idle-time-millis=30000



\#用来检测连接是否有效的sql 必须是一个查询语句

\#mysql中为 select 'x'

\#oracle中为 select 1 from dual

spring.datasource.druid.validation-query=select 'x'



\#申请连接时会执行validationQuery检测连接是否有效,开启会降低性能,默认为true

spring.datasource.druid.test-on-borrow=false



\#归还连接时会执行validationQuery检测连接是否有效,开启会降低性能,默认为true

spring.datasource.druid.test-on-return=false



\#当数据库抛出不可恢复的异常时,抛弃该连接

\#spring.datasource.druid.exception-sorter=true



\#是否缓存preparedStatement,mysql5.5+建议开启

\#spring.datasource.druid.pool-prepared-statements=true

\#当值大于0时poolPreparedStatements会自动修改为true

spring.datasource.druid.max-pool-prepared-statement-per-connection-size=20



\#配置扩展插件

\#spring.datasource.druid.filters=stat,wall



\#通过connectProperties属性来打开mergeSql功能；慢SQL记录

spring.datasource.druid.connection-properties=druid.stat.mergeSql=true;druid.stat.slowSqlMillis=500



\#合并多个DruidDataSource的监控数据

spring.datasource.druid.use-global-data-source-stat=true



\#设置访问druid监控页的账号和密码,默认没有

spring.datasource.druid.stat-view-servlet.enabled=true

spring.datasource.druid.stat-view-servlet.login-username=admin

spring.datasource.druid.stat-view-servlet.login-password=admin

# 10 日志



- 用于弥补mysql运行不可见，日志可以打印出来sql语句
- 可以设置每天生成日志文件
- 生成的日志在工程下logs文件夹中
- **注意：文件夹名不可以改成config**





**将下面文件夹粘贴到resource中：**





**在logback.xml文件中需要修改日志输出根目录，如下：**

- **用traffic项目举例，在logs/后面加上项目名/即可**



  *<!--*定义日志文件的存储地址 勿在 *LogBack* 的配置中使用相对路径*-->*

  <property name="LOG_HOME" value="./logs/traffic" />







**主配置文件中添加：**



**#日志**

[logging.level.com](http://logging.level.com).公司名.项目名.dao=debug 

logging.config=classpath:conf/logback.xml





举例：

logging.level.com.rain.pb_1.test=debug 

logging.config=classpath:conf/logback.xml





# 11 分页



# 12 JPA



@Query的使用方式：

https://blog.csdn.net/zpz_326/article/details/81359061



- JPA是Java Persistence API的简称，中文名Java持久层API

- JPA是JDK5.0后提出的Java持久化规范

- JPA由EJB 3.0软件专家组开发，作为JSR-220实现的一部分

- JPA的宗旨是为POJO提供持久化标准规范

- JPA的出现，主要是为了简化持久层开发以及整合ROM技术，结束Hibernate、Toplink、JDO等ORM框架各自为营的局面。

- JPA是在吸收现有ORM框架的基础上发展而来

- 易于使用、伸缩性强

- 包含下面3方面的技术：

- 1. ORM映射元数据：JPA支持XML和JDK5.0注解两种元数据的形式，框架据此实现实体对象持久到数据库表中
  2. API：操作实体对象，执行CRUD操作
  3. 查询语言：通过面向对象的JPQL查询，而非面向数据库的查询语言，避免程序的SQL语句紧密耦合

##  

##  

## JPA与Spring Data JPA的关系：

- JPA是一个接口，规范
- Spring data Jpa是一个框架
- Spirng data Jpa是Spring提供的一套简化JPA开发的框架，按照约定好的【方法命名规则】写dao层接口，就可以在不写接口实现的情况下，实现对数据库的访问和操作。同时提供了很多除了CRUD之外的功能，如分页、排序、复杂查询等等。
- Spring Data JPA 可以理解为 JPA 规范的再次封装抽象，底层还是使用了 Hibernate 的 JPA 技术实现。如图：



**JPA**接口约定命名规则：







## SB集成JPA的两种方法：

1. 在建工程时，勾选Spring Data JPA
2. 在建好的工程中，在pom.xml文件中添加依赖





## SB中使用JPA+Oracle的使用步骤：



**（**1）实体类

- 实现接口：Serializable
- 类定义处上方加注释：@Entity、@Table(name = "Emp")
- 主键上加注释：@Id
- 如果实体类的名和数据表的名一样的话，@Table后面可以不写name
- 主键必须有
- @Column用在非主键列的成员变量上，当成员和表字段不同名时设置name即可，如：@Colunm(name = "empname")，该注解也可用在属性的getter方法之前
- **如在MySQL+JPA中，主键如果是自增长**，在主键成员上添加注解：@GeneratedValue(strategy = GenerationType.IDENTITY)



@Entity

@Table(name = "EMP")

public class Emp implements Serializable {



 // 生成随机数：悬停，选第二个

 private static final long serialVersionUID = -2483125224181722954L;



 @Id

 private BigDecimal empno;



 private String ename;

 private String job;

 private BigDecimal mgr;

 private Date hiredate;

 private BigDecimal sal;

 private BigDecimal comm;

 private BigDecimal deptno;



 // 生成getter和setter方法



}





**（**2）Dao层继承接口JapRepository

- 实现了该接口，就不需要添加Dao层注解了，即@Repository

- 基础的Repository提供了最基本的数据访问功能，其几个子接口扩展了一些功能：

- 1. Repository：仅仅是一个标识，表明任何继承它的均为仓库接口类
  2. CrudRepository：继承Repository，实现了一组CRUD相关的方法
  3. PagingAndSortingRepository：继承CrudRepository，实现了一组分页排序相关的方法
  4. JapRepository：继承PagingAndSortingRepository，实现了一组JPA规范相关的方法
  5. 自定义的xxxRepository需要继承JpaRepository，这样的接口就具备了通用的Dao层的能力



public interface EmpDao extends JpaRepository<Emp, Integer> { }





**（**3）业务层和控制层中，引入Dao层对象，即可使用Dao层中的方法：





@RestController

public class EmpController {



  @Autowired

  private EmpDao empDao;



  @RequestMapping("getAll")

  public List<Emp> getList(){

​    return empDao.findAll();

  }



  @RequestMapping("getPageEmp")

  public Page<Emp> getPageEmp(){

​    Pageable pageable = PageRequest.of(1,5);// 参数：页码，条数

​    return empDao.findAll(pageable);

  }



}



# 13 MD5





- spring提供的





## 使用步骤：



**（**1）声明字符串



String pwd = "123321";



**（**2）生成加密字符串



String password = DigestUtils.*md5DigestAsHex*(pwd.getBytes());





# 14 拦截器



## 配置拦截说明：



**SpringMVC** 拦截器拦截 /* 和 /** 的区别：

/* 是拦截所有的文件夹，不包含子文件夹

/* ： 匹配一级，即 /add , /query 等



/** 是拦截所有的文件夹及里面的子文件夹

/** ： 匹配多级，即 /add , /add/user, /add/user/user… 等



## 实现登录拦截的步骤说明：

- 拦截器是作用在控制层之前的
- 若需要跨域需要下面的CorosConfig.java工具类，设置全局跨域；若需要缓存则需要下面包中的RedisConfig.java工具类







- 在工程中粘贴下面的工具类





**（**1）在config包中新建配置类：InterceptorConfig，该类实现WebMvcConfigurer

**，并在该类上方添加注解：**@Configuration



**（**2）写一个登录拦截器实现类：config.LoginInterceptor，该类实现接口：HandlerInterceptor



**（**3）登录拦截器中注入缓存工具类，并重写方法：



@Autowired

private RedisUtil redisUtil;



@Override

public boolean preHandle(HttpServletRequest request, HttpServletResponse response, Object handler) throws Exception {

  boolean flag = false;

  String account = request.getHeader("account");

  String token = request.getHeader("token");



  if(account != null && token != null && account != "" && token !="") {

​    Object tokenValue = redisUtil.get(account);

​    if(tokenValue != null){

​      if(token.equals(tokenValue)){

​        flag = true;

​      }

​    }

  }

// 拦截后在响应对象中添加信息，添加方式JSON.parse("返回的JSON对象")

  if(!flag){

​    response.setContentType("application/json; charset=utf-8");

​    response.setCharacterEncoding("utf-8");

​    response.getWriter().write(JSON.*parse*("{result: false}").toString());

  }



  return flag;

}





**（**4）InterceptorConfig中添加方法



@Override

public void addInterceptors(InterceptorRegistry registry) {

  // addPathPatterns(拦截内容)，excludePathPatterns(例外)

registry.addInterceptor(loginInterceptor()).addPathPatterns("/*").excludePathPatterns("/login.html","/checkLogin");

}



@Bean

public LoginInterceptor loginInterceptor(){

  return new LoginInterceptor();

}



**（**5）控制层实现



@RequestMapping("checkLogin")

public Map<String, Object> checkLogin(@RequestBody Map<String, Object> parms){

  return userService.checkLogin(parms);

}







**（**6）前端实现



- 引入js

<script src="js/axios.js"></script>

<script src="js/vue.js"></script>



- body中添加



    <div id="app">

​    id: <input type="text" v-model="parms.account" /><br/>

​    pwd:<input type="text" v-model="parms.password" /><br/>

​    <button type="button" @click="checkLogin">登录</button>

​    <hr>

​    <button type="button" @click="getList">获取数据</button>

  </div>

    <script>

​    var vm = new Vue({

​      el: '#app',

​      data: {

​        parms: {

​          account: '',

​          password: ''

​        },

​        header: {

​          account: '',

​          token: '',

​        }

​      },

​      methods: {

​        checkLogin: function (){

​          axios.request({

​            url: '/checkLogin',

​            method: 'post',

​            data: this.parms

​          }).then(res => {

​            let result = res.data.result

​            if(result == '1'){

​              this.header.account = res.data.userInfo.account

​              this.header.token = res.data.token

​            } else {

​              *alert*("failed")

​            }

​          })

​        },

​        getList: function (){

​          console.log(this.header)

​          axios.request({

​            url: '/getCityList',

​            headers: this.header

​          }).then(res => {

​            *alert*(res.data.length)

​          })

​        }

​      }

​    })

  </script>

# 15 合并注解



## 新建注解：



import java.lang.annotation.Documented;

import java.lang.annotation.ElementType;

import java.lang.annotation.Retention;

import java.lang.annotation.RetentionPolicy;

import java.lang.annotation.Target;



import org.springframework.core.annotation.AliasFor;

import org.springframework.web.bind.annotation.CrossOrigin;

import org.springframework.web.bind.annotation.RequestMapping;

import org.springframework.web.bind.annotation.RestController;



@Target(ElementType.*TYPE*)

@Retention(RetentionPolicy.*RUNTIME*)

@Documented

@RestController

@RequestMapping

public @interface LanB {

  @AliasFor("path")

  String[] value() default {};



  @AliasFor("value")

  String[] path() default {};

}





## 使用方法：



@LanB("Usergroups")

public class Usergroups {}



# 16 获取请求者的IP



参考：https://www.jianshu.com/p/3871a2c47c09



# 17 Excel 导入导出



## 说明：

- EasyPoi可以处理简单的导入导出
- 导入导出都是基于注解的，所以需要在实体中添加注解
- 因为有需求中国式报表的情况，所以出现了一个不错的收费软件：帆软，支持页面中显示中国式报表，和直接导出
- 导出：一般🈯️基于实体类导出Excel模版或Excel带数据的文件
- 导入：一般🈯️基于Ecxel文件导入数据库或硬盘中





**EasyPoi**教程说明：http://easypoi.mydoc.io



**帆软官网：**https://www.fanruan.com





## 导出步骤：

**
** （1）导入EasyPoi，pom.xml文件中添加依赖：



​    <dependency>

​      <groupId>cn.afterturn</groupId>

​      <artifactId>easypoi-spring-boot-starter</artifactId>

​      <version>4.1.3</version>

​    </dependency>





**（**2）修改实体：

- 在需要导出的属性上加注解
- 标注的属性将作为文件中的列名导出



@Excel(name = "性别")

private String sex;





**（**3）导入工具类：







**（**4）控制层写功能：

- 写完需要抛出一个IO异常



  @RequestMapping("toExcel")

  public void toExcel(HttpServletResponse response) throws IOException {

​	// 参数

​    Map<String,Object> parms = new HashMap<>();

​	// 调用

​    List<Employee> employeeList = employeeService.getExcelList(parms);

​	// 导出Excel，参数说明：数据、实体类名、Excel中的sheet名、实体类、文件名、响应对象

​    ExcelUtils.exportExcel(employeeList,"员工信息", "员工", Employee.class,"员工信息表", response);

  }



**（**5）业务层添加功能：

- 业务层接口添加：



  List<Employee> getExcelList(Map<String,Object> parms);



- 业务层实现类添加：



  @Override

  public List<Employee> getExcelList(Map<String, Object> parms) {

​    return employeeDao.getEmpList(parms);

  }





**（**6）前端实现

- 先写好一个按钮，将下面的函数绑定到需要的事件上



**通过**js源码实现



toExcel() {

​	window.location.href = "/toExcel"

}





=================================





## 导入步骤：

- 上传的重点在于多条添加



**（**1）控制层添加功能：



  @RequestMapping("fileUpload")

  public void fileUpload(@RequestParam("file1") MultipartFile file) throws IOException {

​    if (!file.isEmpty()){

​      String fileStr = "F:/Workspace/FileUpload/"+file.getOriginalFilename();

​      File fileNew = new File(fileStr);

​      file.transferTo(fileNew);

​      importExcel(fileStr);

​    }

  }



  public void importExcel(String filePath) throws IOException {

​	// 参数说明：文件路径，表头行数，标题行数，实体

​    List<Employee> employeeList = ExcelUtils.importExcel(filePath,1,1,Employee.class);

​	// 添加的结果

​    int result = employeeService.addList(employeeList);

​    System.out.println(result);

  }





**（**2）业务层添加功能：

- 接口中添加：

 

  int addList(List<Employee> employeeList);



- 实现类中添加：



  @Override

  public int addList(List<Employee> employeeList) {

​    return employeeDao.addList(employeeList);

  }





**（**3）DAO层添加功能：

- 接口中添加：



  int addList(List<Employee> employeeList);



- mapper中添加方法映射：



 <insert id="addList" parameterType="list">

  insert into t_employee(id, `name`, sex, school, positionid) values

  <foreach collection="list" item="item" separator=",">

   (#{item.id, jdbcType=INTEGER},

   \#{item.name, jdbcType=VARCHAR},

   \#{item.sex, jdbcType=VARCHAR},

   \#{item.school, jdbcType=VARCHAR},

   \#{item.pid, jdbcType=INTEGER},)

  </foreach>

 </insert>





**（**4）前端

- 直接正常文件下载即可，参考【文件上传/下载】中的文件下载
- 下面是通过axios实现文件下载：



​      excel: function () {

​        axios.request({

​          method: 'post',

​          url: '/toExcel',

​          responseType: 'blob',

​          params: {

​            uid: 'a'

​          }

​        }).then(function (res) {

​          if (!res.data) {

​            return

​          }

​          let url = window.URL.createObjectURL(new Blob([res.data]));

​          let link = document.createElement('a');

​          link.style.display = 'none';

​          link.href = url;

​          link.setAttribute('download', '测试excel.xls');



​          document.body.appendChild(link);

​          link.click()



​        })

​      }

# 18 加密

#  

**Java**实现AES加密 https://www.cnblogs.com/loong-hon/p/10145060.html





java中简单实现MD5加密 https://www.iteye.com/blog/csuliunian-1157312



**Java生成MD5的两种方式** https://blog.csdn.net/junmoxi/article/details/80841555





Md5 java实现 https://blog.csdn.net/jankingmeaning/article/details/84778668#_1

 



# 18 文件上传/下载

#  

# 上传-后端操作



⭐️说明：

- 不同浏览器可能有传文件名不同的可能，必要时需要判断，文件名是否包含绝对路径
- 基于SpringMVC，所以必须有SpringMVC服务
- 通过SpringMVC提供的MultipartFile对象进行文件上传操作

![Pasted Graphic.png](/blob:file:/62e06ec1-9df6-4a77-a3d8-6b23b6cdc379)

##  

# 试一下相对路径



## 步骤：



**（**1）控制层添加注解

- 如需跨域，需要添加@CrossOrigin



@RestController



**（**2）写上传方法



@RequestMapping("fileUpload”)

public void upload(@RequestParam("file0") MultipartFile multipartFile){

​	if(!multipartFile.isEmpty()){

​		String fileStr = "绝对路径" + multipartFile.getOriginalFilename();// 文件新家地址

​		File file = new File(fileStr);// 新建文件

​		multipartFile.transferTo(file);// 搬家，推荐抛出异常（方便）

​	}

}





**（**3）主文件配置



spring.servlet.multipart.max-request-size=1024MB

spring.servlet.multipart.max-file-size=1024MB

spring.servlet.multipart.enabled=true



==================



# 上传-前端操作





## （一）HTML上传



<form action="/fileUpload" method="post” enctype="multipart/form-data">

​	<input type="file" name="file0” />

​	<button type="submit” > 上传 </button>

</form>







## （二）Axios+Vue上传

- IDEA中可以通过拖入js文件导入js到HTML文件
- 先导入vue和axios的js文件



**（**1）View部分



<div id="app">

​	<input type="file" id="file0" />

​	<button @click="autoUpdate">上传</button>

</div>





**（**2）JS部分



var vm = new Vue({



​	el: '#app',

​	methods:{

​	

​		fileUpload() {

​			var formData = new FormData()

​			// var file = file0.files[0]

​			var file = document.getElementById("file0").files[0]

​			formData.append("file0”,file)

​			axios.request({

​				url: '/fileUpload’,

​				method: 'post’,

​				data: formData,

​				headers: {

​					'Content-Type’: 'multipart/form-data’ // 同Postman一样的操作

​				}

​			})

​		}

​	

​	}



})







## （三）ElementUI

- 前后端分离需要跨域



**test.vue**文件中：



template

​	div

​		<el-upload action="文件上传接口地址” name="file”>

​			<el-button size="small” type="primary”>上传</el-button>

​		</el-upload>





script

​	export default {



​	}







**router/index.js**文件中：

,{

​	path: '/DemoPage/test',

​	name: 'TestPage',

​	component: () => import('@/views/DemoPage/test'),

​	meta: {

​		title: 'test',

​		icon: 'el-icon-s-custom'

​	}

}







===========



# 文件下载



===========

##  

## 后端控制层：



  @RequestMapping("/fileDownload")

  public void fileDownload(HttpServletResponse response) throws IOException {

​    String filePath="F:/Workspace/FileUpload/员工信息导入表.xlsx";

​    File file = org.springframework.util.ResourceUtils.getFile(filePath);

​    if(file.exists()){ //测试此抽象路径名表示的文件或目录是否存在。

​      // 配置文件下载

​      response.setHeader("content-type", "application/octet-stream");

​      response.setContentType("application/octet-stream");

​      // 下载文件能正常显示中文

​      response.setHeader("Content-Disposition", "attachment;filename=" + URLEncoder.encode("员工信息导入表.xlsx", "UTF-8"));

​      byte[] buffer = new byte[1024];//设置传输字节数组



​      //设置文件输入流和输入缓冲流

​      FileInputStream fis = new FileInputStream(file);

​      BufferedInputStream bis = new BufferedInputStream(fis);

​      //获取输出流对象

​      OutputStream outputStream = response.getOutputStream();

​      int i = bis.read(buffer);

​      while (i != -1) {

​        outputStream.write(buffer);

​        i = bis.read(buffer);

​      }

​      bis.close();

​      fis.close();

​      outputStream.close();

​      System.out.print("下载完成");

​    }

  }





## 前端：

- dom中添加：



  <h3>文件下载</h3>

  <button type="button" @click="fileDownload">文件下载</button>





- vue的methods中添加：



​      fileDownload() {

​        window.location.href="/fileDownload?可带参数区分下载";

​      }

# 19 Lombok



优缺点： https://blog.csdn.net/qq_37134175/article/details/99618957





- 添加依赖

- - Lombok：一个Java类库，提供注解，用来消除大量样板代码。仅五个字符（@Data）在model层使用
  - Spring Web 
  - MyBatis Framework
  - MySQL Driver

![Screen Shot 2020-09-13 at 13.49.52.png](/blob:file:/8683cee2-efd1-4762-b2e4-54fcb0e9b325)





# 21 kaptcha



参考

https://www.cnblogs.com/l024/p/9815152.html



gitee，参考：

https://gitee.com/baomidou/kaptcha-spring-boot-starter





# 22 自定义注解



元注解参考： https://blog.csdn.net/sw5131899/article/details/54947192



# 0 参考



System.gc()原理：https://blog.csdn.net/huangdeijia/article/details/89403936