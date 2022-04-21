# 0 博客收藏



全栈：https://www.jianshu.com/u/c4503bc2c490



加密： https://www.cnblogs.com/loong-hon/tag/Java/





# 1 Java说明



- **Java是一门面向对象编程语言，不仅吸收了C++语言的各种优点，还摒弃了C++里难以理解的多继承、指针等概念，因此Java语言具有功能强大和简单易用两个特征。Java语言作为静态面向对象编程语言的代表，极好地实现了面向对象理论，允许程序员以优雅的思维方式进行复杂的编程。**
- **Java具有简单性、面向对象、分布式、健壮性、安全性、平台独立与可移植性、多线程、动态性等特点。Java可以编写桌面应用程序、Web应用程序、分布式系统和嵌入式系统应用程序等。**



## （01）Java环境配置

- JDK：Java软件开发工具包。用来开发Java程序。
- JRE：Java运行时环境。运行Java程序用的。
- Eclipse：Java开发工具之一。开发Java程序用的。



- **JDK是 Java 语言的软件开发工具包，主要用于移动设备、嵌入式设备上的java应用程序。JDK是整个java开发的核心，它包含了JAVA的运行环境（JVM+Java系统类库）和JAVA工具。**
- **JVM是Java Virtual Machine（Java虚拟机）的缩写，JVM是一种用于计算设备的规范，它是一个虚构出来的计算机，是通过在实际的计算机上仿真模拟各种计算机功能来实现的。引入Java语言虚拟机后，Java语言在不同平台上运行时不需要重新编译。Java语言使用Java虚拟机屏蔽了与具体平台相关的信息，使得Java语言编译程序只需生成在Java虚拟机上运行的目标代码（字节码），就可以在多种平台上不加修改地运行。**



## （02）Java版本平台的分类

- JavaSE：Java标准版。

- - 定位：桌面应用程序。即JDK，本质就是Java语言本身。也是其他2个平台基础。

- JavaEE：Java企业版

- - 定位：企业级的应用。凸显Java优势

- JavaME：Java缩微版。

- - 定位：移动电子产品
  - 说明：前端主流：JavaScript、TypeScript



## （03）Java开发路线

1. 第一阶段：Java语言（JavaSE）
2. 第二阶段：Java技术（JavaEE）
3. 第三阶段：Java框架（SpringBoot、SSM）
4. 第四阶段：Java项目



## （04）Java语言大纲

- 第一部分：Java 基础语法部分（逻辑能力）
- 第二部分：Java 面向对象部分（思想能力、最重要）
- 第三部分：Java API（动手能力）

**（**1）Java基础语法部分

1. 八种基本数据类型

2. 1. 整型：byte、short、int、long
   2. 浮点数：float、double
   3. 布尔：boolean
   4. 字符型：char

3. 运算符

4. 1. 基本运算符：+、-、*、/、%
   2. 比较运算符：>、>=、<、<=、==、!=
   3. 关系运算符：&&、||、!
   4. 赋值运算符：=、+=、-=、*=、/=、%=
   5. 自增自减运算符：++、- -
   6. 三目运算符：？：

5. 流程控制语句

6. 1. 分支语句：

   2. 1. if分支语句
      2. switch分支语句

   3. 循环语句：

   4. 1. for循环
      2. while循环
      3. do while循环

7. 数组

8. 1. 数组的创建
   2. 元素的存取
   3. 遍历数组

9. 方法

10. 1. 有无返回值：有返回值方法、无返回值方法
    2. 是否静态：静态方法、非静态方法
    3. 是否抽象（是否有方法体）：实现方法、抽象方法



**（**2）Java面向对象部分

- 概念（熟记）

- 1. 类的分类：

  2. 1. 具体类：被class修饰

     2. 抽象类：被abstract修饰

     3. - 抽象方法：被abstract修饰的方法

        - - 没有方法体

  3. 接口：被interface修饰

  4. 1. 接口成员变量：默认被public static final修饰
     2. 接口成员方法：默认被public abstract修饰

  5. 类的概念及具体内容：

  6. 1. 类：

     2. - 被class修饰的叫做类，作为图纸、模版

     3. 对象：

     4. - 通过构造方法创建出来的实例、实体、实物

     5. 成员变量

     6. - 类中定义的变量，表示属性、状态

     7. 成员方法

     8. - 类中定义的方法，表示功能、行为

     9. 构造方法

     10. - 方法名必须与类名 相同，没有返回值也没有void关键字
         - 用来创建对象、实体化

     11. 创建对象

     12. - 类名 变量 = new 类的构造方法
         - 父类 变量 = new 子类的构造方法
         - 接口 变量 = new 实现类的构造方法

     13. 数据类型分类

     14. - 基本数据类型
         - 类类型（引用类型）

     15. 值传递

     16. - 基本数据类型 存储和传递 的是真实的值
         - 类类型 存储和传递 的是地址的值

     17. 引用和实例的关系

     18. - 一个变量可以引用0或1个实例
         - 一个实例可以被多个变量引用

     19. 成员变量和局部变量的区别

     20. - 作用域不同：

         - - 成员变量，整个类内部都可以使用
           - 局部变量，当前方法的内部都可以使用

         - 初始值不同：

         - - 成员变量：整数默认0、浮点数默认0.0、布尔值默认false、类类型默认值是null
           - 局部变量：系统不自动赋值，必须手动赋值后才能用

     21. final关键字

     22. - 修饰变量 为常量
         - 修饰方法 为不可重写
         - 修饰类 为不可继承

     23. null关键字

     24. - 用于类类型中，表示“空”的意思，即谁也不引用

     25. static关键字

     26. - 有static修饰：在类中，属于类，为静态成员，通过“类.成员”的方式来调用，且静态成员可以被所有对象共用（不推荐）
         - 无static修饰：在对象中，属于对象，为非静态成员，通过“对象.成员”的方式来调用

     27. this关键字和super关键字

     28. - this表示当前类的对象
         - super表示父类的引用

     29. 可见性修饰符

     30. - private私有：本类 可见
         - 默认：本包+本类 可见
         - protect保护：本包+本类+子类 可见
         - public公共：都可见

     31. toString方法

     32. - 方便输出对象信息

     33. 包：

     34. - 在同一个包内的类之间可以互相访问
         - 在外包的类 必须导入才能使用

     35. 创建类的过程

- 思想（理解）

- 1. 封装
  2. 继承
  3. 多态



**（**3）Java API

- 常用API

- 1. 数学工具类

  2. - java.lang.Math

  3. 随机数类

  4. - java.util.Random

  5. 字符串类

  6. - java.lang.String
     - java.lang.StringBuffer

  7. 日期类

  8. - java.util.Date

  9. 日期转换类

  10. - java.text.SimpleDateFormat

  11. byte的类类型

  12. - java.lang.Byte

  13. short的类类型

  14. - java.lang.Short

  15. int的类类型

  16. - java.lang.Integer

  17. long的类类型

  18. - java.lang.Long

  19. float的类类型

  20. - java.lang.Float

  21. double的类类型

  22. - java.lang.Double

  23. boolean的类类型

  24. - java.lang.Boolean

  25. char的类类型

  26. - java.lang.Character

- 成体系API





# （05）Java提示及技巧（无规律排列）



## （1）option加？ 代码提示出现奇怪的符号的解决办法

1. preferences->General->Keys找到Content Assist
2. 设置快捷键为 option + /  即可



## （2）修改注释

**Preferences -> Java -> Code Style -> Code Templates ->Comments -> Types -> Edit**

- ${user} 改成自己的名字
- 点击Insert variable… 可以加入时间等信息





## （3）添加注释

- 方法一：输入/** 之后回车，可以添加注释
- 方法二：在创建类的时候勾选Generate comments即可生成



## （4）TODO关键字

**可以在**task窗口中看见任务都有哪些，双击直接跳转到对应的TODO处



## （5）工程的导入/导出

- 导出：复制出来工程即可

- 导入：

- 1. 右键->import->Existing Projects into Workspace
  2. 选好工程，并且勾选复制到工作空间



## （6）各个后端语言的区别



| 应用层     | Java语言、C#语言、PHP语言等(只专注于功能的实现、不专注于代码的运行原理、认证) |
| ---------- | ------------------------------------------------------------ |
| 操作系统层 | C++语言(内存结构、数据结构和算法)                            |
| 硬件层     | C语言(内存结构、数据结构和算法)                              |



## （7）Java工程说明

**src**文件夹 和 bin文件夹 的区别：

- src文件夹：存放Java文件
- bin文件夹：存放class文件
- 说明：程序员编写Java文件，Eclipse工具自动把Java文件编译为class字节码文件，存放到bin编译文件夹，真正运行的也是class文件



## （8）Java快捷键

**排版代码** ：

ctrl + shift + f

**输出：**

syso	alt +?

**主方法：**

main	alt + ？





## （9）Java代码调试步骤：

- 注意：异常应该先看自己的包、看第一个异常（第一个是真正出错的地方，后面的都是引起出错的地方）



**步骤一：加断点：双击圆点处。如果知道哪行出了问题就直接添加断点，如果不知道，就首行加**



**步骤二：**Debug模式运行：右键->debug as（调试模式）切换调试视图



**步骤三：跟踪代码，找出错误，三种方法：**

- - F5		进入方法内部跟踪



- - F6（常用）	当前代码块内部跟踪



- - F8		跳转到下一个断点 或 直接结束









## （10） Eclipse打不开，code = 13

- 删除：控制面板 》 程序 〉程序和功能 》Java n Update
- 之后再次安装Jdk即可



## （11）双版本jdk

- open ~/.bash_profile
- 粘贴下面代码



export JAVA_8_HOME="$(/usr/libexec/java_home -v 1.8)"

export JAVA_11_HOME="$(/usr/libexec/java_home -v 11)"

alias jdk8='export JAVA_HOME=$JAVA_8_HOME'

alias jdk11='export JAVA_HOME=$JAVA_11_HOME'

export JAVA_HOME=$JAVA_8_HOME



- source ~/.bash_profile
- 查看版本方式：



java11

java -version



java 8

java -version



## （12）多行注释快捷键

1. preferences->General->Keys找到comment   when in windows
2. 设置快捷键为 com + ` 即可

##  



## （13）导出文档

1. 工程上右键，选export
2. 选本地JDK目录下的，bin文件夹中的，Javadoc.class
3. 选导出目录后下一步，再下一步
4. 填写编码方式：-encoding UTF-8 -charset UTF-8 
5. 点击完成，即可生成文档，无视报错





## （14）各种类的简称

- 使用请参考：

- - https://www.toutiao.com/i6871088249989923335/?tt_from=weixin&utm_campaign=client_share&wxshare_count=1&timestamp=1600061721&app=news_article&utm_source=weixin&utm_medium=toutiao_android&use_new_style=1&req_id=202009141335200100110610880C85924B&group_id=6871088249989923335

-  **VO（View Object）：**视图对象，用于展示层，主要用于页面展示以及将页面的数据传送给控制器。

- **DO（Domain Object/Data Object）：**一种说法是Domain Object，领域对象，是对现实生活中的抽象对象，另一种说法是Data Object，也就是数据对象，他的内容和数据库表结构一致，个人比较赞成这种说法。

- **DTO（Data Transfer Object）：**数据传输对象，主要用于Service和Manager层向外传输的对象。

- **PO（Persistent Object）：**持久化对象，它和数据库表结构一致。

- **BO（Business Object）：**业务对象，可以由Service层输出的封装业务逻辑的对象。

- **POJO（Plain Ordinary Java Object）：**一般Java对象，DO、VO、DTO等的统称

- **Query：**数据查找对象，各层接收上层的查询对象。

- **Entity：**实体类，基本和数据库表结构一致

- **Domain：**与POJO一样，一种对象的统称





## （15）UUID

- UUID说明：Universally Unique Identifier全局唯一标识符，定义了一个字符串作为主键，采用32位数字组成，编码采用16进制，定义了时间和空间唯一的系统信息

- UUID编码规则：

- 1. 1～8位采用系统时间，精确到毫秒级保证时间的唯一性
  2. 9～16位采用底层的IP地址，保证在服务器集群中的唯一性
  3. 17～24位采用当前对象的HashCode值，在一个内部对象中的唯一性
  4. 25～32位采用调用方法生成一个随机数，在对象内的毫秒级的唯一性

- 通过以上4种策略可以保证唯一性。

- 在系统中需要用到随机数的地方都可以考虑采用UUID

- UUID所在包：java.util

- .Net中叫GUID







# 3 SOLID

参考：https://blog.csdn.net/u011118321/article/details/54632373



## 单一职责原则（SRP）

- 一个类有且只有一个职责



## 开放封闭原则（OCP）

- 对扩展开放，对修改关闭



## 里氏替换原则（LSP）

- 子类可以替换父类工作



## 接口隔离原则（ISP）

- 接口拥有尽可能少的行为，不依赖用不到的功能



## 依赖倒置原则（DIP）

- 高层模块不依赖底层模块，应该依赖抽象或接口





```
练习


0806练习

TODO 练习6


//
//(1)ABCDE=4*EDCBA;其中，A、B、C、D、E都是1-9中的数字。问这5个数字都是多少。 
//
System.out.println("第一题");
int i = 11111;
while(i<100000) {
	if(i==4*( i%10*10000 + i/10%10*1000 + i/100%10*100 + i/1000%10*10 + i/10000  )) {
		break;
	}
	i++;
}
System.out.println(i);
//(2)有一工人甲，工资是三位数ABC元（一个字母代表0-9中一个数字），
//组内其它五个工人的工资可以这样表示：ACB，BAC，BCA，CAB，CBA，且这五个工人的工资总额为3194元。
//请问工人甲的工资具体是多少。
//
System.out.println("第二题");
int salary = 100;
int a=0,b=a,c=a;

for(;salary<1000;salary++) {
	c = salary%10;
	b = salary/10%10;
	a = salary/100%10;
	if(a*100+a*10*2+a*2+b*100*2+b*10+b*2+c*100*2+c*10*2+c == 3194) {
		break;
	}
}
System.out.println(salary);
System.out.println(a*100+c*10+b);
System.out.println(b*100+a*10+c);
System.out.println(b*100+c*10+a);
System.out.println(c*100+a*10+b);
System.out.println(c*100+b*10+a);


//(3)所谓水仙花数是指一个三位数，其各位数字立方和等于该数本身，
//例如153是水仙花数，因为153=1*1*1+5*5*5+3*3*3.请编程求出所有的水仙花数？
//
System.out.println("第三题");
int uv = 100;
for(;uv<1000;uv++) {
	if( Math.pow((uv%10),3)+Math.pow((uv/10%10),3)+Math.pow((uv/100%10),3) == uv) {
		System.out.println(uv);
	}
}

//(4)一个数如果恰好等于它的因子之和，这个数就称为“完数”。例如6=1＋2＋3.编程
//找出10000以内的所有完数。
//
System.out.println("第四题");
double wjuu = 1;
for(;wjuu<10000;wjuu++) {

	double wjuus = 0;
	double wjuu1 = 1;

	//for(;wjuu1<=Math.sqrt(wjuu);wjuu1++) {
if(wjuu == 1) {
	System.out.println(wjuu);
}
for(;wjuu1<=wjuu/2;wjuu1++) {
	if( wjuu % wjuu1 == 0 ) {
		wjuus += wjuu1;
//					System.out.println("wjuu:"+wjuu);
//					System.out.println("wjuu1:"+wjuu1);
//					System.out.println("wjuus:"+wjuus);
		}
	}
	
	if(wjuus == wjuu) {
		System.out.println(wjuu);
	}
}


//(5) 剩下1000-1100人
//他命令士兵3人一排，结果多出2名；接着命令士兵5人一排，结果多出3名；
//他又命令士兵7人一排，结果又多出2名。韩信马上向将士们宣布：我军有1073名勇士，
//
System.out.println("第五题");
for (int j = 1000; j <= 1100; j++) {
	if(j%3==2 && j%5==3 && j%7==2) {
		System.out.println(j);
	}
}


//(6)有若干只鸡兔同在一个笼子里，从上面数，有35个头；从下面数，有94只脚。求笼中各有几只鸡和兔？
//请用程序计算出来鸡和兔各多少只？
System.out.println("第六题");
int tz = 1;
int ji = 35-tz;
for(;tz<35 ;tz++,ji--) {
	if( tz*4+ji*2==94 ) {
		System.out.println("兔子："+tz+"只");
	System.out.println("鸡："+ji+"只");
	}
} 



0807练习

	public static int arrn(int[] arr,int n) {
		if(n>=0 && n<arr.length)return arr[n];
		return -1;
	}
	
	public static int arr_max(int[] a) {
		int max = a[0];
		for (int i = 1; i < a.length; i++) {
			if(a[i]>max)max = a[i];
		}
		return max;
	}
	
	public static void arr_max_i(int[] a) {
		int max = a[0];
//		int max_i[] = new int[a.length];
//		int j = 0;
		
		for (int i = 1; i < a.length; i++) {
			
			if(a[i]>max) {
				max = a[i];
			}
			
		}
		
		for (int i = 0; i < a.length; i++) {
			if(a[i] == max) {
//				max_i[j++] = i;
				System.out.println(i);
			}
		}
		
//		int max_i1[] = new int[j];
		
//		for (int k = 0; k < max_i1.length; k++) {
//			max_i1[k] = max_i[k];
//		}

//		for (int i = 0; i < max_i1.length; i++) {
//			System.out.println(max_i1[i]);
//		}
		
//		return max_i1;
	}
	
	public static int arr_min(int[] a) {
		int min = a[0];
		for (int i = 1; i < a.length; i++) {
			if(a[i]<min)min = a[i];
		}
		return min;
	}
	
	public static void arr_avg(int[] a) {
		 double s = 0;
		 for (int i = 0; i < a.length; i++) {
			s+=a[i];
		}
		 System.out.println(s/a.length);
	}
	
	public static void change_maxmin(int[] a) {
		int maxi = 0;
		int mini = 0;
		int max = a[0];
		int min = a[0];
		for (int i = 1; i < a.length; i++) {
			if(a[i] > max) {
				max = a[i];
				maxi = i;
			}
			if(a[i] < min){
				min = a[i];
				mini = i;
			}
		}
		
		int t = 0;
		t = a[maxi];
		a[maxi] = a[mini];
		a[mini] = t;
		
		for (int i = 0; i < a.length; i++) {
			System.out.println(a[i]);
		}
	}
	
	public static boolean isvalue(int[] a , int b) {
		for (int i = 0; i < a.length; i++) {
			if (a[i] == b) {
				return true;
			}
		}
		return false;
	}
	
	public static boolean isvu(int[] a) {
		for (int i = 0; i < a.length; i++) {
			
			int f = 0 ;
			
			for (int j = 2; j <= Math.sqrt(a[i]) ; j++) {
				
				if(a[i]%j == 0) {
					f = 1;
					break;
				}
				
			}
			
			if(f == 1) {
				return true;
			}
			
		}
		
		return false;
	}
	

	public static int[] asc(int[] a) {
		int t = 0;
		for (int i = 0; i < a.length; i++) {
			for (int j = i; j < a.length; j++) {
				
				if(a[i] > a[j]) {
					t = a[i];
					a[i] = a[j];
					a[j] = t;
				}
			
			}
		}
		return a;
	}
	
	
	public static void arrs_jj(int[] a,int[] b) {
		
		for (int i = 0; i < a.length; i++) {
			for (int j = 0; j < b.length; j++) {
				if(a[i] == b[j]) {
					System.out.println(a[i]);
					break;
				}
			}
		}
		
	}
	
	public static void times(int[] a , int n) {
		int c = 0;
		for (int i = 0; i < a.length; i++) {
			if(a[i] == n) {
				c++;
			}
		}
		System.out.println(c);
		
		
	}

	
	public static boolean istwo(int[] a) {
		for (int i = 0; i < a.length; i++) {
			for (int j = a.length-1; j > i ; j--) {
				if(a[i] == a[j]) {
					return true;
				}
			}
		}
		return false;
	}
	
	public static void find_maxodd(int[] a) {
		int maxodd=0;
		int i = 0;
		for (; i < a.length; i++) {
			
			if (a[i]%2!=0) {
				continue;
			}
			maxodd = a[i];
			break;
		}
		if(i==a.length-1) {
			System.out.println(maxodd);
		}else {
			for (i++; i < a.length; i++) {
				if(a[i]%2==0 && a[i]>maxodd) {
					maxodd=a[i];
				}
			}
			System.out.println(maxodd);
		}
	}





	public static void rectangle() {
		for (int i = 0; i < 3; i++) {
			for (int j = 0; j < 5; j++) {
				System.out.print("*");
			}
			System.out.println();
		}
	}
	
	public static void triangle() {
		for (int i = 0; i < 4; i++) {
			for (int j = 0; j <= i; j++) {
				System.out.print("*");
			}
			System.out.println();
		}
	}
	

	public static void write(String a) {
		System.out.print(a);
	}
	public static void writen(String a) {
		System.out.println(a);
	}
	
	public static void untriangle() {
		for (int i = 0; i < 4; i++) {
			for (int j = 0; j < 4-i; j++) {
				write("*");
			}
			writen("");
		}
	}
	
	public static void dytriangle() {
		for (int i = 0; i < 3; i++) {
			
			for (int j = 0; j < 3-i-1; j++) {
				write(" ");
			}
			for (int j = 0; j < 2*i+1; j++) {
				write("*");
			}
			writen("");
			
		}
	}
	
	public static void jj() {
		
		for (int i = 1; i <= 9; i++) {
			
			for (int j = 1; j <= i; j++) {
				System.out.print( i + "*" + j + "=" + (i*j) + " " );
			}
			writen("");
		}
		
	}
	
	public static void unjj() {

		for (int i = 9; i >= 1; i--) {
			
			for (int j = 1; j <= i ; j++) {
				System.out.print( j + "*" + i + "=" + (i*j) + " " );
			}
			writen("");
		}
		
	}
	
	public static void jzt() {
		
		for (int i = 1; i <= 9; i++) {
			
			for (int j = 1; j <= 9-i; j++) {
				write(" ");
			}

			for (int j = 1; j <= i; j++) {
				write(j+"");
			}
			
			for (int j = i - 1; j >= 1; j--) {
				write(j+"");
			}
			writen("");
		}
		
	}
	
	public static void ssyz(int n) {
		
		for (int i = 1; i <= 100; i++) {

			write(i+"的素数因子有：");
			
			for (int j = 2; j <= i/2  ; j++) {
				
				if(i%j == 0) {
					int f = 0;
					
					for (int j2 = 2; j2 <= Math.sqrt(j); j2++) {
						
						if(j%j2 == 0) {
							f = 1;
						}
						
					}
					if(f==0) {
						write(j+",");
					}
					
				}
				
			}
			
			writen("");
			
		}
		
	}
	
	
	
	
	
	
	
	
	public static void main(String[] args) {
		TODO Test3
		
//		(一)用*在控制台输出以下图形：
//		(1)	长方形
//		*****
//		*****
//		*****
		writen("第一.3题");
		rectangle();
		
//		(2)	正直角三角形
//		*
//		**
//		***
//		****
		writen("第一.2题");
		triangle();
		
//		(3)	倒直角三角形
//		****
//		***
//		**
//		*
		writen("第三题");
		untriangle();
		
//		(4)	等腰三角形
//		    *
//		   ***
//		*****
		writen("第四题");
		dytriangle();
		
//		(二)请观察下面的九九乘法表，归纳其规律再将其打印出来。
//		1*1=1 
//		2*1=2 2*2=4 
//		3*1=3 3*2=6 3*3=9 
//		4*1=4 4*2=8 4*3=12  4*4=16  
//		5*1=5 5*2=10  5*3=15  5*4=20  5*5=25  
//		6*1=6 6*2=12  6*3=18  6*4=24  6*5=30  6*6=36  
//		7*1=7 7*2=14  7*3=21  7*4=28  7*5=35  7*6=42  7*7=49  
//		8*1=8 8*2=16  8*3=24  8*4=32  8*5=40  8*6=48  8*7=56  8*8=64  
//		9*1=9 9*2=18  9*3=27  9*4=36  9*5=45  9*6=54  9*7=63  9*8=72  9*9=81  
		writen("第二题");
		jj();

//		(三)请大家思考反向乘法口诀如何输出?
//		1*9=9 2*9=18  3*9=27  4*9=36  5*9=45  6*9=54  7*9=63  8*9=72  9*9=81  
//		1*8=8 2*8=16  3*8=24  4*8=32  5*8=40  6*8=48  7*8=56  8*8=64  
//		1*7=7 2*7=14  3*7=21  4*7=28  5*7=35  6*7=42  7*7=49  
//		1*6=6 2*6=12  3*6=18  4*6=24  5*6=30  6*6=36  
//		1*5=5 2*5=10  3*5=15  4*5=20  5*5=25  
//		1*4=4 2*4=8   3*4=12  4*4=16  
//		1*3=3 2*3=6   3*3=9 
//		1*2=2 2*2=4 
//		1*1=1
		writen("第三题");
		unjj();
		
//		(四)思考如何输出以下三角阵
//		1
//	   121
  ........
//12345678987654321
		writen("第四题");
		jzt();
		
//		(五)打印出100以内各数的素数因子
//		24的素数因子有：2，3，
//		25的素数因子有：5，
//		26的素数因子有：2，13，
//		27的素数因子有：3，
//		28的素数因子有：2，7，
//		29的素数因子有：
//		30的素数因子有：2，3，5，
		writen("第五题");
		ssyz(100);
```











# 0 Java SE目录

1. Java起步、大纲、技巧

2. 1. Java环境配置
   2. Java版本平台的分类
   3. Java开发路线
   4. Java语言大纲
   5. Java提示及技巧

3. Java基本数据类型（八种）

4. 1. 八种数据类型
   2. 变量
   3. 基本数据类型的类型转换

5. Java运算符

6. 1. 算数运算符5种
   2. 比较运算符6种
   3. 逻辑运算符3种
   4. 赋值运算符6种
   5. 自增自减
   6. 三目运算符

7. Java流程控制语句

8. 1. if分支语句，单分支
   2. if两分支
   3. if多分支
   4. switch分支语句
   5. for循环
   6. while
   7. do while
   8. break和continue

9. Java数组、方法

10. 1. 数组
    2. 方法

11. Java具体类

12. 1. 概念
    2. 成员变量
    3. 成员方法
    4. 构造方法
    5. 创建对象的语法格式
    6. Java类的创建步骤
    7. toString方法
    8. 成员变量 和 局部变量的区别
    9. Java中的类型分为两种
    10. 值传递
    11. 类类型变量和对象之间的引用关系
    12. null关键字
    13. static关键字
    14. final关键字
    15. this关键字和super关键字

13. Java抽象类

14. 1. 抽象类
    2. 成员变量
    3. 成员方法
    4. 构造方法
    5. 抽象方法
    6. 具体类和抽象类对于抽象方法的区别
    7. 方法的分类总结
    8. 继承的概念
    9. 具体类和抽象类之间的继承讨论
    10. 创建对象的语法格式总结
    11. 父类型和子类型之间的转换
    12. Java语言中每一个类都直接或间接的继承Object类
    13. 构造方法之间的调用
    14. 具体类和抽象类 简单对比

15. Java接口

16. 1. 接口的概念
    2. 接口的成员变量
    3. 接口的成员方法
    4. 构造方法
    5. 类（具体类、抽象类）和接口之间的关系
    6. 具体类、抽象类、接口之间关系
    7. 创建对象的格式
    8. 可见性修饰符关键字：4个范围和3个关键字
    9. 包的引用
    10. 具体类、抽象类和接口的对比

17. Java特征

18. 1. 封装思想

    2. 继承思想

    3. 多态

    4. 1. 多态实现说明
       2. 多态中的两种多态（重载和重写）

19. Java常用API

20. 1. 数学 java.lang.Math
    2. 随机数 java.util.Random
    3. 字符串 java.lang.String
    4. 可变长字符串 java.lang.StringBuffer
    5. 日期 java.uitl.Date
    6. 日期转换 java.text.SimpleDateFormat
    7. 封装类 java.lang.Integer

21. Java 成体系API

22. 1. 集合体系API（接口interface）
    2. IO体系API
    3. 异常体系API

23. Java扩展

24. 1. char和int转换
    2. 二维数组
    3. 递归算法
    4. 数组遍历
    5. 类的初始化顺序
    6. 匿名类
    7. 日期类Date用于转换
    8. 集合扩展
    9. Collection遍历扩展（List和Set）
    10. Map遍历扩展
    11. Java反射API
    12. Java线程API
    13. Java网络API





# 12 Java扩展

20200818



## （1）char 和 int 转换

char c = ‘a’;

int i = c;

syso(i);//输出97

char c2 = i ;

syso(c2)//输出a



## （2）二维数组

int[][] arr = { {1,2} , { 4,5,6 } };

syso(arr[0][1]);//输出2



## （3）递归算法

求n的阶乘

public static int m(int n){

​	if( n == 1 ) return 1;

​	return n * m(n-1);

}



## （4）数组遍历

**标准写法**

for( int i = 0 ; i < arr.length ; i++){

​	syso( arr[i] );

}

**简便写法**

for( int i:arr){

​	syso( i );

}



## （5）类的初始化顺序 类加载顺序

**注意：静态成员** 不能 调用非静态成员！！

- 单个类的初始化顺序：静态成员 -> 非静态成员 ->构造方法

- 继承体系下的类的初始化顺序

- - 父类静态 -> 子类静态 -> 父类非静态 -> 父类构造 -> 子类非静态 -> 子类构造

- final和static 通常连用

- - 常量不需要很多份

- static不常用（Java是面向对象的语言）

- - 通常先new对象，然后用方法
  - 不通常：类.方法



## （6）内部类

- 内部类定义：定义在一个类内部的类

- 一般包括这四种：成员内部类、局部内部类、匿名内部类、静态内部类。

- - 成员内部类：

  - - 最普通的内部类，位于类内部成员变量处
    - 可以访问外部类所有成员
    - 创建对象：需要先创建外部类对象

  - 局部内部类：

  - - 定义在方法内部或作用域内部
    - 该类像局部变量一样，不能有限制修饰符（public、protected、private以及static等）

  - 匿名内部类：

  - - 四种内部类中，用的最多
    - 用于监听代码
    - 方便、使代码易于维护
    - 唯一没有构造器的类
    - 使用范围：接口回调
    - 可用于继承其他类或是接口，并不需要增加额外的方法，只是对继承方法的实现或是重写

  - 静态内部类：

  - - 比成员内部类多一个static关键字
    - 不依赖于外部类，与静态成员类似
    - 不可使用外部类非静态成员



**嵌套类型的内部类：**

public class Outter{



​	// **静态内部类**，文件夹中会多出Outter$StaticInner

​	static class StaticInner{ }



​	// **成员内部类（非静态嵌套类）**，文件夹多出个Outter$Inner

​	class Inner{ }



​	public void m(){	

​		// **局部类**，文件夹多出个Outter$1C	

​		class C{ }

​		// **创建局部类对象**

​		C c = new C();

​	}



}



**成员内部类和静态内部类创建对象的方式：**



// 创建外部类对象

Outter outter = new Outter();



// 创建内部类对象

Outter.Inner inner = outter.new Inner();



// 创建静态内部类对象

Outter staticinner = new Outter.StaticInner();





**用接口举例匿名类：**

- 通常：具体类实现接口，创建对象，调用实现的方法

Car c = new Audi();

c.driver();



- 匿名类：可以把实现的过程 和 创建对象，合二为一

Car c2 = new Audi() {

public void driver(){ syso(“匿名类实现的方法”)};

};//文件夹中多出Java01$1





## （7）日期类Date用于转换：

- Date对象的本质：是一个距离历史时间点（1970年）的毫秒数

Date date = new Date();

long g = date.getTime();

syso(g)//输出毫秒数

- 十天后的日期

date.setTime( date.getTime() + 10 * 24 * 60 * 60 *1000L );

SimpleDateFormat s = new SimpleDateFormat(“yyyy-MM-dd”);

syso( s.format( date ) );//输出十天后的日期





## （8）集合扩展

**List**扩展

- AarrayList 底层是数组结构来实现，遍历起来比较快

- - 创建：List<String> list = new ArrayList<String>();

- LinkedList 底层是 链表结构来实现，添加、删除比较快

- - 创建：List<String> list = new LinkedList<String>();



**Set**扩展

- HashSet不重复

- - 创建：Set<Integer> set = new HashSet();

- TreeSet不重复，自动排序

- - 创建：Set<Integer> set = new TreeSet<Integer>();



**Map**扩展

- HashMap 哈希表的实现类

- - 创建：Map<String,String> map = new HashMap<String,String>();

- TreeMap 按照key自动排序

- - 创建：Map<String,String> map = new TreeMap<String,String>();



## （9）Collection遍历扩展（list和set集合）

**一般遍历方式：**

List<String> list = new ArrayList<String>();

for( String s : list){

​	syso(s);

}



**标准遍历方式：**

- 提示：各种list对象都实现了Iterator接口，所以可以用Iterator存各种list

**第一步：把**list集合的数据放入到新的迭代器集合中

import java.util.Iterator

Iterator<String> i = list.iterator();

**第二步：遍历迭代器中的数据**

while( i.hasNext()){

​	syso( i.next() );

}





## （10）Map遍历扩展

Map<String,String> map = new TreeMap<String,String>();

map.put(“abc”,”123”);

map.put(“bbc”,”123”);

map.put(“aba”,”123”);



**map**的遍历方式一：通过keySet()方法取出一个set集合存key，遍历set集合，通过map.get(key)来获取value

Set<String> set = map.keySet();

for( String s : set ){

​	syso( map.get(s) );

}



**map**的遍历方式二：每次取一个【键值对对象】

Set< Entry<String,String> > set = map.entrySet();

for( Entry<String,String> e : set ){

​	syso( e.getKey() + “\t” + e.getValue() );

}





## （11）Java反射API

- 反射的理解：一种看透Java的能力（类似钩子函数）

- 四个接口：

- - 类对象：java.lang.Class
  - 成员变量对象：java.lang.reflect.Field
  - 成员方法对象：java.lang.reflect.Method
  - 构造方法：java.lang.reflect.Constructor

- 例子：

**类对象：**

Class c = Class.forName(“com.wyh.Person”);

**获取成员变量：**

Field[] arr = c.getDeclaredFields();

for( Field f : arr ){

​	syso( f );//输出成员变量名

}

**获取成员变量：**

Method[] brr = c.getDeclaredMethods();

for( Method m : brr ){

​	syso(m);//输出成员方法

}

**获取构造方法：**

Constructor[] crr = c.getDeclaredConstructors();

for( Constructor c : crr ){

​	syso(c);输出构造方法

}

**获取父类：**

Class f = c.getSuperclass();

syso( f.getName() );

**获取接口：**

Class[] drr = c.getInterfaces();

for( Class i : drr ){

​	syso( i.getName );

}







## （12）Java线程API

- 线程说明：线程即程序中的执行线程。Java虚拟机允许应用程序并发的运行多个线程

- **实现多线程程序的两个方式：**

- 1. 继承Thread类

  2. - extends Thread

  3. 实现Runnable接口

  4. - implements Runnable

- **Java线程中常用方法：**

- 1. **start()：使该线程开始执行；Java 虚拟机调用该线程的 run 方法。**
  2. **run()：如果该线程是使用独立的 Runnable 运行对象构造的，则调用该 Runnable 对象的 run 方法；否则，该方法不执行任何操作并返回。**
  3. **sleep(long millis)：在指定的毫秒数内让当前正在执行的线程休眠（暂停执行），此操作受到系统计时器和调度程序精度和准确性的影响。该线程不丢失任何监视器的所属权。**
  4. **interrupt()：中断线程。如果当前线程没有中断它自己（这在任何情况下都是允许的），则该线程的 checkAccess 方法就会被调用，这可能抛出 SecurityException。**
  5. **yield()：暂停当前正在执行的线程对象，并执行其他线程。**

- 打印当前线程的方法：

- 1. syso(Thread.currentThread().getName());

- 任务管理器：多个线程通过时间片 轮换 交替执行

- Java服务器端 的运行机制 是 多线程机制

- 1. 以前的程序都是单线程的，只执行线程main

- 两个线程API

- 1. java.lang.Thread
  2. java.lang.Runnable



**Thread**类的部分实现：

- 下面代码并没有完全实现Runnable的run功能，想实现多线程，必须重写run方法

 Private Runnable target； // 成员变量，其他线程类对象

 public Thread(Runnable target,String name){ // 构造方法

   init(null,target,name,0); // 调用初始化方法

 } 

 private void init(ThreadGroup g,Runnable target,String name,long stackSize){ // 初始化方法

   ... 

   this.target=target; // 赋值成员线程对象

 } 

 public void run(){ // 运行阶段执行的方法

  if(target!=null){ 

​    target.run(); 

 } 

}



**继承**Thread和实现Runnable的区别：

- 继承Thread：不适合多个线程共享资源
- 实现Runnable：适合实现共享资源



**线程的状态变化：**

- 要想实现多线程，必须在主线程中创建新的线程对象。任何线程一般具有5种状态，即创建，就绪，运行，阻塞，终止。下面分别介绍一下这几种状态：
- 创建状态： 

在程序中用构造方法创建了一个线程对象后，新的线程对象便处于新建状态，此时它已经有了相应的内存空间和其他资源，但还处于不可运行状态。新建一个线程对象可采用Thread 类的构造方法来实现，例如 “Thread thread=new Thread()”。

- 就绪状态 ：

新建线程对象后，调用该线程的 start() 方法就可以启动线程。当线程启动时，线程进入就绪状态。此时，线程将进入线程队列排队，等待 CPU 服务，这表明它已经具备了运行条件。

- 运行状态 ：

当就绪状态被调用并获得处理器资源时，线程就进入了运行状态。此时，自动调用该线程对象的 run() 方法。run() 方法定义该线程的操作和功能。

- 阻塞状态 ：

- - 等待阻塞
  - 同步阻塞
  - 其他阻塞

一个正在执行的线程在某些特殊情况下，如被人为挂起或需要执行耗时的输入/输出操作，会让 CPU 暂时中止自己的执行，进入阻塞状态。在可执行状态下，如果调用sleep(),suspend(),wait() 等方法，线程都将进入阻塞状态，发生阻塞时线程不能进入排队队列，只有当引起阻塞的原因被消除后，线程才可以转入就绪状态。

- 死亡状态 ：

线程调用 stop() 方法时或 run() 方法执行结束后，即处于死亡状态。处于死亡状态的线程不具有继续运行的能力。









⭐️在此提出一个问题，Java 程序每次运行至少启动几个线程？

**回答：**

​	至少启动两个线程，每当使用 Java 命令执行一个类时，实际上都会启动一个 JVM，每一个JVM实际上就是在操作系统中启动一个线程，Java 本身具备了垃圾的收集机制。所以在 Java 运行时至少会启动两个线程，一个是 main 线程，另外一个是垃圾收集线程。



**取得和设置线程的名称：**

 class MyThread implements Runnable{ //实现Runnable接口 

   public void run(){ 

​    for(int i=0;i<3;i++){ 

​      System.Out.Println(Thread.currentThread().getName()+"运行, i="+i); //取得当前线程的名称 

​    } 

  } 

 }; 

 

 public class ThreadDemo{ 

public static void main(String args[]){ 

  MyThread my=new MyThread(); //定义Runnable子类对象 

  new Thread(my).start;  //系统自动设置线程名称 

  new Thread(my,"线程A").start(); //手工设置线程名称 

 } 

};



**结果：**





参考：https://www.cnblogs.com/java1024/archive/2019/11/28/11950129.html

- 线程的操作方法

- - 线程的强制运行：join()

  - 线程的休眠：sleep()

  - 中断线程：interrupt()

  - 后台线程：setDaemon(true)

  - 线程的优先级：setPriority(参数如下)

  - - 最低优先级：(Thread.MIN_PRIORITY)
    - 中等优先级：(Thread.NORM_PRIORITY)
    - 最高优先级：(Thread.MAX_PRIORITY)

  - 线程的礼让：yield()

- 同步及死锁：

- - 同步设置同步代码块：synchronized(同步对象){需要同步的代码}
  - 声明为同步方法：synchronized 方法返回值 方法名称 (参数列表) { }
  - 死锁：A要B先做b事，A才能做a事；B要A先做a事，B才能做b事，这种情况形成死锁





## （13）Java网络API

- C/S

- API包

- - 服务器端的套接字：[java.net](http://java.net).ServerSocket

- IP：主机

- port：分机，端口号，跑不同的软件



**创建服务器端套接字对象：**

// 服务器1004端口监听客户请求

ServerSocket server = new ServerSocket(1004);

while(true){

​	// 等待接收请求

​	// 导入 [java.io](http://java.io).InputStream

​	// 导入 [java.net](http://java.net).Socket

​	Socket s = server.accept();//等待请求

​	InputStream is = s.getInputStream();//存入 输入直接流

​	byte[] b = new byte[1024*5];

​	int i = is.read(b);//实际长度

​	String str = new String(b,0,i);//截取

​	syso(str);//输出请求

}



**客户端**

- 导包：java.new.Socket
- 找到ip地址、port端口号

Socket s = new Socket(“127.0.0.1”,1004);

OutputStream out = s.getOutputStream();

out.write(“你好”.getBytes());

out.close();





## （14）Java泛型

- 泛型说明：即“参数化类型”，用<数据类型列表>形式表示

- 一些常用的泛型类型变量：

- - E：元素（Element），多用于Java集合框架
  - K：关键字（key）
  - N：数字（Number）
  - T：类型（Type）
  - V：值（Valve）

- 意义：

- - 适用于多种数据类型执行相同的代码（代码复用）
  - 泛型中的类型在使用时指定，不需要强制类型转换（类型安全，编译器会检查类型）

- 约束和局限性

- - 不能实例化泛型类
  - 静态变量或方法不能引用泛型变量，不过静态泛型方法可以
  - 基本类型不能转换泛型
  - 无法使用instanceof关键字或==判断泛型类的类型
  - 泛型类的原生类型与传递的泛型无关，无论传递什么类型，原生类是一样的
  - 泛型数组可以声明，但无法实例化
  - 泛型类不能继承Exception或Throwable
  - 不能捕获泛型类限定的异常，但是可以抛出

- 继承规则

- - 对于泛型参数，是继承关系的泛型类之间，是没有继承关系的
  - 泛型类可以继承其他的泛型类，如：public class ArrayList<E> extends AbstractList<E>
  - 泛型类的继承关系在使用中同样会受到泛型类型的影响



##  

## （15）Java网络编程

●**网络编程是指编写运行在多个设备（计算机）的程序，这些设备都通过网络连接起来。**

●**java.net 包中 J2SE 的 API 包含有类和接口，它们提供低层次的通信细节。你可以直接使用这些类和接口，来专注于解决问题，而不用关注通信细节。**

●**java.net 包中提供了两种常见的网络协议的支持：**

●**TCP：TCP 是传输控制协议的缩写，它保障了两个应用程序之间的可靠通信。通常用于互联网协议，被称 TCP / IP。**

●**UDP：UDP 是用户数据报协议的缩写，一个无连接的协议。提供了应用程序之间要发送的数据的数据包。**

●**Socket: 套接字（socket）是一个抽象层，应用程序可以通过它发送或接收数据，可对其进行像对文件一样的打开、读写和关闭等操作。套接字允许应用程序将I/O插入到网络中，并与网络中的其他应用程序进行通信。网络套接字是IP地址与端口的组合。**

●**套接字使用TCP提供了两台计算机之间的通信机制。 客户端程序创建一个套接字，并尝试连接服务器的套接字。当连接建立时，服务器会创建一个 Socket 对象。客户端和服务器现在可以通过对 Socket 对象的写入和读取来进行通信。**

●**Java.net.Socket 类代表一个套接字，并且 java.net.ServerSocket 类为服务器程序提供了一种来监听客户端，并与他们建立连接的机制**

●**参考资料https://www.runoob.com/java/java-networking.html**





## （16）Java序列化

- Java提供了一种对象序列化的机制。
- 序列化：对象可以被表示为字节序列，存入.ser文件中
- 反序列化：就是将序列转换为对象
- 序列化过程：

1. 创建要序列化的类Emp
2. 创建该类对象e
3. 创建FileOutputStream类对象fileout，构造参数为文件地址，如“/tmp/employee.ser”
4. 创建ObjectOutputStream类对象out，参数为上一步创建的对象fileout
5. 向文件写入对象：out.writeObject(e)
6. 关闭out和fileout：out.close();fileout.close();

- 反序列化过程：

1. 创建对象e用于引入文件中对象
2. 创建FileInputSream对象filein，参数为文件地址
3. 创建ObjectInputStream对象in，参数为上一步中创建的对象
4. 用创建好的对象e接收读取出来的对象：e = (Employee) in.readObject();
5. 关闭in和filein：in.close();fileclose();







# 0 基础题





1. JAVA基本数据类型有哪些，各占多少位
2. 基本数据类型转换，什么时候要强制转换
3. JAVA运算符有哪些
4. 流程控制语句格式，写出分支、循环语句，两个中途控制关键字
5. 创建数组正确写法
6. 创建静态方法写法
7. static、final可以用在哪里，有什么效果
8. this、super表示什么
9. 抽象类、具体类、接口有什么区别
10. 怎么理解泛型
11. 多态有哪两种情况，分别有什么特征
12. JAVA常见API







# 1 Java基本数据类型（八种）



- Java数据类型的分类：

- 1. 基本数据类型：存储真实的值
  2. 类类型（引用类型）：对象在内存中地址的值



# （一）八种数据类型

- **4个整数类型: byte,short,int,long**
- **2个小数类型:float,double**
- **2个特殊类型:char,boolean**



## (1)byte字节型(8位)

byte b = 1;



## (2)short短整型(16位)

short s = 12;



## (3)int整型(32位)

int i = 123;



## (4)long长整型(64位)

long l = 1234;

long l = 1234567890L;



![IMG_8534(20200807-161214).PNG](/blob:file:/1719e7d2-a098-4059-853d-fcc236f44430)

# 说明：以上4个类型都可以存整数，不同点是区间由小到大

# 经验：开发中整数默认是int，根据实际情况 放大或缩小



## 例子：//int类型的整数需要在最后面加L 转成Long型的

long ex1 = 1234567890L;



## (5)float单精度浮点数(32位)

- **注意：float变量必须默认写F或f**

float f = 1.23f;



## (6)double双精度浮点数(64位)

double d = 1.2345;



# 说明：以上2个类型的浮点数都可以存浮点数，不同点是区间大小不同

# 经验：开发中 使用的类型 及 浮点数的默认类型 都是double，需要根据实际情况调整类型



## (7)char 字符类型

- **注意：必须是单个字符**

char c = ‘c’;



## (8)boolean布尔类型

- **boolean类型值只有 true 和 false**

boolean b1 = true;

boolean b2 = false;

#  



# （二）变量

- 八种基本数据类型的 变量 可以理解为一个容器

int a= 2;

a = 3;



//final修饰后，变为常量，是恒定的值，不可修改

final int b = 5;

## b = 3; // 会报错





# （三）基本数据类型的类型转换



## (1)同类 不同精度 的类型转换

- **byte < short < int <long**
- **float < double**



**低精度** 可以直接给 高精度 赋值

short a = 2;

int b = a;



**高精度** 给低精度 赋值 需要【强制类型转换】

int b = 6;

short a = (short)b;



int b = 9;

byte a = (byte)b;



## (2)不同类型 整型 与 浮点数

- **整数 可以直接赋值给 浮点数**

- 浮点数 赋值给 整数 需要【强制类型转换】

- - long g = 123;
  - float f = g;



## 浮点数 强转 整数 只保留整数部分，不做四舍五入！！

double d = 223.921;

int i = (int)d;



## (3)自动类型转换

- **如果在计算过程中、低精度的会自动转最高精度、类型一致后、再进行计算**

byte a1 = 2;2.0 f

int a2 = 3;3.0 f

float a3 = 4.5f;



错误的：int a4 = a1 + a2 + a3;2.0

正确的：float a5 = a1 + a2 + a3;



System.out.println(3/2);

输出：1

System.out.println(3/2.0);//自动向最高精度转换

输出：1.5











# 2 Java运算符

- 算数运算符 +、-、*、/、%
- 比较运算符 >、>=、<、<=、==、!=
- 逻辑运算符 &&、||、！
- 赋值运算符 =、+=、-=、/=、%=
- 自增自减运算符 ++、—
- 三目运算符 ？：



## (1)算数运算符 5种

System.out.println(3 + 2);

System.out.println(3 - 2);

System.out.println(3 * 2);

System.out.println(3 / 2);

System.out.println(3 % 2);



## (2)比较运算符 6种

System.out.println(3 > 2);

System.out.println(3 >= 2);

System.out.println(3 < 2);

System.out.println(3 <= 2);

System.out.println(3 == 2);

System.out.println(3 != 2);



## (3)逻辑运算符 3种

- **与:&&** 
- **或:||** 
- **非:!**
- 逻辑与&&表示并且的意思、两边都是true结果为true、其它情况都是false
- 逻辑或||表示或者的意思、有一个为true结果为true、其它情况都是false
- 逻辑非!表示取反的意思、true取反为false、false取反为true

System.out.println("与：");

System.out.println(true && true);

System.out.println(true && false);

System.out.println(false && false);

System.out.println("或：");

System.out.println(true || true);

System.out.println(true || false);

System.out.println(false || false);

System.out.println("非：");

System.out.println(!true);

System.out.println(!false);



## (4)赋值运算符 6种

int a = 2;

a += 2;

a -= 2;

a *= 2;

a /= 2;

a %= 2;



## (5)自增自减运算符 ++ --

System.out.println(a++);

System.out.println(a);

System.out.println(++a);

System.out.println(a--);

System.out.println(a);

System.out.println(--a);



## (6)三目运算符 ? :

- **(条件)?(结果1):(结果2)**
- **true -> 结果1**
- **false -> 结果2**

int b = (true ? 1 : 2 );

结果：b = 1

int b = (true ? 1 : 2 );

结果：b = 1







# 3 Java流程控制语句

- 分支语句：if、switch
- 循环语句：for、while、do while
- 中途控制：break、continue



## (1) if 分支语句，单分支

if(true) {

​	System.out.println(1);

}

if(false) {

​	System.out.println(2);

}



## (2) if 两分支

- 与三目运算一个逻辑

if(false) {

​	System.out.println(3);

}else {

​	System.out.println(4);

}



## (3) if 多分支 只能执行一个分支

if(false) {

​	System.out.println(5);

}else if(false) {

​	System.out.println(6);

}else{

​	System.out.println(7);

}



## (4) switch 分支语句

- 根据常量来执行不同分支
- 只能判断 byte,short,int,char,String 
- break:跳出分支语句

int a = 1;

String s = "1";

switch(s) {

case "1":

​	System.out.println(11);

​	break;

case "2":{

​	System.out.println(22);

​	break;

}

case "3":

​	System.out.println(33);

​	break;

default:

​	System.out.println("default");

}





## (5) for循环



for( A ; B ; C ) {

​	D

}



**执行流程：**

A -> B(布尔值false) -> D -> C -> B(false) -> 退出循环





**for(初始化; 布尔表达式; 更新) {**

  **代码语句**

**}**



**括号内三部分**

- **循环变量起始值**
- **循环执行的条件**
- **单次执行后变量更新操作**



**打印**1-10

System.out.println("打印1-10");

for (int i = 1 ; i < 11 ; i++) {

​	System.out.println(i);

}

System.out.println("打印完毕");





## (6) while

int i = 1 ;

for ( ; i < 11 ; ) {

​	System.out.println(i);

​	i++;

}

System.out.println("while 循环");

i = 1;

while(i<11) {

​	System.out.println(i);

​	i++;

}



## (7) do while

- 先执行，后判断，至少执行一次

i = 1;

do {

​	System.out.println(i);

​	i++;

} while(i<11);



## (8)break和continue

- break和continue 可以用于循环语句中
- break 可以跳出循环，终止循环
- continue 可以终止这一次循环，直接下一次循环



for (int i=1;i<=10;i++) {

​	if(i==4) {

break;

​	}

​	System.out.println(i);

}

System.out.println("-----");

for (int i=1;i<=10;i++) {

​	if(i==4) {

continue;

​	}

​	System.out.println(i);

}







# 4 Java数组、方法



# （一）数组

## (1) 创建数组

## 错的：

int arr = new int[10];

## 对的：

int[] arr = new int[10];	//长度为10

int arr[] = new int[10];	//长度为10

int arr[] = {};				// 长度为0 

int[] arr = {1,2,3,4};		// 长度为4

## 推荐写法：

int[] a = {1,2,3,4,5};

double[] b = {2.5 , 32.5 , 421.23};

char[] c = {'你','A','5'};



## (2) 存取数据

- 数组中元素的存取必须通过下标实现、而且下标是从零开始计数的。

**通过下标实现** 元素5和元素4位置互换

System.out.println(a[4]);

a[4] = 888;

System.out.println(a[4]);



**(3)** 遍历数组

**数组的**length属性 表示 数组的长度 或 元素的个数

for (int i = 0; i < a.length; i++) {

​	System.out.println(a[i]);

}



# （二）方法

- **方法需要掌握的内容：两个定义格式 和 两个调用格式**⬇️

- **掌握没有返回值方法的定义格式和调用格式**

- **掌握有返回值方法的定义格式和调用格式(项目中最常用/重点)**

- 主方法：是Java应用程序的运行入口主方法 的方法定义 不能有任何修改 

- - 可以通过 先写一个 main ，然后按opt+/ 直接生成下面的语句
  - public static void main(String[] args) {  }

​	

## 方法分两类



**第一类：** 没有返回值

**定义格式：**

public static void 方法名 (参数列表){方法体}



**例子：**

public static void m1( int a , int b ){ }



**调用格式：** 方法名(参数列表)

- 注意 参数列表 中的参数 顺序一定要 完全一致



**例子：**

m1();

m2(4,5.3,'a');

m3(true);



**第二类：有返回值的**

**定义格式：**

public static 返回类型 方法名 (参数列表){方法体,return语句}



**例子：**

public static int m2( int a , int b ) { }



**调用格式：**	返回类型 变量名 = 方法名(参数列表);



**例子：**

int x = m4();

System.out.println(x);

System.out.println(m5());

System.out.println(m6()[3]);







# 5 Java具体类



## (01)概念



- 类的概念 : 

- - 被class关键字修饰的叫做类。
  - 用来描述现实生活中实例的"图纸"或"模板"。

 

-  对象的概念:

- - 通过调用类的构造方法 创建出来的、生产出来的 具体的实例。
  -  表示现实生活中的"实例"或"实体"。

 

 现实生活		->		Java世界中(电脑内存中)

 图纸			->		类

 实体			->		对象

 

## (02)成员变量:

- 在类中定义的变量 叫做 类的成员变量。
- 用来描述类的 属性 或 状态 。

 

## (03)成员方法:

- 在类中定义的方法 叫做 类的成员方法。
- 用来描述类的 行为 或 功能。

 

## (04)构造方法:

- 用来创造对象的方法
- **方法名必须与类同名、并且没有返回值、也没有void关键字。**
- 作用：根据类构造出对象所调用的方法。
- 默认：当类中 一个都没有 写构造方法的时候、系统会自动提供一个无参的构造方法。
- **建议：每个类中都要写上 无参 和 有参 的构造方法。**

 

## (05)创建对象的语法格式:

**类名** 变量 = new关键字 构造方法 ;

 

## (06)Java类的创建步骤:

- 第一步：创建类(注意首字母大写)
- 第二步：成员变量
- 第三步：生成构造方法(注意通过生成无参和有参的构造方法)
- 第四步：生成getter方法和setter方法
- 第五步：生成toString方法



**创建具体类过程**:

**//01.**创建类

public class Company {

​	

​	**//02**成员变量

​	String name;

​	String address;

​	

​	**//03**生成构造方法 右键->source->生成构造方法

## 	//有参和无参 要各生成一个！！！

​	public Company() {

​		super();

​	}



​	public Company(String name, String address) {

​		super();

​		this.name = name;

​		this.address = address;

​	}

​	

​	**//04**生成get set方法

​	public String getName() {

​		return name;

​	}



​	public void setName(String name) {

​		this.name = name;

​	}



​	public String getAddress() {

​		return address;

​	}



​	public void setAddress(String address) {

​		this.address = address;

​	}

​	

​	**//05**生成toString方法

​	*@Override*

​	public String toString() {

​		return "Company [name=" + name + ", address=" + address + "]";

​	}



}



 

## (07)toString方法:

- 通常类中会生成一个toString方法、它可以方便的打印类中的成员变量的信息。

- 当我们使用输出语句打印某对象的时候、Java会自动调用类中的toString方法。

 

## (08)成员变量 和 局部变量的区别

- 成员变量 : 在类中定义的变量。作用域是在整个类的内部都可以使用。**系统会自动默认赋值。**

- 成员变量默认值 : 

- - 整数默认0
  - 浮点数默认0.0
  - 布尔值默认false
  - 类类型默认值是null
  - char：空

- 局部变量 : 在方法中定义的变量。作用域是在整个方法的内部可以使用。系统不会自动赋值、必须手动赋值才能使用。

 

## (09)Java中的类型分为两种

- **基本数据类型**：八种基本数据类型。基本类型的变量中存储的是真实的数据真实的值。
- **类类型(引用类型)**：除了8种基本数据类型之外的都是类类型。类类型的变量中存储的是数据或值的对应的内存地址的引用。地址的值。

 

## (10)值传递

- **基本数据类型传递的是真实的值**。原因：基本数据类型存储的就是真实的值。
- **类类型传递的是地址的值**。原因：类类型存储的是地址的值。

- 提示：Java思想把类类型的变量翻译为“遥控器”、类类型的变量和对象之间的关系是一个引用关系。

 

## (11)类类型变量和对象之间的引用关系

- 变量可以引用零个或一个实例。

- - 既 一个类 可以赋值一个地址 或 空地址

- 一个实例可以被多个变量引用。

- - 既一个实例可以有 多个类指向它的地址

 

## (12)null关键字(空)

- 表示 类类型的变量 任何对象都不引用。
- 当某个对象没有被任何变量引用的时候、该对象会被Java的垃圾回收机制回收并**释放内存空间**。

 

## (13)static关键字(静态)

- 用处：区别 类的变量和方法 与 对象的变量和方法

- 用法：用static修饰的 就是 类的变量和方法

- - 理解:static关键字是用来区别类和对象、区别哪些成员在类中、哪些成员在对象中。

- 被static修饰的叫静态成员

- - 成员都在 类 中、属于类、类成员
  - 通过"类名.成员"的方式来调用。

- 不被static修饰的叫非静态成员

- - 成员都在 对象 中、属于对象、对象成员
  - 通过"对象.成员"的方式来调用。

- 静态成员 也可以被对象 调用，既 静态成员可以被所有对象共用共享。(不建议)



## (14)final关键字(最终、恒定)

- final修饰的变量是常量

- - 不能更改。

  - - 基本数据类型，不可以改值
    - 类类型，不可以改地址、调用

- final修饰的方法、不能被覆盖。

- - 父类用final修饰，子类不可以再定义该方法

- final修饰的类、不能被继承。

- 在早期的JVM实现版本中，被final修饰的方法会被转为内嵌调用以提升执行效率。而从Java SE5/6开始，就渐渐摈弃这种方式了。因此在现在的Java SE版本中，不需要考虑用final去提升方法调用效率。只有在确定不想让该方法被覆盖时，才将方法设置为final。

 

## (15)this关键字和super关键字

- this表示当前类的对象。

- - 既 new关键字调用构造方法时候所创建出来的对象。

- this关键字可以区分同名的成员变量和局部变量、this所引用的变量是成员变量。

- super表示父类的引用。

- - super()就是父类构造方法的引用，可能含参

-  成员方法中：name = name，左边是成员变量，右边是局部变量。

 





# 6 Java抽象类



- Java语言概念主线:具体类、抽象类、接口



## (01)抽象类:

- 被abstract关键字修饰的类叫做抽象类。

- - public abstract class Person{ }

- 用来描述现实生活中"抽象的图纸"、"抽象的模板"。

- 具体类 和 抽象类的举例对比：

- - 具体类:长方形类、圆形类、猫类、狗类。

  - - 目的：作为图纸，用来创建对象。

  - 抽象类:图形类、动物类。

  - - 目的：设计图纸



## (02)成员变量:

- 在抽象类中定义的 变量 叫做抽象类的成员变量。
- 描述抽象类的属性或状态
- 创建方式：同具体类创建方式一样



## (03)成员方法:

- 在抽象类中定义的 方法 叫做抽象类的成员方法。
- 描述抽象类的工作或作用。
- 创建方式：同具体类创建方式一样 或者 是抽象方法（无方法体）



## (04)构造方法:

- 方法名和类同名、没有返回值也没有void关键字。
- 注意:抽象类中有构造方法。但是抽象类不能创建对象！！
- 目的:**设计、管理**。由项目经理、项目组长、项目管理者来做。



## (05)抽象方法:

- 特点：

- 1. 被abstract修饰
  2. 没有方法体

- **注意:**只有方法的定义没有方法的实现。

- **目的:**在于设计方法。

- **理解:**只考虑方法名、参数列表、返回类型、根本不考虑实现。



## (06)具体类 和 抽象类 对于抽象方法的区别:

- 抽象类中 **不一定** 包含抽象方法
- 包含抽象方法的类 **一定是** 抽象类。



## (07)方法的分类总结:

- 第一种，**是否返回值：**没有返回值的方法、有返回值的方法。
- 第二种，**是否静态**：静态的方法、非静态的方法。
- 第三种，**是否实现**：抽象的方法、实现的方法。



## (08)继承的概念:

- 子类通过使用extends关键字可以继承父类中所有的成员。
- 格式：public class 子类 extends 父类
- 理解:父类有的子类都有。



## (09)具体类 和 抽象类 之间的继承讨论:

- 由于具体类和抽象类都是类、所以他们之间可以相互继承
- 具体类 可以继承 抽象类(**父类是抽象类、子类是具体类、在实际开发中最常见**)
- 具体类 可以继承 具体类
- 抽象类 可以继承 具体类
- 抽象类 可以继承 抽象类



## (10)创建对象的语法格式总结:

- 第一种:类名(具体类) 变量 = new 构造方法(具体类)
- 第二种:父类  变量 = new 子类构造方法



## (11)父类型和子类型之间的转换:

- 子类型转换为父类型没问题
- 父类型转换为子类型就必须【强制类型转换】



## (12)Java语言中每一个类都直接或间接的继承Object类。

- 如果某个类没有指定直接父类、则系统会默认添加extends Object。
- Object类是所有Java类的顶级父类、单根继承。
- 每个类的构造方法的首句、都会默认调用父类的无参构造方法。



## (13)构造方法之间的调用

- this表示当前类的对象。super表示父类的引用。

- 调用当前类中构造方法使用this关键字。this也可以调用本类的其它成员。

- - this()是当前类的构造方法，也可以根据参数列表来判定调用的哪个方法，比如：this(“aa”); this(“bb”,12);
  - **一般省略this，this.m1()和m1()一样，一般直接写m1()**

- 调用父类中的构造方法使用super关键字。super也可以调用父类的其它成员。

- - 没写的话，系统也会自动生成
  - super(“”); super();super(“”,123);
  - 一般省略super，super.name 和 name 一样，一般直接写name



## (14) 具体类 和 抽象类 简单对比

- 具体类class：

- - 成员变量、成员方法、构造方法，
  - 为了创建对象 

- 抽象类abstract class：

- - 成员变量、成员方法、构造方法、抽象方法、
  - 为了被继承







# 7 Java接口

20200813

## (01)接口的概念：

- 被interface修饰 叫做 接口
- 描述生活中的“标准” 或 “规范”
- 定义接口格式：public interface Company{ }



**定义接口例子：**



public interface Member {



​	public static final int a = 100;

​	

​	int b = 2;

​	

​	public abstract void m1(int b);

​	

​	double m2(boolean boo);

​	

}



## (02)接口的成员变量： 

- 默认被public static final修饰



## (03)接口的成员方法： 

- 默认被public abstract修饰



## (04)构造方法：

## 接口中没有构造方法，也不能创建对象！！



## (05)类（具体类、抽象类）和接口之间的关系：

- 类可以实现接口

- - 格式：public class 类 implements 接口 { }

- 第一步：接口角色：设计

- 第二步：抽象类角色：部分功能实现 

- 第三步：具体类角色：全部功能实现



## (06)具体类、抽象类、接口之间关系：

- 类与类：继承关系 extends 
- 接口与接口：继承关系 extends 
- 类与接口：实现关系implements



## (07)创建对象的格式：

-  第一种：类（具体类） 变量 = new 构造方法（具体类的构造方法）
-  第二种：父类（抽象类） 变量 = new 构造方法（子类的构造方法）
-  第三种：接口 变量 = new 构造方法（实现类的构造方法）



## (08)可见性修饰符关键字：4个范围和3个关键字

- 从小到大的成员可用范围：

| 关键字    | 意义             | 可见范围                                       |
| --------- | ---------------- | ---------------------------------------------- |
| private   | 私有             | 本类                                           |
| 默认      | 默认（不加修饰） | 本类+本包                                      |
| protected | 保护             | 本类+本包+外包子类（需要导包import 包名.类名） |
| public    | 公共             | 都可见                                         |



## (09)包的引用

- 注意：

- - 本包的类：可以直接调用

  - - 例子：Person.run();

  - 外包的类：必须import关键字导入，才能调用

​	

## (10)具体类、抽象类 和 接口 的对比



|              | **类**       | **抽象类**         | **接口**                |
| ------------ | ------------ | ------------------ | ----------------------- |
| **关键字**   | **class**    | **abstract class** | **interface**           |
| **成员变量** | **都可以**   | **都可以**         | **public static final** |
| **成员方法** | **全部实现** | **部分实现**       | **public abstract**     |
| **构造方法** | **有**       | **有**             | **没有**                |
| **创建对象** | **能**       | **不能**           | **不能**                |
| **意图目的** | **实现**     | **设计**           | **设计**                |



**做项目步骤：先设计，再实现**	







# 8 范型



参考 https://www.jianshu.com/p/1ea6868efdd1









# 9 注解



- Java 注解（Annotation）又称Java标注，是JDK5.0引入的一种注释机制
- Java语言中的类、方法、变量、参数和包都可以被标注。
- 和Javadoc不同，Java标注可以通过反射获取标注内容。在编译生成class文件时，标注可以被嵌入到字节码中。Java虚拟机可以保留标注内容，在运行时获取标注内容。
- 当然，也支持自定义的Java标注。



**Java**中内置的注解：

- Java定义了一套注解，共7个，3个在java.lang中，剩下4个在java.lang.annotation中

- 作用在代码的注解：

- 1. @Override - 检查方法是否重载方法。如发现其父类或引入接口中并没有该方法时，会报编译错误
  2. @Deprecated - 检查过时方法。如果使用该方法，会报编译警告
  3. @SuppressWarnings - 指示编译器去忽略注解中声明的警告



**作用在其他注解的注解（元注解）：**

- @Retention - 表示当前注解怎么保存，只是在代码中，还是编入class文件中，或者在运行时可以通过反射访问
- @Documented - 标记这些注解是否包含在用户文档中
- @Target - 标记当前注解应该是哪种Java成员
- @Inherited - 标记这个注解是继承于哪个注解类（默认：注解并没有继承于任何子类）



**从**Java7开始，额外添加了3个注解：

- @SafeVarargs - Java7开始支持，忽略任何使用参数位泛型变量的方法或构造函数调用产生的警告
- @FunctionalInterface - Java8开始支持，标识一个匿名函数或函数式接口
- @Repeatable - Java8开始支持，标识某注解可以在同一个声明上使用多次





# 10 枚举



code sheep 枚举使用说明参考：https://mp.weixin.qq.com/s/DgOr7cat8SP0zoY7Ke3toQ



## 枚举与常量类的区别

https://www.cnblogs.com/dqiii/p/13229521.html

https://blog.csdn.net/yin_pisces/article/details/52050427





- 是一种数据类型，属于基础数据类型（在C语言中属于构造数据类型）

- 为了满足【一个变量可能是一组数据其中的一个】这种情况而出现

- 当变量有上述需求时，可以定义为枚举类型

- 枚举可以根据Integer、Long、Short或Byte中的任意一种数据类型来创建一种新型变量。

- 这种变量能设置为已经定义的一组之中的一个

- 有效地防止用户提供无效值

- 该变量可使代码更加清晰，因为它可以描述特定的值。

- 基础类型必须能够表示该枚举中定义的所有枚举数值。

- 枚举声明可以显式地声明 byte、sbyte、short、ushort、int、uint、long 或 ulong 类型作为对应的基础类型。

- 没有显式地声明基础类型的枚举声明意味着所对应的基础类型是 int。

- 默认值

- - 在枚举类型中声明的第一个枚举成员它的默值为零。
  - 以后的枚举成员值是将前一个枚举成员（按照文本顺序）的值加 1 得到的。
  - 这样增加后的值必须在该基础类型可表示的值的范围内；否则，会出现编译时错误。

- 如下示例都以C语言中的方法，其他也都类似



示例：

public enum TimeofDay:uint

{

  Morning,

  Afternoon,

  Evening

};



Morning的值为0,Afternoon的值为1,Evening的值为2。





- 允许多个枚举成员有相同的值.
- 没有显示赋值的枚举成员的值，总是前一个枚举成员的值+1.



示例：

public enum Number

{

  a=1,

  b,

  c=1,

  d

};



b的值为2,d的值为2.





**枚举类型与基础类型的转换**

- 基础类型不能隐式转换为枚举类型
- 枚举类型也不能隐式转换为基础类型



示例：

public enum Number

{

  a,

  b,

  c,

  d

};



class Test

{

  public static void Main()

  {

​    int i=Number.a;//错误，要强制类型转换(int)Number.a

​    Number n;

​    n=2 //错误,要强制类型转换(Number)2

  }

}





**System.Enum类型**

- System.Enum 类型是所有枚举类型的抽象基类,并且从 System.Enum 继承的成员在任何枚举类型中都可用。
- System.Enum 本身不是枚举类型。相反，它是一个类类型，所有枚举类型都是从它派生的。
- System.Enum 从类型 System.ValueType派生









## 使用枚举类型



using System;

public enum TimeofDay

{

  Morning,

  Afternoon,

  Evening

};



class Test

{

  static void WriteGreeting(TimeofDay timeofDay)

  {

​    switch(timeofDay)

​    {

​      case TimeofDay.Morning:

​        Console.WriteLine("good morning");

​        break;

​      case TimeofDay.Afternoon:

​        Console.WriteLine("good afternoon");

​        break;

​      case TimeofDay.Evening:

​        Console.WriteLine("good evening");

​        break;

​    }

  }



  static void Main()

  {

​    WriteGreeting(TimeofDay.Morning);

​    WriteGreeting(TimeofDay.Evening);

​    WriteGreeting(TimeofDay.Afternoon);

  }



}





①赋值运算 COLOR：=RED ；注意类型一致不能出界；

②关系运算 IF

③输入 枚举变量的值只能用赋值语句获得，不要用READ语句；

④输出 不能直接用WRITE语句直接输出枚举元素，系统会认为它是一个

未定义的变量名；必须赋给一个枚举变量，然后输出给变量的值；



如果想要用READ和WRITE语句，怎么办？

- VAR I：INTEGER；

- COLOR：（RED，YELLOW，BLUE）；

- BEGIN

- - WRITELN（‘0—RED ，1—YELLOW ，2—BLUE ’）；

  - READLN（I）；

  - - CASE I OF
    - ：COLOR：=RED；：COLOR：=YELLOW；：COLOR：=BLUE END；
    - { 数据处理 }
    - CASE COLOR OF
    - RED ：WRITELN（‘RED’）；
    - YELLOW：WRITELN（‘YELLOW’）；
    - BLUE：WRITELN（‘BLUE’）

  - END；

- END.



例二：一家水果店出售4种水果，每千克价格分别是：苹果1.15元，桔子1.20元，香蕉0.95元，菠萝0.85元。编一程序使售货员主要从键盘上打入货品的代码及重量，计算机将显示货品名、单价、重量及总价。货品代码为苹果1，桔子2，香蕉3，菠萝4。



CONST PA=1.15；PO=1.20；PB=0.95；PP=0.85；

TYPE FRUITTYPE =（APPLE，ORANGE，BANANA，PINEAPPLE）；

VAR TOTAL，WEIGHT，P：REAL； { 重量和价格 }

CODE：INTEGER； { 代码 }

FRUIT：FRUITTYPE；

- BEGIN

- - READLN（CODE，WEIGHT）；

  - WHILE （CODE>=1）AND （CODE<=4）DO

  - BEGIN

  - - CASE CODE OF
    - 1 : FRUIT:=APPLE;
    - 2 : FRUIT:=ORANGE;
    - 3 : FRUIT:=BANANA;
    - 4 : FRUIT:=PINEAPPLE;
    - END;
    - CASE FRUIT OF
    - APPLE : BEGIN WRITE(‘APPLE’); P:=PA END;
    - ORANGE: BEGIN WRITE(‘ORANGE’); P:=PO END;
    - BANANA : BEGIN WRITE(‘BANANA’); P:=PB END;
    - PINEAPPLE : BEGIN WRITE(‘PINEAPPLE’); P:=PP END;
    - END;
    - WRITE(P:6:2, ‘ * ’, WEIGHT:6:2 , ‘ = ’);
    - WRITELN(p*WEIGHT:8:2);
    - READLN(CODE,WEIGHT);

  - END;

- END.

C中示例：

typedef enum {

DEMO_LABEL_A = 0,

DEMO_LABEL_B,

DEMO_LABEL_C

DEMO_LABEL_D

} demo_label_t;

demo_label_t demo_label;

/* 对demo 的赋值操作 */

if (demo_label == DEMO_LABEL_C)

printf ("the label is C");





# API





# 0 说明





jdk11: https://docs.oracle.com/en/java/javase/11/docs/api/index.html



# 1 数字API

20200813

- API：应用程序接口（标准、规范）
- 理解：Java语言 提供了 很多具体类、抽象类、接口，这些类提供了开发中常用的功能和方法



## （1）数学java.lang.Math

- 分析:static、public、返回值、构造方法可见性私有private

- 常见的方法、变量

- - Math.max(2,3);取最大
  - Math.min(2,3);取最小
  - Math.abs(-12.34);变成正数
  - Math.PI 圆周率





## （2）随机数java.util.Random



**第一步：创建随机数对象**

Random r = new Random();



**第二步：调用**nextInt方法返回一个随机整数，从0到n-1的一个随机数，格式：r.nextInt(int n)

char[] arr = {'你', '我', '他', '它'};

for (int i=0; i < 4; i++) {

​	System.out.print(arr[r.nextInt(4)]);

}







# 2 字符串API







##  （3）字符串java.lang.String

- 对比String、StringBuilder、StringBuffer：

https://www.cnblogs.com/dolphin0520/p/3778589.html

- String：对String的任何操作都不会影响到原对象，任何改变操作都会产生新对象
- StringBuilder：在对原有字符串操作时，不会产生新的对象
- StringBuffer：在StringBuilder的基础上，添加了同步关键字，相对SB是线程安全的





- 说明一:java.lang.*包中的类会自动导入、除此包外其它的类必须手动导入才能使用。
- 说明二:字符串类是所有类型中使用最多的一个类所以要掌握字符串中常用的10个方法。
- 说明三:字符串的本质实际上是一个字符数组char[]

1. length方法：求长度

2. - int a = s.length()

3. charAt方法：根据下标获取字符

4. - char b = s.charAt(4)

5. equals方法：判断值相等

6. - boolean c = s.equals(“abc”)

7. indexOf方法：查找字符串，如果找到则返回起始下标、如果找不到则返回-1

8. - int d = s.indexOf(“abc”)

9. substring方法：截取字符串

10. - 从起始下标截取到最后：String e1 = s.substring(2)
    - 包含结束下标 的用法：String e2 = s.substring(2,3)

11. trim方法：去除两端空格

12. - String f = s.trim()

13. isEmpty方法：字符串是否为空

14. - boolean flag = s.isEmpty();

15. startsWith、endsWith方法：判断起始、结束

16. - boolean g1 = s.startsWith(“ab”)
    - boolean g2 = s.endsWith(“cd”)

17. replace方法：替换字符串

18. - String h = “abcdef”.replace(“cd”,”你好”)

19. toUpperCase、toLowerCase方法：转换大小写

20. - String i = “abCDef”.toUpperCase()
    - String i = “abCDef”.toLowerCase()

21. valueOf方法：基本数据转换为字符串

22. - String j = String.valueOf(5)
    - String j = String.valueOf(6.1)

23. contains方法：是否包含某字符串

24. - boolean k = “abcd”.contains(“bc”)

25. split方法：分割字符串

26. - 注意：返回字符串数组
    - String[] l = “张三,李四，王五”.split(“,”)











## 字符串补充一：字符串的两种创建方式 及 对比

- 具体类/抽象类/接口	变量  = new关键字  构造方法
- 字符串有两种创建对象方式



**(1)**通过字面值直接赋值(建议)

- 原因一:代码简单(字符串开发使用太频繁)
- 原因二:字面值赋值效率高、当使用字面值赋值的时候、Java会先检查内存中是否有此字符串、如果有则直接引用、如果没有再创建新的字符串。

String s1 = "abc";

System.out.println(s1);



**(2)**通过new创建对象(不建议)

- 不建议的原因：每次创建对象，不管有没有重复的，都新分配存储空间，效率低，浪费空间



**创建格式：**

String s2 = new String("abc");



**举例说明：**

**第一种字符串的创建方式：（建议使用）**

String a = "abc”;地址：301

String b = "abc”;地址：301

System.out.println(a == b);地址相同输出true

System.out.println(a.equals(b));

**第二种字符串的创建方式：（不建议使用）**

String c = new String("你好");302

String d = new String("你好");303

System.out.println(c == d);地址不同输出false

System.out.println(c.equals(d));



## 字符串补充二:

基本数据类型之间  使用==来比较相等

类类型之间  使用equals方法来比较相同

如果类类型  使用==比较表达的是**两个对象的地址**是否相等、**而不是值**是否相等



## （4）可变长字符串java.lang.StringBuffer

- String、StringBuffer和StringBuilder对比：

- - String：常量，不可修改
  - StringBuffer：可修改
  - StringBuilder：可修改，比StringBuffer不线程安全

- 提示：String字符串使用+可以连接多个字符串、"+"在字符串中表示连接的意思、"+"还可以把其它数字类型自动转换为字符串类型

- - 如：String s = 1 + “a” +true ;

- 说明:当字符串的值经常改变连接的时候、建议使用StringBuffer来实现、这样效率更高。

- 原因:

- - String类是一个不变的字符串、如果改变字符串的值、会每次都创建一个新的字符串。
  - StringBuffer类是一个可变字符串、如果改变字符串的值、对象时不会重新创建、而是直接修改原有字符串

- 用法：StringBuffer中的append方法相当于String使用中的+、都是连接的意思。

- 建议：在实际开发中如果字符串经常连接或改变，建议使用StringBuffer类



**反应**StringBuffer在多次改变时，地址的改变情况的例子：

StringBuffer a = new StringBuffer("abc");

System.out.println(a.hashCode());// 地址：102

a.append("123");

System.out.println(a.hashCode());// 地址：102

a.append(true);

System.out.println(a.hashCode());// 地址：102

a.append(-12.34);

System.out.println(a.hashCode());// 地址：102















**1.**对比地址



String s1="ABC";

String s2="ABC";

System.out.println(s1==s2);



输出：true



String s1=new String ("ABC");

String s2=new String("ABC");

System.out.println(s1==s2);



输出：false





**2.**对比内容是否相同



s1.equals(s2)





**3.**对比大小

- s1比s2大，返回1
- 相等，返回0
- s1比s2小，返回-1
- 依据：根据Unicode编码比较



s1.compareTo(s2)





**4.**获取长度



s1.length()





**5.**根据下标获取单个字符

- 下标从0开始
- 如超过length-1，会返回error



s1.charAt(3)



输出：字符串中第四个字符





**6.**获取字符串的子串

- substring(b,e)，返回从b到e-1的全部内容



s1 = 0123456

s1.substring(3,6)



输出：345





**7.**判断是否包含字符、字符串

- 存在，返回首个元素下标
- 不存在，返回-1
- indexOf(c,n)：从n位置开始寻找c



s1.indexOf(s2)

s1.indexOf(c1)

s1.indexOf(c2,3)





**8.**去除两端空格



s1.trim()





**9.**替换字符串



s1.replace(“abc”,”123”)





**10.**转换大小写



s1.toUpperCase()

s2.toLowerCase()





**11.**基本数据类型转换为字符串



s1 = String.valueOf(3213.321)





**12.**是否包含字符串



boolean boo = “abcd”.contains(“bc”)





**13.**分割字符串

- 返回字符串数组



String[] strs = “张三,李四,王五”.split(“,”)









**1、equals()：比较两个字符串是否相等** 

它具有如下的一般形式：boolean equals(Object str) 

str是一个用来与调用字符串（String）对象做比较的字符串（String）对象。如果两个字符串具有相同的字符和长度，它返回true，否则返回false。这种比较是区分大小写的。 



**2、equalsIgnoreCase( )：忽略大小写的两个字符串是否相等比较** 

当比较两个字符串时，它会认为A-Z和a-z是一样的。 

其一般形式如下：boolean equalsIgnoreCase(String str) 

str是一个用来与调用字符串（String）对象做比较的字符串（String）对象。如果两个字符串具有相同的字符和长度，它也返回true，否则返回false。 

**3、toString()：转换成String类型** 

Object object = getObject(); 

System.out.println(object.toString()); 

注意：必须保证object不是null值，否则将抛出NullPointerException异常。 

采用这种方法时，通常派生类会覆盖Object里的toString（）方法。 

**4、String：转换成String类型** 

（String）object：这是标准的类型转换，将object转成String类型的值。 

注意：类型必须能转成String类型。因此最好用instanceof做个类型检查，以判断是否可以转换。否则容易抛出CalssCastException异常。 

因定义为Object 类型的对象在转成String时语法检查并不会报错，这将可能导致潜在的错误存在。 

如： Object obj = new Integer(100); 

String strVal = (String)obj; 

在运行时将会出错，因为将Integer类型强制转换为String类型，无法通过。 

但是， Integer obj = new Integer(100); 

String strVal = (String)obj; 

如是格式代码，将会报语法错误。此外，因null值可以强制转换为任何java类类型，(String)null也是合法的。 

**5、String.valueOf()：转换成String类型（不用担心object是否为null值这一问题）** 

注意：当object为null 时，String.valueOf（object）的值是字符串”null”，而不是null。 

**6、split()：分隔符** 

1、如果用“.”作为分隔的话,必须是如下写法,String.split("\\.") 

2、如果用“|”作为分隔的话,必须是如下写法,String.split("\\|") 

“.”、“|”、"*" 和"+"都是转义字符,必须得加"\\"; 

3、如果在一个字符串中有多个分隔符,可以用“|”作为连字符,比如,“acount=? and uu =? or n=?”,把三个都分隔出来,可以用String.split("and|or"); 

例如：String[] aa = "aaa|bbb|ccc".split("\\*"); 

for (int i = 0 ; i <aa.length ; i++ ) { 

System.out.println("--"+aa[i]); 

} 

**7、subString()：截取字符串中的一段字符串** 

String str; 

（1）str＝str.substring(int beginIndex); 

截取掉str从首字母起长度为beginIndex的字符串，将剩余字符串赋值给str； 

（2）str＝str.substring(int beginIndex，int endIndex); 

截取str中从beginIndex开始至endIndex结束时的字符串，并将其赋值给str; 

**8、charAt()：返回指定索引处char值** 

public char charAt(int index) 

char s = str.charAt(1); 

**9、toLowerCase()：将所有在此字符串中的字符转化为小写（使用默认语言环境的规则）** 

public String toLowerCase() 

String newStr = str.toLowerCase(); 

**10、indexOf()：指出 String 对象内子字符串的开始位置** 

1、int indexOf(String str) ：返回第一次出现的指定子字符串在此字符串中的索引。 

2、int indexOf(String str, int startIndex)：从指定的索引处开始，返回第一次出现的指定子字符串在此字符串中的索引。 

3、int lastIndexOf(String str) ：返回在此字符串中最右边出现的指定子字符串的索引。 

4、int lastIndexOf(String str, int startIndex) ：从指定的索引处开始向后搜索，返回在此字符串中最后一次出现的指定子字符串的索引。 

注意：如果没有找到子字符串，则返回-1。 

如果 startindex 是负数，则 startindex 被当作零。如果它比最大的字符位置索引还大，则它被当作最大的可能索引。 

例如：String s = "xXccxxxXX"; 

// 从头开始查找是否存在指定的字符 //结果如下 

System.out.println(s.indexOf("c")); //2 

// 从第四个字符位置开始往后继续查找，包含当前位置 

System.out.println(s.indexOf("c", 3)); //3 

//若指定字符串中没有该字符则系统返回-1 

System.out.println(s.indexOf("y")); //-1 

System.out.println(s.lastIndexOf("x")); //6 

**11、replace和replaceAll** 

（1）replace的参数是char和CharSequence，即可以支持字符的替换，也支持字符串的替换（CharSequence即字符串序列的意思,说白了也就是字符串）； 

（2）replaceAll的参数是regex，即基于规则表达式的替换，比如：可以通过replaceAll("\\d", "*")把一个字符串所有的数字字符都换成星号； 

相同点：都是全部替换，即把源字符串中的某一字符或字符串全部换成指定的字符或字符串； 

不同点：（1）replaceAll支持正则表达式，因此会对参数进行解析（两个参数均是），如replaceAll("\\d", "*")，而replace则不会，replace("\\d","*")就是替换"\\d"的字符串，而不会解析为正则。 

（2）“\”在java中是一个转义字符，所以需要用两个代表一个。例如System.out.println( "\\" ) ;只打印出一个"\"。但是“\”也是正则表达式中的转义字符，需要用两个代表一个。所以：\\\\被java转换成\\，\\又被正则表达式转换成\，因此用replaceAll替换“\”为"\\"，就要用replaceAll("\\\\","\\\\\\\\")，而replace则replace("\\","\\\\")。 

（3）如果只想替换第一次出现的，可以使用replaceFirst()，这个方法也是基于规则表达式的替换，但与replaceAll()不同的是，只替换第一次出现的字符串。 

说到正则表达式，有个例子就能很好的解释replaceAll的用法。即替换空格 

String test = "wa n\tg_p\\te\\tn　g"; 

test = test.replaceAll("\\t|\\\\t|\u0020|\\u3000", "");//去掉空格 

System.out.println(test); 

其中test = test.replaceAll("\\t|\\\\t|\u0020|\\u3000", "") 

与test = Pattern.compile("\\t|\\\\t|\u0020|\\u3000").matcher(test).replaceAll("") 

是等效的， 

因此用正则表达式仅仅是替换全部或替换第一个的话，用replaceAll或replaceFirst即可。 

**12、getBytes()：得到一个系统默认的编码格式的字节数组** 

都是将一个string类型的字符串转换成byte类型并且存入一个byte数组中。在java中的所有数据底层都是字节，字节数据可以存入到byte数组。 

UTF-8每个汉字转成3bytes，而GBK转成2bytes，所以要说明编码方式，否则用缺省编码。 

String.getBytes(String decode) 

byte[] b_gbk = "中".getBytes("GBK"); 

byte[] b_utf8 = "中".getBytes("UTF-8"); 

byte[] b_iso88591 = "中".getBytes("ISO8859-1"); 

将分别返回"中"这个汉字在GBK、UTF-8和ISO8859-1编码下的byte数组表示,此时 

b_gbk的长度为2, 

b_utf8的长度为3, 

b_iso88591的长度为1。 

new String(byte[], decode)实际是使用指定的编码decode来将byte[]解析成字符串. 

String s_gbk = new String(b_gbk,"GBK"); 

String s_utf8 = new String(b_utf8,"UTF-8"); 

String s_iso88591 = new String(b_iso88591,"ISO8859-1"); 

通过输出s_gbk、s_utf8和s_iso88591,会发现s_gbk和s_utf8都是"中",而只有s_iso88591是一个不被识别的字符（可以理解为乱码）,为什么使用ISO8859-1编码再组合之后,无法还原"中"字？原因很简单,因为ISO8859-1编码的编码表根本就不包含汉字字符,当然也就无法通过"中".getBytes("ISO8859-1");来得到正确的"中"字在ISO8859-1中的编码值了,所以，再通过new String()来还原就更是无从谈起。因此,通过String.getBytes(String decode)方法来得到byte[]时,一定要确定decode的编码表中确实存在String表示的码值,这样得到的byte[]数组才能正确被还原。 

**13、StringBuffer的append方法** 

StringBuffer buf=new StringBuffer("Hard "); 

String aString = "Waxworks"; 

buf.append(aString,3,4); 

原文说明：这个操作将aString的从索引位置3开始的由四个字符组成的子串追加到StringBuffer对象buf中。然后buf对象就会包含字符 串"Hard work"。 

请注意，这个代码的实际运行结果是： buf对象包含的字符串为"Hard w"。 

具体原因引用源代码： 

public synchronized StringBuffer append(CharSequence s, int start, int end) 

{ 

super.append(s, start, end); 

return this; 

} 

根据运行结果分析，StringBuffer对象的append（）方法的参数，如果是String类型，那么，后面取子串的操作实际是从索引3开始，取值到索引4之前的串。如果append的语句改成 buf.append(aString,3,3); ,那么没有添加aString的子串，即 buf包含的字符实际还是"Hard "。如果此语句再改成 buf.append(aString3,2); ，那么系统会抛出"IndexOutOfBoundsException"的异常！ 

但是，如果append()的参数是字符数组（char[])，那么结果就如原文所述，buf将包含串"Hard work". 代码如下： 

StringBuffer buf=new StringBuffer("Hard "); 

char[] text ={'W','a','x','w','o','r','k','s'}; 

buf.append(text ,3,4); // buf包含串"Hard work" 

具体原因引用源代码： 

public synchronized StringBuffer append(char str[], int offset, int len) 

{ 

super.append(str, offset, len); 

return this; 

} 

JAVA 中 Stringbuffer 有append()方法 

　　Stringbuffer其实是动态字符串数组 

　　append()是往动态字符串数组添加，跟“xxxx”+“yyyy”相当那个‘+’号 

　　跟String不同的是Stringbuffer是放一起的 

　　String1+String2 和Stringbuffer1.append("yyyy")虽然打印效果一样，但在内存中表示却不一样 

　　String1+String2 存在于不同的两个地址内存 

　　Stringbuffer1.append(Stringbuffer2)放再一起







# 3 集合API



## 集合体系：









- 20200814



## (一)集合体系API

- 注意：集合体系的对象只能添加对象，不可以添加基本数据类型的数值



- 单个对象存储结构：

- Collection(interface、顶级)

- - List(interface、有序)

  - - ArrayList(class)
    - LinkedList (class)
    - Vector (class)

  - Set(interface、不重复)

  - - HashSet(class)
    - TreeSet (class)



- 键值对存储结构：

- Map(interface、顶级)

- - HashMap(class)
  - TreeMap (class)



- 需要掌握的集合体系包：

- java.util.List（接口）

- - java.util.ArrayList（List接口的实现类）

- java.util.Set（接口）

- - java.util.HashSet（Set接口的实现类）

- java.util.Map（接口）

- - java.util.HashMap（Map接口实现类）



**三种集合的使用方法** 及 说明：

- 说明:创建的集合默认可以存储任何类型的对象、Java建议使用泛型来规定集合中存储的对象类型。

- 使用集合的步骤：

- 1. 导包
  2. 创建对象
  3. 添加对象
  4. 遍历输出集合



**（**1）List集合

- 特点：有序



**步骤一：**

import java.util.List

import java.util.ArrayList



**步骤二：**

List<Man> manlist = new ArrayList<Man>();

Man man1 = new Man();



**步骤三：**

manlist.add(man1);



**步骤四：**

String name = manlist.get(1).getName();

System.out.println(name);

for( Man man : manlist ){

​	System.out.println( man );

}



**（**2）Set集合

- 特点：无序、不重复



**步骤一：**

import java.util.Set

import java.util.HashSet



**步骤二：**

Set<String> set = new HashSet<String>();



**步骤三：**

set.add("a");

set.add("b");

set.add("a");

set.add("b");

- 所有对象不会重复储存

System.***out\***.println(set.add("c"));//输出true

System.***out\***.println(set.add("c"));//输出false，因为有重复值



**步骤四：**

String name = set.get(1).getName();

System.out.println(name);

for( String s : set ){

​	System.out.println( s );

}//输出 abc



**（**3）Map集合（键值对）

- 注意：以键(key)值(value)对的方式来存储数据
- **注意：key是不能重复的!！**
- 说明：键值对: key -> value



**步骤一：**

import java.util.Map

import java.util.HashMap



**步骤二：**

Map<Integer,String> map = new HashMap<Integer,String>();



**步骤三：**

manmap.put(1,”张三”);



**步骤四：**

**获取单个对象：根据**key值获取value值

String value = map.get(3);



**遍历集合：首先要获取**key集合

Set<Integer> keys = map.keySet();

for( int key : keys ){

​	System.out.println( map.get( key ) );

}













# 16 迭代器



**Java List中迭代器遍历：** https://www.cnblogs.com/zhangyue123/p/9286239.html









/**

\* @param args

*/

public static void main(String[] args) {

// TODO Auto-generated method stub





  List<String> list =new ArrayList<String>();

  list.add("a");

  list.add("b");

  list.add("c");

//1:通过索引遍历list

  for(int i=0;i<list.size();i++){

  System.err.println("1:"+list.get(i));  //err：输出换行

  System.out.print("2:"+list.get(i));  //out：输出不换行

  }



//2：迭代器遍历

for(Iterator<String> it=list.iterator();it.hasNext();){

  String str=it.next();

  System.out.println(str);

  it.remove();

}



//while形式





  Iterator<String> i=list.iterator();

  while(i.hasNext()){

  String s=i.next();

  System.out.print(s);

  }

  }



}







# 4 I/O API









## (二)I/O体系API

- I/O概念：文件的 读写、输入输出 体系

- - I、InputStream、读、输入
  - O、OutputStream、写、输出

- Java中通过 数据流、序列化和文件系统 提供系统输入和输出。封装在java.io中

- 注意:IO有打开必须有关闭，关闭顺序和打开顺序逆向

- - 即先关缓存、再关文件读写流，如：

  - - bufferedReader.close()
    - fileReader.close()

- 读、输入操作，导包：

- - import java.io.FileReader;
  - import java.io.BufferedReader;
  - import java.io.IOException;//解决异常报错
  - import java.io.FileNotFoundException;

- 写、输出操作，导包：

- - import java.io.FileWriter;
  - import java.io.BufferedWriter;



**字符流，以字符数组的方式（**char[]）来读写

- java.io.Reader(abstract class、字符输入流)

- - java.io.FileReader(class、文件字符输入流)
  - java.io.BufferedReader(class、缓存输入流)

- java.io.Writer(abstract class、字符输入流)

- - java.io.FileWriter(class、文件输出流)
  - java.io.BufferedWriter(class、缓存输出流)



**字节流，以字节数组的方式（**byte[]）来读写

java.io.InputStream(abstract class、字节输入流)

java.io.OutputStream(abstract class、字节输出流)



## 字符流 读写 步骤：

1. 导包
2. 创建 文件输入、输出流对象
3. 以第二步为构造参数，创建一个缓冲流
4. 对文件进行读写操作
5. 先关闭缓存流，再关闭输入输出流



**（**1）读取、输入 文件例子：

1. 导包

2. - import [java.io](http://java.io).FileReader;
   - import [java.io](http://java.io).BufferedReader;

3. 创建文件输入流（ 参数 是文件的绝对路径，路径太长可以将文件拖进终端，复制出来地址，注意空格）

4. - FileReader f = new FileReader(“文件地址”);//可能会出现异常，鼠标悬停，选第一个

5. 以文件输入流为构造参数创建一个缓冲流(该类提供按行读取的方法)

6. - BufferedReader b = new BufferedReader( f );

7. 使用while循环遍历

8. - String s = "";
   - while( ( s = b.readLine() ) != null ){
   -   System.out.println( s );
   - }

9. 关闭IO流

10. - b.close();
    - f.close();



**（**2）写入、输出 文件例子：

1. 导包

2. - import [java.io](http://java.io).FileWriter;
   - import [java.io](http://java.io).BufferedWriter;

3. 创建文件输出流

4. - FileWriter f = new FileWriter(“文件地址”);

   - 注意：一个参数 表示每次都是重新写整个文件，如果想继续在文件末尾输出，需要两个参数的构造方法，如下：

   - - FileWriter f = new FileWriter(“文件地址” , true);

5. 创建缓存流

6. - BufferedWriter b = new BufferedWriter( f );

7. 向文件输出

8. - b.write( “你好\n“ );
   - b.write( “这是向文件输出的第二条数据“ );

9. 关闭IO流

10. - b.close();
    - f.close();







# 5 异常API





参考： https://blog.csdn.net/michaelgo/article/details/82790253

![20180920165502957.png](/blob:file:/b05dcae6-84f0-48ed-99d0-f2e05e1d9f37)

 

如何优雅的处理异常 https://www.zhihu.com/question/28254987





# (三)异常体系API

- 理解：异常就是代码的错误，异常是一种错误处理机制，会告诉我们 哪个类 哪一行出了什么问题
- 注意：异常只是一种帮助我们查找错误原因的机制而且、并不能帮我们去修改错误



## (01)常见的异常：

- java.lang.ArithmeticException
- java.lang.ArrayIndexOutOfBoundsException
- java.lang.NullPointerException
- java.lang.NumberFormatException
- java.lang.ClassCastException
- java.text.ParseException
- java.io.FileNotFoundException





## (02)处理异常的方式

- 异常的两种处理方式

- - 方式一：捕获异常、try关键字、catch关键字、finally关键字
  - 方式二：抛出异常、throws关键字





## (03)异常体系的每个类都是具体类、每个类都可以创建对象

- Throwable(顶级)

- - Error(错误类、Java本身的问题、我们处理不了的问题、java虚拟机、内存泄漏等)

  - Exception(异常类)

  - - RuntimeExcetion(运行时异常、非检查型异常、非强制处理的异常)
    - 其它所有子类(检查型异常、必须要处理的异常、否则不行运行)





## (04)异常体系的常见例子

- (1)-(5)这些异常有个共同的特点：编写时无错误提示，运行时才报错
- 6、7在编写代码时 就提示有可能会 出错

​		

**(1)**算数异常：

**java.lang.ArithmeticException**

System.out.println(2 / 0);

​		

**(2)** 数组下标越界异常：java.lang.ArrayIndexOutOfBoundsException 

int[] a = {1,2};

System.out.println(a[2]);

​		

**(3)** 空指针异常

**java.lang.NullPointerException**

String s = null;

System.out.println(s.charAt(2));

​		

**(4)**数字转换异常

**java.lang.NumberFormatException**

String s = "你好";

int i = Integer.parseInt(s);

System.out.println(i);

​		

**(5)**类型转换异常

**java.lang.ClassCastException**

Integer i = 10;

Object o = i;

Date a = (Date)o;

System.out.println(a);

​		

- 注意：(6)-(7)在编写代码的时候就提示有可能出错，必须处理的异常。



 **(6)** 字符串 转换 日期：

 日期解析异常：

**java.text.ParseException: Unparseable date**

String s = "2020";

SimpleDateFormat f = new SimpleDateFormat("yyyy-MM-dd");

//Date d = f.parse(s); //鼠标悬停，选第二个，生成下面的代码⬇️

try {

​	Date d = f.parse(s);

} catch (ParseException e) {

​	e.printStackTrace();

}

​		

 **(7)**文件找不到异常：

**java.io.FileNotFoundException**

try {

​	FileReader f = new FileReader("d:/abc.txt");

} catch (FileNotFoundException e) {

​	e.printStackTrace();

}//没有abc.txt文件





**(6)-(7)**两个异常可以一起捕获



try {



​	String s = "2020年11月11日";

​	SimpleDateFormat f = new SimpleDateFormat("yyyy年MM-dd");



​	Date d = f.parse(s);

​	FileReader f2 = new FileReader("d:/abc.txt");



} catch (FileNotFoundException e) {

​	e.printStackTrace();

} catch (ParseException e) {

​	e.printStackTrace();

}

​	

##  

## (08)异常的两种处理方式以及关键字

- 判定标准：

- - 当写方法的人 写的实现的代码 的问题，建议 捕获异常，如：

  - - 在写方法时，方法体内出错误了

  - 方法本身没有问题，调用方法 的人出了问题，建议 抛出异常，如：

  - - 在调用时出错，比如参数写错时，在当前方法的定义处 定义抛出异常即可

- 合并捕获异常：

- - 选中多个可能有异常的语句块
  - 右键
  - Surround With
  - Try/catch Block



**（**1）捕获异常（鼠标悬停，选第二个）

- 说明：当写方法的人出的代码问题，建议捕获。方法内部具体实现的问题。	

- 关键字：

- - try：用来包含有可能出问题的代码
  - catch：当有异常产生时，会执行此语句块并打印异常信息，没有错的时候不执行
  - finally：有没有异常，都执行的语句块

- 代码出现异常的执行原理：

- - 当某一行代码出现异常、代码会立刻终止、并抛出异常



**捕获异常例子：**person.txt文件不存在

try {

​	System.out.println(111);//正常运行

​	FileReader f = new FileReader("d:/person.txt");

​	System.out.println(222);//不会运行

} catch (FileNotFoundException e) {

​	System.out.println("抛出异常”);//正常运行

​	e.printStackTrace();//正常运行

} finally {

​	System.out.println("不论是否有异常都一定会执行的代码块");//正常运行

}



**（**2）抛出异常（鼠标悬停，选第一个）

- 说明：方法本身没有问题，调用方法的人出了问题，建议抛出异常。
- throws关键字：写在调用错的方法的定义处、表示抛出异常的意思、抛给方法的调用者



**抛出异常例子：**person.txt文件不存在

public static void m1(String filename) throws FileNotFoundException {

​		FileReader f = new FileReader(filename);

}

m1("d:/person.txt”);









# 6 Calendar API



参考： https://blog.csdn.net/ytasdfg/article/details/81086118









## （6）Calendar

- Calendar类时一个抽象类，在实际使用中，需要用到子类的getInstance方法创建对象



// 创建对象

Calendar c1 = Calendar.getInstance();

// 获取月份

int month = c1.get(Calendar.MONTH) + 1;

// 获取日期

int date = c1.get(Calendar.DATE);

// 获取小时

Int hour = c1.get(Calendar.HOUR_OF_DAY);

// 获取分钟

Int minute = c1.get(Calendar.MINUTE);

// 获取星期（与Date类不同：1代表星期日，2代表星期一，以此类推）

int day = c1.get(Calendar.DAY_OF_WEEK);











​		*//* 其日历字段已由当前日期和时间初始化：

​		
 
 	Calendar rightNow = Calendar.getInstance(); *//* 子类对象

​		
 
 	*//* 获取年

​		
 
 	int year = rightNow.get(Calendar.YEAR);

​		
 
 	*//* 获取月

​		
 
 	int month = rightNow.get(Calendar.MONTH);

​		
 
 	*//* 获取日

​		
 
 	int date = rightNow.get(Calendar.DATE);

​		
 
 	*//*获取几点

​		
 
 	int hour=rightNow.get(Calendar.HOUR_OF_DAY);

​		
 
 	*//*获取上午下午

​		
 
 	int moa=rightNow.get(Calendar.AM_PM);

​		
 
 	if(moa==1)

​		
 
 		System.out.println("下午");

​		
 
 	else

​		
 
 		System.out.println("上午");

​		
 
 

​		
 
 	System.out.println(year + "年" + (month + 1) + "月" + date + "日"+hour+"时");

​		
 
 	rightNow.add(Calendar.YEAR,5);

​		
 
 	rightNow.add(Calendar.DATE, -10);

​		
 
 	int year1 = rightNow.get(Calendar.YEAR);

​		
 
 	int date1 = rightNow.get(Calendar.DATE);

​		

 	System.out.println(year1 + "年" + (month + 1) + "月" + date1 + "日"+hour+"时");











# 7 反射API



https://blog.csdn.net/u014199143

上面的博客中的：

https://blog.csdn.net/u014199143/article/details/80456267





- 定义：在运行状态中，对任意一个类，都能知道这个类的所有成员；对于一个对象，能够调用它的任意一个方法和属性；这些动态获取信息及动态调用对象的功能称为Java语言的反射机制
- 想要了解一个类，必须获取该类的字节码文件对象。这样解剖的功能由Class类中的方法提供。所以先要获取到每个字节码文件对应的Class类型的对象
- 简单说：反射就是Java将工程中各个成分都映射成对象，需要时什么信息都能得到，最常见的使用 就是开发工具中代码提示
- 如：一个类有成员变量、成员方法、构造方法、依赖包等信息，利用反射可以将这个类的各个信息取到
- 下图是类的一般加载过程：反射的原理在于Class对象

![20170513133210763.png](/blob:file:/3c8aa399-35dd-4887-8374-f6c09e4f1bdb)

- 可见，Class是一个特殊的对象，了解它对理解反射机制很重要



## Class类在Java中的api详解（11JDK中）



**模块** [java.base](itss://chm/java.base/module-summary.html)

**软件包** [java.lang](itss://chm/java.base/java/lang/package-summary.html)

**Class Class<T>**

- [java.lang.Object](itss://chm/java.base/java/lang/Object.html)

- - java.lang.Class<T>

- **参数类型 
  ** T - 此类对象建模的类的类型。 例如， String.class的类型是Class<String> 。 如果正在建模的类未知，请使用Class<?> 。 
   
   **实现的所有接口 
  ** [Serializable](itss://chm/java.base/java/io/Serializable.html) ， [AnnotatedElement](itss://chm/java.base/java/lang/reflect/AnnotatedElement.html) ， [GenericDeclaration](itss://chm/java.base/java/lang/reflect/GenericDeclaration.html) ， [Type](itss://chm/java.base/java/lang/reflect/Type.html) 
   
   
   public final class **Class<T>**

- extends [Object](itss://chm/java.base/java/lang/Object.html)

implements [Serializable](itss://chm/java.base/java/io/Serializable.html), [GenericDeclaration](itss://chm/java.base/java/lang/reflect/GenericDeclaration.html), [Type](itss://chm/java.base/java/lang/reflect/Type.html), [AnnotatedElement](itss://chm/java.base/java/lang/reflect/AnnotatedElement.html)
 类类实例表示正在运行的Java应用程序中的类和接口。 枚举类型是一种类，注释类型是一种接口。 每个数组也属于一个类，该类反映为类对象，由具有相同元素类型和维数的所有数组共享。 原始Java类型（ boolean ， byte ， char ， short ， int ， long ， float ，和double ），以及关键字void也表示为类对象。 类没有公共构造函数。 而是当类加载器调用[defineClass](itss://chm/java.base/java/lang/ClassLoader.html#defineClass(java.lang.String,byte[],int,int))方法之一并传递class文件的字节时，Java虚拟机会自动构造类对象。 
 **类类的方法暴露了类或接口的许多特征。 大多数特性派生自类加载器传递给Java虚拟机的class文件。** 一些特性由运行时的类加载环境决定，例如getModule()返回的模块。 
 类类某些方法公开Java源代码中的类或接口的声明是否包含在另一个声明中。 其他方法描述了类或接口如何位于嵌套中 。 nest是一组类和接口，在同一运行时包中，允许相互访问其private成员。 类和接口称为*nestmates* 。 一个巢穴充当巢主 ，并列举属于巢的其他巢穴; 它们中的每一个又将其记录为嵌套主机。 属于嵌套的类（包括其主机）的类和接口是在生成class文件时确定的，例如，Java编译器通常会将顶级类记录为嵌套的主机，其中其他成员是类，声明包含在顶级类声明中的接口。 
 以下示例使用类对象来打印对象的类名： 

   void printClassName(Object obj) {

​     System.out.println("The class of " + obj + " is " + obj.getClass().getName());

   }
 
 也可以使用类文字为指定类型（或void）获取类对象。 参见*The Java™ Language Specification*的第15.8.2节。 例如： 
 System.out.println("The name of class Foo is: "+Foo.class.getName()); 
 
 **从以下版本开始： 
** 1.0





## Class类说明：

- Class 没有公共构造方法。Class 对象是在加载类时由 Java 虚拟机以及通过调用类加载器中的defineClass 方法自动构造的。
- Class类的方法众多，60多个吧，大部分都是用来获取当前类的信息的

![20170513144141409.png](/blob:file:/6b11b9c4-6890-4168-9bff-039d3bacc112)





## 反射的使用：

**（**1）获取Class对象的三种方式

1. Object -> getClass();
2. 任何数据类型（基本类型和类类型）都有一个“静态”的class属性
3. 通过Class类的静态方法：forName(String className)（常用）



**通过实例说明：**



package test;



public class Test {

​	public static void main(String[] args) {



​		// 第一种方式获取Class对象

​		// 该new操作生成了一个Student对象，一个Class对象

​		Student s1 = new Student();



​		// 获取Class对象，并打印出来

​		Class sClass = s1.getClass();

​		System.out.println(sClass.getName());





​		// 第二种方式获取Class对象

​		Class sClass2 = Student.class;

​		

​		// 判断第一种方式获取的Class对象和第二种方式获取的是否为同一个

​		System.out.println(sClass == sClass2);





​		// 第三种方式获取Class对象

​		try {

​			// 注意此字符串必须是真实路径，即包名.类名

​			Class sClass 3 = Class.forName("bean.Student");

​			// 判断三种方式获取的是否为同一个Class对象

​			System.out.println(sClass3 == sClass2);

​		} catch (ClassNotaFoundException e) {

​			e.printStachTrace();

​		}

​		

​	}

}



## 注意：在运行期间，一个类，只有一个Class对象产生！！

## 说明：三种方式常用第三种，第一种都有对象了，还要反射作甚？第二种需要导入 类的包，依赖太强，不导包就抛编译错误。一般用第三种，字符串可以传入，也可写在配置文件中等多种方法





**（**2）通过反射获取构造方法并使用



**在**Student类中写好一些构造方法：



 //---------------构造方法-------------------

  //（默认的构造方法）

  Student(String str){

​    System.out.println("(默认)的构造方法 s = " + str);

  }



  //无参构造方法

  public Student(){

​    System.out.println("调用了公有、无参构造方法执行了。。。");

  }



  //有一个参数的构造方法

  public Student(char name){

​    System.out.println("姓名：" + name);

  }



  //有多个参数的构造方法

  public Student(String name ,int age){

​    System.out.println("姓名："+name+"年龄："+ age);//这的执行效率有问题，以后解决。

  }



  //受保护的构造方法

  protected Student(boolean n){

​    System.out.println("受保护的构造方法 n = " + n);

  }



  //私有构造方法

  private Student(int age){

​    System.out.println("私有的构造方法  年龄："+ age);

  }





**测试类：**



/*

 \* 通过Class对象可以获取某个类中的：构造方法、成员变量、成员方法；并访问成员；

 \* 

 \* 1.获取构造方法：

 \*   1).批量的方法：

 \*     public Constructor[] getConstructors()：所有"公有的"构造方法

​      public Constructor[] getDeclaredConstructors()：获取所有的构造方法(包括私有、受保护、默认、公有)



 \*   2).获取单个的方法，并调用：

 \*     public Constructor getConstructor(Class... parameterTypes):获取单个的"公有的"构造方法：

 \*     public Constructor getDeclaredConstructor(Class... parameterTypes):获取"某个构造方法"可以是私有的，或受保护、默认、公有；

 \*    

 \*     调用构造方法：

 \*     Constructor-->newInstance(Object... initargs)

 */



public class Constructors {



  public static void main(String[] args) throws Exception {

​    //1.加载Class对象

​    Class clazz = Class.forName("fanshe.Student");、



​    //2.获取所有公有构造方法

 System.out.println("**********所有公有构造方法**********");

​    Constructor[] conArray = clazz.getConstructors();

​    for(Constructor c : conArray){

​      System.out.println(c);

​    }



 System.out.println("**********所有的构造方法(包括：私有、受保护、默认、公有)**********");

​    conArray = clazz.getDeclaredConstructors();

​    for(Constructor c : conArray){

​      System.out.println(c);

​    }



​    System.out.println("**********获取公有、无参的构造方法**********");

​    Constructor con = clazz.getConstructor(null);

​    //1>、因为是无参的构造方法所以类型是一个null,不写也可以：这里需要的是一个参数的类型，切记是类型

​    //2>、返回的是描述这个无参构造函数的类对象。

​    System.out.println("con = " + con);



​    //调用构造方法

​    Object obj = con.newInstance();

​    System.out.println("调用了公有、无参构造方法执行了。。。");



  // System.out.println("obj = " + obj);

  // Student stu = (Student)obj;



 System.out.println("**********获取私有构造方法，并调用**********");

​    con = clazz.getDeclaredConstructor(char.class);

​    System.out.println(con);



​    //调用构造方法

​	// 暴力访问(忽略掉访问修饰符)

​    con.setAccessible(true);

​    obj = con.newInstance('男');

​	System.out.println( "姓名:" + obj.getSex() );

  }



}





**输出结果：**



**********所有公有构造方法**********

public fanshe.Student(java.lang.String,int)

public fanshe.Student(char)

public fanshe.Student()

**********所有的构造方法(包括：私有、受保护、默认、公有)**********

private fanshe.Student(int)

protected fanshe.Student(boolean)

public fanshe.Student(java.lang.String,int)

public fanshe.Student(char)

public fanshe.Student()

fanshe.Student(java.lang.String)

**********获取公有、无参的构造方法**********

con = public fanshe.Student()

调用了公有、无参构造方法执行了。。。

**********获取私有构造方法，并调用**********

public fanshe.Student(char)

姓名：男





**获取构造方法的方法说明：**



 1).批量的方法：

public Constructor[] getConstructors()：所有”公有的”构造方法

​      public Constructor[] getDeclaredConstructors()：获取所有的构造方法(包括私有、受保护、默认、公有)

   

 2).获取单个的方法，并调用：

public Constructor getConstructor(Class… parameterTypes):获取单个的”公有的”构造方法：

public Constructor getDeclaredConstructor(Class… parameterTypes):获取”某个构造方法”可以是私有的，或受保护、默认、公有；



 调用构造方法：

Constructor–>newInstance(Object… initargs)



2、 newInstance是 Constructor类的方法（管理构造函数的类）

api的解释为：

newInstance(Object… initargs)

​      使用此 Constructor 对象表示的构造方法来创建该构造方法的声明类的新实例，并用指定的初始化参数初始化该实例。

它的返回值是T类型，所以newInstance是创建了一个构造方法的声明类的新实例对象。并为之调用





**（**3）获取成员变量并调用



**Student**类中：



  public Student(){



  }

  //**********字段*************//

  public String name;

  protected int age;

  char sex;

  private String phoneNum;



  @Override

  public String toString() {

​    return "Student [name=" + name + ", age=" + age + ", sex=" + sex

​        \+ ", phoneNum=" + phoneNum + "]";

  }





**测试类中：**



​    public static void main(String[] args) throws Exception {



​      //1.获取Class对象

​      Class stuClass = Class.forName("fanshe.field.Student");





​      //2.获取字段

​      System.out.println("===获取所有公有的字段===");

​      Field[] fieldArray = stuClass.getFields();

​      for(Field f : fieldArray){

​        System.out.println(f);

​      }

   



​		System.out.println("===获取所有的字段(包括私有、受保护、默认的)===");

​      fieldArray = stuClass.getDeclaredFields();

​      for(Field f : fieldArray){

​        System.out.println(f);

​      }





​      System.out.println("===获取公有字段，并调用===");

​      Field f = stuClass.getField("name");

​      System.out.println(f);



​      //获取一个对象

​		//产生Student对象，等同：Student stu = new Student();

​		Object obj = stuClass.getConstructor().newInstance();

​		

​      //为字段设置值

​		//为Student对象中的name属性赋值--》stu.name = "刘德华"

​      f.set(obj, "刘德华");



​      //验证

​      Student stu = (Student)obj;

​      System.out.println("验证姓名：" + stu.name);





  		System.out.println("===获取私有字段，并调用===");

​      f = stuClass.getDeclaredField("phoneNum");

​      System.out.println(f);



​		//暴力反射，解除私有限定

​      f.setAccessible(true);

​      f.set(obj, "18888889999");

​      System.out.println("验证电话：" + stu);



​    }





后台输出：



===获取所有公有的字段===

public java.lang.String fanshe.field.Student.name

===获取所有的字段(包括私有、受保护、默认的)===

public java.lang.String fanshe.field.Student.name

protected int fanshe.field.Student.age

char fanshe.field.Student.sex

private java.lang.String fanshe.field.Student.phoneNum

===获取公有字段，并调用===

public java.lang.String fanshe.field.Student.name

验证姓名：刘德华

===获取私有字段，并调用

private java.lang.String fanshe.field.Student.phoneNum

验证电话：Student [name=刘德华, age=0, sex=,





由此可见

调用字段时：需要传递两个参数：



//产生Student对象–》Student stu = new Student();

Object obj = stuClass.getConstructor().newInstance();//为字段设置值



//为Student对象中的name属性赋值–》stu.name = “刘德华”

f.set(obj, “刘德华”);



第一个参数：要传入设置的对象，第二个参数：要传入实参





**（**4）获取成员方法并调用



**（**5）反射main方法



**（**6）反射方法的其它使用之—通过反射运行配置文件内容



**（**7）反射方法的其它使用之—通过反射越过泛型检查

























# 8 封装类API





##  (07)封装类java.lang.Integer

- 字符串和基本数据类型的相互转换
- 基本数据类型转换为字符串：String.valueOf(基本数据类型)

**基本数据类型** 转 字符串 例子：

- 通过valueOf()方法将基本数据类型转换为字符串对象：

int a = 3;

String s = String.valueOf(a);



**字符串** 转为 基本数据类型 例子：

- 用基本数据类型所对应的类类型parse方法转换

String str = "12";

int b = Integer.parseInt(str);

double x = Double.parseDouble("-12.34");



## 说明：

八种基本数据类型和对应的封装类有【自动装箱拆箱原理】、可以相互自动转换

## 举例：

- Integer b = 2;

- - 装箱过程：自动把int类型的值封装为Integer类型的对象

- int c = b;

- - 拆箱过程：自动把Integer类型对象还原为int类型的值









# 9 日期API







##  （5）日期java.util.Date、日期转换java.text.SimpleDateFormat

- Date表示日期时间类
- SimpleDateFormat表示 日期类型 和 字符串类型 转换的一个类
- 说明：String	 <->	SimpleDateFormat	<->	Date



**(1)**日期转换为字符串的方式：

- 创建日期对象：

- - Date date = new Date();

- 创建日期排版对象：

- - SimpleDateFormat s = new SimpleDateFormat("yyyy-MM-dd hh:mm:ss");

- 通过format方法，将日期转换成字符串

- - String str = s.format(date);



**(2)**字符串转换为日期的方式：

- 创建字符串：

- - String str2 = "2019年11-11";

- 注意：日期格式必须和字符串格式一致、否则转换会报错

- 创建日期排版对象：

- - SimpleDateFormat s2 = new SimpleDateFormat("yyyy年MM-dd");

- 通过parse()方法，将字符串转换成日期对象

- - Date date2 = s2.parse(str2);// 异常需要处理，鼠标悬停，选择抛出异常









# 999 Java 成体系API





获取操作系统名： https://blog.csdn.net/yin__ren/article/details/103410884



## 补充：集合和数组区别

- 区别一:数组是固定长度的结构。集合是动态长度的结构。 （推荐用集合）
- 区别二:数组可以存储 基本数据类型 和 类类型。集合只能存储 类类型的对象。



**（**1）数组 既可以存 基本数据类型 又可以存 对象类型

- 创建数组方式一

int[] a = {1, 2, 3};

- 创建数组方式二:3表示数组的长度

int[] b = new int[3];

数组存对象类型：String[] c = new String[3];



**（**2）集合 只存 对象

- 原理：基本数据类型的封装类自动装箱拆箱原理

- - int(2) -> 自动装箱 -> Integer(2) -> 存入集合
  - Integer(2) -> 自动拆箱 -> int(2) -> 遍历集合

**例子：**

List<Integer> list = new ArrayList<Integer>();

list.add(2);

list.add(4);

for (int i:list) {

​	System.out.println(i);

}

​		



# 1 Java特征

20200813

- 面向对象语言的三大 特征 ：**封装性、继承性、多态性**
- 具体类、抽象类、接口：都有封装性 和 继承性
- 多态性指的是**方法的多态**



## (01) 封装思想

- 概念：把 相关的变量和方法 封装在 类内部，既{ }

- - 相关的变量可能包括其他类对象
  - 比如：公司类里封装了一个员工集合

- 好处：更适合现实需求，让我首先关注类本身

- 理解：本质是，根据实际需求，在开发第一步，先用Java语言把现实生活中的场景建模出来（分析、设计）。

- 封装类的作用：

- - 能够 把字符串 转换为 基本数据类型
  - 能够 让集合 存储 基本数据类型



## (02)继承思想

- 概念：子类使用extends关键字 继承 父类，父类的所有成员，子类都有

- 特征：这些子类，都有相同的属性，满足“是一个”的原则

- - 如：猫是一个动物，狗是一个动物，就可以使用继承，先写一个动物的抽象类，让猫类和狗类继承

- 好处：父类的代码子类都有、设计统一标准。便于设计与管理

- 提示：写抽象类的目的就是为了继承，没有被继承的抽象类就没用。

- 注意：父类中的成员 是 所有子类都共有的成员。

- 注意：如果不用继承、这些子类都是各自独立编写的，不便于设计和管理

- 注意：如果使用继承，就是用父类去管理子类。是项目经理管理组员的工具。







##  (03-1) 多态思想说明

- **注意：子类覆写了的话，自动调用子类实现的方法**

- 概念：多种形态，不论实现什么功能，都给用户提供多种选择和多种形态，多种选择就是重写，多种形态就是重载

- - 重载可以使同一个功能有多种形态
  - 重写可以使同一个功能在不同的子类中体现出更多的选择

- 好处：同一个功能（方法）有更多的选择及更多的形态，便于用户的使用，减少设计、管理及实现的成本。

##  

## (03-2) 多态中的 两种多态（重载和重写）

- 类内部的多态：又叫做**重载**，在一个类的内部，有多个方法，同名，但不同参数列表。既 参数的 个数、类型、顺序 不同，就是重载。重载方法的返回值 和 权限修饰符 可以相同也可以不同。

- - 特征：

  - 1. 同一内部的多个方法
    2. 同名
    3. 参数列表、返回值、权限有不同

  - 好处：方法名相同，说明实现的是同一种功能，这一种功能可以完成多种参数需求，可以通过多种方式完成一个功能

  - 重载发生在编译时

  - 例子：构造方法的有参无参，输出方法(syso)可以输出不同类型，两个数相加或者三个数相加

- 继承中的多态：又叫做**覆写、重写**，在父类和子类中，有2个方法的方法定义完全相同，会自动调用子类的方法，即指子类重写父类的方法，返回值类型、方法名、参数列表 都必须一样

- - 特征：

  - 1. 继承中的两个方法
    2. 返回值、方法名、参数列表相同
    3. 方法体不同

  - 好处：一个父类(定标准)、相同功能、子类越多、选择越多、标准都相同。

  - 子类重写方法的 抛出异常的范围 必须小于等于 父类中被重写的方法；

  - 子类重写方法的 权限修饰符范围 必须大于等于 父类中被重写的方法；

  - 若父类中的方法的权限修饰符为 private，那子类就不能重写该方法；

  - 注意： 构造器不能被重写，但是可以重载。

  - 例子：toString方法（会有@Override重写注解）

  - 1. toString方法是顶级父类Object类中定义的方法
    2. 默认打印的是"包名.类名@哈希值"
    3. 哈希值是每个对象的唯一标识、可以理解为地址

- 提示：

- - 接口中多态：一个接口有多个实现类，也是多态的思想。





有时间再看看 苹果电脑 eclipsse 里的 0812 的三个练习！！！！！



