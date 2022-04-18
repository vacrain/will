# 0 spring 说明



ioc详解： https://www.jianshu.com/p/17b66e6390fd

- IoC 在 Spring 里，只需要低级容器就可以实现，2 个步骤：

- - a. 加载配置文件，解析成 BeanDefinition 放在 Map 里。
  - b. 调用 getBean 的时候，从 BeanDefinition 所属的 Map 里，拿出 Class 对象进行实例化，同时，如果有依赖关系，将递归调用 getBean 方法 —— 完成依赖注入。



**spring模块体系：**

[**https://www.cnblogs.com/kirito-c/p/9198297.html**](https://www.cnblogs.com/kirito-c/p/9198297.html)



**spring-core 和 spring-beans**

spring-core 和 spring-beans 是 Spring 的基石，提供了基本的 DI （依赖注入）功能。

但是我们基本**不需要添加这两个依赖**，因为我们通常都会使用更上层的模块，而这些上层模块依赖了它们，我们引入上层模块后，依赖管理工具会自动链入下层依赖。



# 0 Spring



**参考：**https://blog.csdn.net/madman_donghui?t=1







# 1 Ioc和AOP



**Ioc**和DI参考：https://blog.csdn.net/madman_donghui/article/details/79240820





# 2 容器



参考：https://blog.csdn.net/madman_donghui/article/details/79244776



**BeanFactory**容器：https://blog.csdn.net/madman_donghui/article/details/79245079





# 3 应用上下文ApplicationContext



**参考：**https://blog.csdn.net/madman_donghui/article/details/79247003



- **ApplicationContext**：应用上下文
- 由BeanFactory派生而来：

![20180203151946226.jpeg](/blob:file:/24d6b545-95a8-496e-aeec-31520df061d6)

- 该接口主要有两个实现类：

- 1. ClassPathXmlApplicationContext：默认从类路径加载配置文件
  2. FileSystemXmlApplicationContext：默认从文件系统中加载配置文件

- 两个类的实例：



  public static void main(String[] args) {

​		// FileSystemXmlApplicationContext实例

​		// ApplicationContext content = new FileSystemXmlApplicationContext("//Users/Documents/applicationContext.xml");

​		// ClassPathXmlApplicationContext实例

​		ApplicationContext content = new ClassPathXmlApplicationContext("applicationContext.xml");

​    People peo = (People) content.getBean("peo");

​    System.out.println(peo);

  }



- 值得注意的是，FileSystemXmlApplicationContext的构造传参如果是字符串并且第一个字符是“/”的话，spring会自动去掉这个“/”，所以必要的时候，需要多谢个“/”，就像上面的例子。



**ApplicationContext**相对于BeanFactory多实现这些接口：

- ApplicationEventPublisher：使容器拥有了事件的功能，包括容器启动事件、关闭事件等。
- MessageSource：为应用提供i18n国际化消息访问的功能。
- ResourcePatternResolver：这个接口让容器可以通过带前缀的ant风格的资源文件路径装载spring的配置文件，其实就是放弃了spring的Resource类，并直接在ApplicationContext构造函数传参带通配符的路径字符串。
- LifeCycle：该接口提供了start（）和stop（）两个方法，主要用于控制异步处理。 
- 这些接口，是BeanFactory没有，而ApplicationContext特有的，也就意味着ApplicationContext要比BeanFactory多出这些功能。
- 所以我们经常这么来描述BeanFactory和ApplicationContext的关系：BeanFactory面向的是程序底层，ApplicationContext面向的应用功能。

# 6 注解



@Configuration 和 @Bean ：https://blog.csdn.net/u014199143/article/details/80692685



简单使用：



@Configuration

public class AppConf {



​	// LoadBalanced是负载均衡配置

  @Bean

  @LoadBalanced

  public RestTemplate restTemplate(){

​    return new RestTemplate();

  }



}



通过@Autowired即可注入RestTemplate类对象





**7 主动获取spring容器工具类SpringContextUtil**



https://blog.csdn.net/flyingzip/article/details/51659572?utm_source=blogxgwz5



# 8 ⭐️SSM项目设计、开发说明

20200905



参考如下，还有参考实际项目SSM01：









⭐️说明（解释理论）：

- 本说明假定读者已经掌握后端和数据库的基本理论、基本设计与运用常识及相关软件的安装、配置及基础操作

- - 后端泛指：Java基础（JavaSE）、Java技术原理及SSM框架原理（JavaEE）等
  - 后端特指：JDK、JRE、Maven、Tomcat、Eclipse、Spring Tool Suite等的安装及基础使用
  - 数据库泛指：数据库基本理论、基础操作及MySQL基础理论知识
  - 数据库特指：MySQL、Navicat的安装及基础使用

- 所以根据上述说明，下文将从一个创建及配置好的SSM项目开始介绍其设计及开发步骤。

- 本说明创建当天留：本说明是在只有一次简易完整SSM项目实践经验下写出来的，并不足够专业，只可作入门参考学习！





⭐️注意（解释操作）：

- 为保证项目的配置一致，这里以《**15 -1**⭐️**SSM**项目 配置、起步说明》为项目的创建及配置标准，进而进行下一步的设计及开发说明







## （一）Bean的设计与实现

- Bean、POJO、Entity都为实体类包，与数据库中表结构映射

- 本说明以com.demo.bean包为例说明

- 实现前将数据库中表结构打开，以便参考，具体操作：

- - 在需要映射的数据表上点右键，随后点【设计表】即可



**（**1）基本映射实现



# 9 Autowired和Source区别



参考：https://blog.csdn.net/weixin_40423597/article/details/80643990





|      | @Autowired | @Source |
| ---- | ---------- | ------- |
| 属于 | Spring     | Java    |





# 4 主配置文件说明





**Spring Boot application.yml application.properties 优先级：**

[**https://blog.csdn.net/testcs_dn/article/details/79010798**](https://blog.csdn.net/testcs_dn/article/details/79010798)

- 如果你的项目中存在 application.properties 文件，那么 application.yml 文件就只是一个摆设。



**application.properties 文件和 application.yml 文件有什么区别呢？：**[**https://blog.csdn.net/testcs_dn/article/details/78959700**](https://blog.csdn.net/testcs_dn/article/details/78959700)

- yml文件的好处，天然的树状结构，一目了然，实质上跟properties是差不多的。



## yml的使用：

- 官方给的很多demo，都是用yml文件配置的。



**注意点：**

1，原有的key，例如[spring](http://lib.csdn.net/base/javaee).jpa.properties.[hibernate](http://lib.csdn.net/base/javaee).dialect，按“.”分割，都变成树状的配置

2，key后面的冒号，后面一定要跟一个空格

3，把原有的application.properties删掉。然后一定要执行一下  maven -X clean install



**示例：**

**#application.yml**



server:

 port: 8086

 

spring:

  datasource:

​    name: test

​    url: jdbc:mysql://192.168.1.112:3306/test

​    username: root

​    password: xxx

​    \# 使用druid数据源

​    type: com.alibaba.druid.pool.DruidDataSource

​    driver-class-name: com.mysql.jdbc.Driver

​    filters: stat

​    maxActive: 20

​    initialSize: 1

​    maxWait: 60000

​    minIdle: 1

​    timeBetweenEvictionRunsMillis: 60000

​    minEvictableIdleTimeMillis: 300000

​    validationQuery: select 'x'

​    testWhileIdle: true

​    testOnBorrow: false

​    testOnReturn: false

​    poolPreparedStatements: true

​    maxOpenPreparedStatements: 20





**对比**#application.properties



server.port=8085



spring.datasource.type=org.apache.tomcat.jdbc.pool.DataSource

spring.datasource.url=jdbc:mysql://aliyuncs.com:3306/home?useUnicode=true&zeroDateTimeBehavior=convertToNull&autoReconnect=true

spring.datasource.username=root

spring.datasource.password=***

spring.datasource.driver-class-name=com.mysql.jdbc.Driver



\#mybatis.mapper-locations=classpath*:com/wanyu/fams/mapping/*Mapper.xml

\#mybatis.type-aliases-package=com.wanyu.fams.model



spring.mvc.view.prefix=/WEB-INF/jsp/

spring.mvc.view.suffix=.jsp



spring.druid.datasource.type=com.alibaba.druid.pool.DruidDataSource

spring.druid.datasource.driverClassName=com.mysql.jdbc.Driver

spring.druid.datasource.url=jdbc:mysql://localhost:3306/spring_boot?characterEncoding=utf-8

spring.druid.datasource.username=root

spring.druid.datasource.password=xxx





# 20 SpringBoot DevTools



**SpringBoot DevTools 的用途是什么？参考：**

[**https://www.cnblogs.com/programb/p/12430638.html**](https://www.cnblogs.com/programb/p/12430638.html)



- *spring-boot-devtools* 模块在生产环境中是默认禁用的，archives 的 repackage 在这个模块中默认也被排除。因此，它不会给我们的生产环境带来任何开销。
- 通常来说，DevTools 应用属性适合于开发环境。这些属性禁用模板缓存，启用 web 组的调试日志记录等等。最后，我们可以在不设置任何属性的情况下进行合理的开发环境配置。
- 每当 classpath 上的文件发生更改时，使用 DevTools 的应用程序都会重新启动。这在开发中非常有用，因为它可以为修改提供快速的反馈。
- 默认情况下，像视图模板这样的静态资源修改后是不会被重启的。相反，资源的更改会触发浏览器刷新。注意，只有在浏览器中安装了 LiveReload 扩展并以与 DevTools 所包含的嵌入式 LiveReload 服务器交互时，才会发生。



使用，参考：https://www.cnblogs.com/songxingzhu/p/9635264.html



# 0 Spring MVC原理



参考： https://www.cnblogs.com/fengquan-blog/p/11161084.html





SpringMVC的工作原理图：

# 6 Spring MVC

20200825

- 文件说明：

src/main/java				Java后台源文件

src/main/resources		配置文件、前台页面

src/test/java				Java测试源文件

pom.xml					maven配置文件



- SSM = Spring框架 + SpringMVC框架 + Mybatis框架



| 分层     | View | Controller | Service    | DAO        | EIS        |
| -------- | ---- | ---------- | ---------- | ---------- | ---------- |
| 语言     |      | Java       | Java       | Java       | Mysql(SQL) |
| 技术     | JSP  | Servlet    | Java       | JDBC       | Mysql(SQL) |
| 具体框架 |      | SpringMVC  | Java       | Mybatis    | Mysql(SQL) |
| 整体框架 |      | Spring     | Spring     | Spring     |            |
| 框架配置 |      | SpringBoot | SpringBoot | SpringBoot |            |



​			

\########################################################################



## (一)SpringMVC框架(编写控制器的步骤)

- Spring MVC属于 Spring

- Spring MVC出现后，Struts2占有率直线下降

- - Struts2是基于转发和重定向的，搭配JSP使用最好

- 概念：SpringMVC是基于【MVC原理】的【web层】框架

- 理解：Mybatis框架是JDBC技术的封装。SpringMVC框架是Servlet技术的封装。



**com.zhaoyang.controller.Action01**：



@Controller		控制器的注解

@RequestMapping(“映射别名”)		请求映射的注解





**登陆案例：**

​	访问路径：

localhost:8080/user/login



登陆页面				用户控制器					成功页面

login.html				UserAction.java				main.html



## (二)控制器获取前台数据的方式



**方式一：通常参数少，常见** 删除 、查询 操作

- 在控制器的方法中写入和前台数据个数、名字、类型相同的参数。

​	例子：

public String login(String username , String password){ }



**方式二：通常参数多，常见** 添加、修改 操作

- 在控制器的方法中写入封装类，如：com.wyh.bean.User
- 封装类中的变量必须和前台数据个数、名字、类型相同的参数。

​	例子：

public String login(User user){

​	user.getUsername();

​	user.getPassword();

}



方式三：通用

通过Map集合来获取数据。使用@RequestParam注解。动态获取数据。

​	例子：

public String login(@RequestParam Map<String,Object> map ){

​	map.get(“username”);

​	map.get(“password”);

}





## (三)	控制器响应前台数据的方式

- 控制器响应前台的方式有两大类



**第一种：跳转页面、把页面发送给前台、此种方式是**SpringMVC框架默认的方式

​	例子：

public String login ( String username,String password){

​	String path = “”;



​	return “redirect:” + path;

}



**第二种：把**Java对象转换为JSON数据、然后把JSON数据直接发给前台



方式一：**方法上方添加**@ResponseBody注解

@ResponseBody

public String login ( ){ }



方式二：**类上方添加**@RestController注解(所有方法全都返回JSON数据)

- @RestController = @Controller + @ResponseBody

@RestController

public class UserAction { }



## SpringMVC框架返回数据的方式有4种:

- 理解：Java对象转换为JSON数据格式的4种



(1)文本字符串

return “123”;



(2)对象

return user;



(3)List

return list;



(4)Map

return map; 





# 5 Mybatis框架

20200824



[Mybatis多个参数传值方法](https://www.cnblogs.com/leirenyuan/p/6043289.html)



- 说明：

- - **Spring** **Boot**：简化新Spring应用的初始搭建以及开发过程。(资源管理、配置管理、约定大于配置)

  - **Spring** ：不是哪一层的框架，由7部分组成，核心Spring Core（IOC）

  - - Spring框架是一个开放源代码的J2EE应用程序框架。
    - Spring通过一种称作控制反转（IoC）的技术促进了松耦合。

  - **Mybatis框架**：

  - - 概念:Mybatis框架是基于【ORM原理】（对象关系映射）的【持久层】框架。
    - 前身ibatis，后被谷歌托管，更名Mybatis，最后托管在GitHub上
    - 说明:Mybatis框架底层是对JDBC技术的封装。是一款优秀的持久层框架，好处在映射的便利

- 实现步骤：

- - 配置主配置文件：application.properties
  - 实体类：com.wyh.bean.Person
  - DAO层接口：com.wyh.dao.PersonDAO
  - 实现DAO层接口：通过Mapper.xml映射文件实现（可以理解为DAO层接口的实现类）
  - 业务层：通过注入的DAO层对象，调用DAO层的方法



\################################################



## （一）主配置文件配置 及 实体类实现：

##  

**（**1）主配置文件 配置环境（application.properties）

- 右键该文件，属性（最后一行），改编码方式（最后一行），改成UTF-8。
- 该文件注释方式，在开头加#
- 说明：实体类别名，作为地址前缀，例子：PersonMapper.xml文件夹中不需要写com.wyh.bean.Person，可以直接写Person



**1.**配置数据库连接参数

\#配置数据库连接参数

spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
 spring.datasource.url=jdbc:mysql://127.0.0.1:3306/db0820?useUnicode=true&characterEncoding=UTF-8&serverTimezone=UTC
 spring.datasource.username=root
 spring.datasource.password=root



**2.**配置Mybatis映射文件和实体类的包

\#配置mybatis映射文件路径(mapper/*.xml)、实体类路径别名（com.wyh.bean)

mybatis.mapper-locations = classpath:mapper/*.xml

mybatis.type-aliases-package = com.wyh.bean





**（**2）实体类实现（com.wyh.bean.Person）

- 建包：com.wyh.bean
- 包中建实体类：Person.java
- 根据数据库映射的表及表联系，实现该类





## （二）DAO层使用Mybatis框架

**（**1）根据业务层需求，设计DAO层接口

- com.wyh.dao.PersonDAO



**（**2）实现DAO层接口，通过mapper/PersonMapper.xml



**1**、创建SQL映射文件

- 在src/main/resource中新建文件夹中 建一个mapper文件夹
- SQLMapper.xml文件 粘贴到 mapper文件夹中，并改名为mapper/PersonMapper.xml





**2**、实现DAO层功能

- 注释方式：<!- -注释 - ->

- 因为insert、update、delete三个方法返回的数据都是int型（0或1），所以这三种SQL标签都不需要定义resultType（返回值类型）

- int 代表 integer、_int 代表 int，不过JKD自带自动装箱拆箱，写哪个都可以

- 标签属性说明：

- - id：接口的方法名
  - parameterType：参数类型
  - resultType：返回内容的数据类型



**实现的接口路径**:

<mapper namespace = “com.wyh.dao.PersonDao”>



**实现增删改查功能：**



 <insert id=”insert” parameterType=”Person”>

​	Insert into person(name,money,bir) values(#{name},#{money},${bir})

</insert>



<update id = “update” parameterType=”Person”>

​	update person set name = #{name},money = #{money},bir = #{bir} where id = #{id}

</update>



<delete id = “update” parameterType=”int”>

​	Delete from person where id = #{id}

</delete>



<select id=”getOne” parameterType=”int” resultType=”Person”>

​	Select * from person where id = #{id}

</select>



<select id=”getList” parameterType=”string” resultType=”Person”>

​	Select * from person where name like concat('%',#{name,jdbcType=VARCHAR},'%')

</select>





## （三）业务层调用DAO层

1. 业务层com.wyh.service.PersonService接口，方法对应dao层写

2. 业务层com.wyh.service.PersonServiceImpl实现类

3. - 添加注解@service
   - 注入Dao层对象：Person DAO dao;

- 封装好处：隐藏细节，可以只关注当前层的内容，不用关心别的层怎么实现的



## （四）通过Junit测试

**（**1）pom.xml加入依赖：

<dependency> 
 <groupId>junit</groupId> 
 <artifactId>junit</artifactId>
 <scope>test</scope>
 </dependency>



**（**2）加注释，测试类中，类上方加入注解：

@RunWith(SpringRunner.class)

@MappperScan(“com.wyh.dao”)



**（**3）改包：

将import org.junit.jupiter.api.Test;改成：

import org.junit.Test;



**（**4）公开类、公开方法：

类定义处 前 加public

方法 前 加public



**（**5）注入业务层对象：

PersonService service;



**（**6）测试添加：

int i = service.add(new Person(“abc”,12.34,”2020-11-22”));



## （五）补充



**（**1）Mybatis实现分页功能

- 使用pagehelper实现分页功能（pagehelper插件）



**1.Pom.xml**文件中加入依赖，并更新maven

        <dependency>              <groupId>com.github.pagehelper</groupId>              <artifactId>pagehelper</artifactId>              <version>5.0.0</version>          </dependency>          <dependency>              <groupId>com.github.pagehelper</groupId>              <artifactId>pagehelper-spring-boot-autoconfigure</artifactId>              <version>1.2.3</version>          </dependency>          <dependency>              <groupId>com.github.pagehelper</groupId>              <artifactId>pagehelper-spring-boot-starter</artifactId>              <version>1.2.3</version>          </dependency>



**2.**分页在业务层使用，搜索的实现方法中使用分页插件即可：

public List<Person> search(name,page,size){

​	**PageHelper.starPage(page,size);**

​	return dao.getListByName(name);

}



**（**2）Mybatis传递多参写法：

- DAO层接口中，方法参数加注解：@Param(“随便写”)通常和参数名相同

- - 如：delete(@Param(“id”) int id);
  - 

**PersomMapper.xml**文件中多参数的写法：

​	第一种方式：

<search id=”search” resultType=”Person”>

​	Select * from where name like concat(‘%’,#{p1},’%’) and money between #{p2} and #{p3}

</search>



​	第二种方式：

- 通过map来实现传递多个参数，DAO层的方法传递map集合

- - 如：List<Person> search (Map<String,Object> map);

<search id=”search” resultType=”Person”>

​	Select * from where name like concat(‘%’,#{key1},’%’) and money between #{key2} and #{key3}

</search>





**（**3）Mybatis多表查询



**1.**先准备好数据

- 建新的数据表 在数据库中
- 在 bean 中加入新的类映射数据库的数据表 

- 如果有关联的话，在 1对n的关系中 
- 在n的对应的类中要加入 1的对应的类的对象集合
- 在1的对应的类中要加入n的对应的类的对象 



**2.DAO**层（包括接口和Mapper.xml文件）

- 如 ：ComDAO接口，定义添加用户方法；EmpDAO接口，定义查询一个员工对象的方法
- Mapper文件夹中，新建EmpMapper.xml配置映射文件：用右连接，因为员工多，为基础

​	<select id=”getOne” parameterType=”int”>

​		Select c.id cid , c.name cname, e.id eid ,e.name ename,e.age age 

​		from com c right join emp e on c.id = e.comid 

​		where e.id =#{id}

​	</select> 

- Select 后必须起别名
- 注意：多表查询必须要配置 映射关系，SQL查询语句和类之间的映射 关系



**该映射文件加入：**

- <resultMap id ：resultMap的id随便起，不重复即可，表示映射关系名
- <id />：主键映射关系
- <result />：除主键外的映射关系
- type：返回类型
- property：返回类型的成员变量
- column：查询出来的，表中的列名

<resultMap id=”map01” type=”Emp”>

​	<id property=”id” column=”eid”/>

​	<result property=”name” column=”e.name”>

​	<result property=”age” column=”age”>//名字相同可以省

​	<result property=”com.id” column=”cid”>

​	<result property=”com.name” column=”cname”>

</resultMap>



**之后再**<select></select>标签加入属性：resultMap=”map01”



**之后**test类中测试即可



**3.**映射关系中，含有集合的情况：

- 新建Com类的映射文：ComMapper.xml

- - Namespace = “com.wyh.dao.ComDAO”



<result id=”map02” type=”Com”>

​	<id property=”id” column=”cid”>

​	<result property=”name” column=”cname”>

​	<collection property=”list” resultMap=**”map03”**></collection>

</result>



<result **id=”map03”** type=”Emp”>

​	<id property=”id” column=”eid” />

​	<result property=”name” column=”ename”/>

​	<result property=”age” column=”age”>

</result>



- 业务中几乎不用，效率低，项目中多见多对一的需求，只需取出一，不需要取出列表
- 测试：取出公司对象 ，输出公司信息，并遍历员工集合



# 5-1 一对多查询





 <select id="getAllData" resultMap="BaseResultMap">

  select t_department.*,

​    tp.id as pid,tp.name as pname,tp.departmentid,

​    te.id as eid,te.name as ename,te.positionid

  from

​    t_department left join t_position tp

​      on t_department.id = tp.departmentid

​    left join t_employee te on tp.id = te.positionid

 </select>







<resultMap id="BaseResultMap" type="com.sunrise.springboot10.model.TDepartment">

  <id column="id" jdbcType="INTEGER" property="id" />

  <result column="name" jdbcType="VARCHAR" property="name" />

​    

​    

  <collection property="positionList" ofType="com.sunrise.springboot10.model.TPosition" column="id">

   <id column="pId" jdbcType="INTEGER" property="id" />

   <result column="pName" jdbcType="VARCHAR" property="name" />

   <result column="salary" jdbcType="DOUBLE" property="salary" />

   <result column="departmentid" jdbcType="INTEGER" property="departmentid" />

​     

   <collection property="employeeList" ofType="com.sunrise.springboot10.model.TEmployee" column="employeeId" javaType="java.util.List">

​     

​     <id column="eId" jdbcType="INTEGER" property="id" />

​    <result column="eName" jdbcType="VARCHAR" property="name" />

​    <result column="sex" jdbcType="VARCHAR" property="sex" />

​    <result column="photo" jdbcType="VARCHAR" property="photo" />

​    <result column="birthday" jdbcType="DATE" property="birthday" />

​    <result column="school" jdbcType="VARCHAR" property="school" />

​    <result column="other" jdbcType="VARCHAR" property="other" />

​    <result column="positionid" jdbcType="INTEGER" property="positionid" />

​      

   </collection>

​     

  </collection>

 </resultMap>





# 5-2 多对一/一对一查询





 <association property="position" javaType="com.wyh.ssm21.bean.Position">



  <id column="pid" jdbcType="INTEGER" property="id" />

  <result column="pname" jdbcType="VARCHAR" property="name" />

  <result column="salary" jdbcType="DOUBLE" property="salary" />

  <result column="departmentid" jdbcType="INTEGER" property="departmentid" />



 </association>





# 3 消息队列





作者：Java3y
 链接：https://www.zhihu.com/question/54152397/answer/657234090



# 5 微服务

# Spring Cloud、Nacos



详解

 https://mp.weixin.qq.com/s/g0br3PfTmm8C_nkKbzE_ig

https://zhuanlan.zhihu.com/p/95696180?from_voters_page=true







参考图：

![springcloud.png](/blob:file:/e29fc53f-d16b-4db9-92af-d255c00bab52)

![微服务框架.jpg](/blob:file:/198e4bb9-f492-4804-84b7-fe31d57d5b94)

**说明：**

- 一个服务为一个模块，一个模块至少是一个SpringBoot工程
- 注册中心：服务启动之后，注册到注册中心，服务中心负责管理这些服务，服务之间还可以互相调用
- 配置中心：所有配置写到这里，包括数据库连接，端口号等，阿里的Nacos把注册中心和配置中心做成了一个应用，可以在nacos中注册服务，从而实现微服务之间的互相配合
- 监控中心：查看运行状态





## Nacos注册中心的简单使用说明

- 安装后，在终端中进入nacos的bin文件夹，通过startup. cmd命令启动nacos服务器

- - 需要配好CLASS_PATH环境变量，存JDK的HOME文件夹的地址
  - 启动后的服务器注册首页地址为：[http://ip地址:端口号(8848)/nacos/index.html](http://xn--ip:(8848)-ij8o2gp08a7fx230c/nacos/index.html)
  - 注册服务需要帐号密码，由nacos服务器提供
  - 通过spring.application.name设置服务名，同名的服务将采用轮询方式访问

- 在非Nacos服务器的主机上实现微服务



**实现微服务步骤：**

1. 新建SpringBoot工程，在新建最后一步

2. 1. SpringBoot版本改成：2.2.10
   2. 依赖选Alibaba->**Nacos Service Discovery** 还有Spring Web

3. 在启动类上加注解，意为服务注册中心客户端：@EnableDiscoveryClient

4. 主配置文件中配置：

5. 1. server.port=8088
   2. spring.application.name=app-007 #服务名
   3. spring.cloud.nacos.discovery.server-addr=ip地址:8848 #注册中心地址

6. 新建一个控制层的类

7. 1. 类添加注解：@RestController

   2. 写一个方法

   3. 1. 添加注解：@RequestMapping("a01")
      2. 随便返回一个字符串

8. 新建类：config.AppConf

9. 1. 类添加注解：@Configuration

   2. 写一个方法：public RestTemplate restTemplate()

   3. 1. 添加注解：@Bean、@loadBalanced
      2. 方法体：return new RestTemplate();

10. 再写一个控制层的类

11. 1. 类添加注解：@RestController

    2. 注入对象：private RestTemplate restTemplate;

    3. 写一个方法：public String get()

    4. 1. 添加注解：@RequestMapping("a")
       2. 方法体，返回的参数为其他服务提供的方法，和方法返回的数据类型的类：return restTemplate.getForObject("http://app-09/a01",String.class);

12. 验证服务方式：访问http://localhost:8848/a



![Screen Shot 2020-10-17 at 06.53.59.png](/blob:file:/c94d6327-169c-4013-ac72-a1a705ae0a59)











## Nacos的配置中心简单实用说明

- **配置是写在nacos服务器中的**
- **工程是可以通过服务器下载配置**



**（**1）在Nacos服务器中（即nacos主页）新建配置，如下图：

- 该配置存在nacos服务所在主机

![Screen Shot 2020-10-17 at 06.57.06.png](/blob:file:/43fcd742-317f-403e-b599-e27b4e597eec)

![Screen Shot 2020-10-10 at 09.00.48.png](/blob:file:/ae422bcf-f3ea-461e-a25e-bdd4a5bba113)

![Screen Shot 2020-10-10 at 09.03.49.png](/blob:file:/d7a4eb00-b367-44aa-a6b5-73192b99d58f)



**（**2）新建服务

- Nacos+MyBatis+MySQL
- 新建工程添加依赖：Spring Web、Mybatis Framework、MySQL Driver、**Nacos Configuration**



**（**3）服务配置

- 主配置文件中进行配置



\# 本机工程端口

server.port=8082

\# nacos服务器中的配置名

spring.application.name=springboot

\# nacos服务器

spring.cloud.nacos.config.server-addr=【nacos服务器ip】:8848

spring.cloud.nacos.discovery.server-addr=【nacos服务器ip】:8848



**（**4）新建数据库

- 按照约定好的名字（springboot），在各个服务的主机建好数据库即可





**（**4）启动类配置

- 添加注解：



@NacosConfigurationProperties(dataId = "springboot")