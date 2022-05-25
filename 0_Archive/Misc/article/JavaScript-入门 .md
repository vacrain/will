

## 一、介绍

> 所有技术

### 1. 科班/工作必会内容

#### 1.1 <u>一句话概括，它是什么？</u>

:raised_hands: **​Javascript**是一种**脚本语言**，**弱类型语言**

#### 1.2 <u>行话、术语有哪些？都是什么意思？</u>

> ​	每篇文章下的该部分内容会持续更新，想起来了什么相关的，我就再加上~（建议收藏:star:）

:point_right: **脚本**

​	要想理解脚本语言是什么，要先说一下**脚本**这个词，这个还真查过，不是个外来语，记得早在宋朝就有这个词了，背不太好本意，偷偷搬一下百度百科~如下：

> ​	脚本是指表演戏剧、拍摄电影等所依据的底本又或者书稿的底本。脚本可以说是故事的发展大纲，用以确定故事的发展方向。之后，确定故事到底是在什么地点，什么时间，有哪些角色，角色的对白，动作，情绪的变化，等等，这些细化的工作都是剧本上所要清楚确定下来的。

​	emmm...有点啰嗦，简单说就是一个剧本的具体实施步骤，比如：（可以联想一下打开网站，页面一点点从服务器取数据，并渲染到浏览器内存，最后显示出来）

1. 第一步打光
2. 第二步主角登场
3. 第三步反派登场
4. 第四步反派嗝屁。。。  

​	也可能会有突发事件，不过也在脚本上有写，比如：张三如果突然上场了的话，李四就耍个刀给他赶下来...（可以联想一下，点击了不好用的超链接，弹出了一个窗口）

:point_right: ​**脚本语言**

​	根据上面对**脚本**的描述应该就很好理解脚本语言了，既然是**戏剧**，那就要有**舞台**（浏览器），要有**演员**（HTML元素、缓存中的变量），在这个舞台上，按照脚本（JavaScript写的程序），一步一步的推进剧情（执行脚本程序）。

​	**舞台**不光只有**浏览器**，**脚本语言**也不止有**JavaScript**。比如在windows系统下，我们计科相关专业的基操：win+R，之后cmd，回车！然后打开黑本窗口（终端），这个软件叫操作系统的shell（壳子），里面我们用的各种命令（也可以叫指令）也是脚本语言。

​	脚本语言的初衷还是为了较少程序运行需要的步骤（编译-链接-运行），我总喜欢拿洗衣机举例子（洗衣机真是太好用了八，谁发明的，还能用在这...）用脚本语言写的程序（注意断句），就像是按照步骤，按洗衣机上的按钮。而不需要，当我们想来个浸泡洗模式、水位7、力度中时，还要现拼装**特定模式、水位、力度的零件**（编写对应的底层程序），**安装到洗衣机里**（编译），**插电**（运行）。不过脚本语言一般较为灵活，常见的就是我们总要cmd一下（不是电脑出问题，就是软件没安明白。。）

:point_right: ​**弱类型语言**

​	说它弱，那肯定是相对强才叫弱。先说一下**强类型语言**~

> 强类型语言：是一种**强制类型定义**的语言，一旦某一个变量被定义类型，如果不经过强制转换，则它永远就是该数据类型了，强类型语言包括Java、.net 、Python、C++等语言。

​	相对上面的描述，弱类型语言就是不强制类型的定义，声明时也不需要确定类型，在第一次赋值的时候系统会确定类型，下面用Java做一个简单的对比，分别声明一个整型变量和字符串，来感受一下：

​	Java（强类型语言）：

```java
// 声明时就必须固定数据类型，不这么做就运行不了程序
int i = 123;// i现在就是int类型
String j = "abc";// j现在就是String类型
```

​	JavaScript（弱类型语言）：

```javascript
var i,j;// 声明变量时，可以不赋值，也不强制固定数据类型，在后续赋值时再确定数据类型~
i = 123;// i变成了Number类型的变量
j = 'abc';// j变成了String类型的了
```

​	（后面这些术语、行话后，续填坑~）

:point_right: ​**事件**



:point_right: ​**函数**

:point_right: ​**外部方法**

:point_right: ​**JSON**

:point_right: ​**DOM**

:point_right: ​**遍历**

:point_right: ​**注释**

:point_right: ​**ES6**



#### 1.3 <u>语言基础语法知识有哪些？</u>

> ​	一般我们学习一个新的语言时都要默默的问一下这些问题：文件格式是什么？大小写是否敏感？注释方法是什么？有哪些基本数据类型？运算符有哪些？流程控制语句怎么写？变量怎么声明并使用？方法或函数怎么声明并使用？主方法或主函数怎么写？如何编写并运行一个简单的程序？...

:star2: **文件格式**：.js

:star2: ​对大小写**敏感**

:star2: ​**单行注释方法**：

```javascript
// 注释内容
```

:star2: ​**多行注释方法**：

```javascript
/*
	注
	释
	内
	容
*/
```
:star2: ​**基本数据类型：**

| 类型说明 | 举例               | 数据类型  |
| -------- | ------------------ | --------- |
| 字符串   | '123abc'           | String    |
| 数字     | 0.01或123          | Number    |
| 布尔     | true/false         | Boolean   |
| 对象     | {name:'张三'}/null | Object    |
| 未定义   | undefined/var un;  | Undefined |

:star2: ​**运算符：**

1. 算数运算符：+、-、*、/、%
2. 比较运算符：>、>=、<、<=、==、!=
3. 逻辑运算符：&&、||、!
4. 赋值运算符：+=、-=、*=、/=、%=、=
5. 自增自减运算符：++、--
6. 三目运算符：? :

:star2: ​**流程控制语句**：这部分重写

1. if分支语句：if(条件) { // 语句块 } else { // 语句块 }
   1. if、else、elseif
   2. 有else、elseif必须有if，有if可以没有else
2. for循环语句：for( item in list ){ // 语句块 }、if(i = 0;i<10;i++) { // 语句块 }
   1. in 可以依次取出元素的下标
   2. of  可以依次取出元素

#### 1.4 <u>现在的流行版本？有哪些新增特性？</u>

:muscle: ​**流行版本**：ES6

:sparkles: **新特性：**

- const与let声明方式
- 模板字面量
- 解构
- 对象字面量简写法
- for...of循环
- 展开运算符
- 剩余参数（可变参数）
- ES6箭头函数
- JS标准函数this
- 箭头函数和this
- 默认值和解构
- 默认参数函数
- JS类
- super和extends
- Promise对象

### 2. 其他了解

> ​	多了解点，学的更明白，以后也好和同行或外行唠嗑（吹:cow::beer:）~

#### 2.1 <u>为什么会出现？</u>

1994年，网景公司（Netscape）发布了Navigator浏览器0.9版。这是历史上第一个比较成熟的网络浏览器，轰动一时。但是，这个版本的浏览器只能用来浏览，不具备与访问者互动的能力。比如，如果网页上有一栏"用户名"要求填写，浏览器就无法判断访问者是否真的填写了，只有让服务器端判断。如果没有填写，服务器端就返回错误，要求用户重新填写，这太浪费时间和服务器资源了。

因此，网景公司急需一种网页脚本语言，使得浏览器可以与网页互动。工程师Brendan Eich负责开发这种新语言。他觉得，没必要设计得很复杂，这种语言只要能够完成一些简单操作就够了，比如判断用户有没有填写表单。送

1994年正是面向对象编程（object-oriented programming）最兴盛的时期，C++是当时最流行的语言，而Java语言的1.0版即将于第二年推出，Sun公司正在大肆造势。

Brendan Eich无疑受到了影响，Javascript里面所有的数据类型都是对象（object），这一点与Java非常相似。但是，他随即就遇到了一个难题，到底要不要设计"继承"机制呢？

**Brendan Eich的选择**

如果真的是一种简易的脚本语言，其实不需要有"继承"机制。但是，Javascript里面都是对象，必须有一种机制，将所有对象联系起来。所以，Brendan Eich最后还是设计了"继承"。

但是，他不打算引入"类"（class）的概念，因为一旦有了"类"，Javascript就是一种完整的面向对象编程语言了，这好像有点太正式了，而且增加了初学者的入门难度。

他考虑到，C++和Java语言都使用new命令，生成实例。

C++的写法是：

> 　　ClassName *object = new ClassName(param);

Java的写法是：

> 　　Foo foo = new Foo();

因此，他就把new命令引入了Javascript，用来从原型对象生成一个实例对象。但是，Javascript没有"类"，怎么来表示原型对象呢？

这时，他想到C++和Java使用new命令时，都会调用"类"的构造函数（constructor）。他就做了一个简化的设计，在Javascript语言中，new命令后面跟的不是类，而是构造函数。

举例来说，现在有一个叫做DOG的构造函数，表示狗对象的原型。

> 　　function DOG(name){
>
> 　　　　this.name = name;
>
> 　　}

对这个构造函数使用new，就会生成一个狗对象的实例。

> 　　**var dogA = new DOG('大毛');**
>
> 　　alert(dogA.name); // 大毛

注意构造函数中的[this关键字](http://www.ruanyifeng.com/blog/2010/04/using_this_keyword_in_javascript.html)，它就代表了新创建的实例对象。

**三、new运算符的缺点**

用构造函数生成实例对象，有一个缺点，那就是无法共享属性和方法。

比如，在DOG对象的构造函数中，设置一个实例对象的共有属性species。

> 　　function DOG(name){
>
> 　　　　this.name = name;
>
> 　　　　**this.species = '犬科';**
>
> 　　}

然后，生成两个实例对象：

> 　　var dogA = new DOG('大毛');
>
> 　　var dogB = new DOG('二毛');

这两个对象的species属性是独立的，修改其中一个，不会影响到另一个。

> 　　**dogA.species = '猫科';**
>
> 　　alert(dogB.species); // 显示"犬科"，不受dogA的影响

每一个实例对象，都有自己的属性和方法的副本。这不仅无法做到数据共享，也是极大的资源浪费。

**四、prototype属性的引入**

考虑到这一点，Brendan Eich决定为构造函数设置一个prototype属性。

这个属性包含一个对象（以下简称"prototype对象"），所有实例对象需要共享的属性和方法，都放在这个对象里面；那些不需要共享的属性和方法，就放在构造函数里面。

实例对象一旦创建，将自动引用prototype对象的属性和方法。也就是说，实例对象的属性和方法，分成两种，一种是本地的，另一种是引用的。

还是以DOG构造函数为例，现在用prototype属性进行改写：

> 　　function DOG(name){
>
> 　　　　this.name = name;
>
> 　　}
>
> 　　**DOG.prototype = { species : '犬科' };**
>
> 　　var dogA = new DOG('大毛');
>
> 　　var dogB = new DOG('二毛');
>
> 　　alert(dogA.species); // 犬科
>
> 　　alert(dogB.species); // 犬科

现在，species属性放在prototype对象里，是两个实例对象共享的。只要修改了prototype对象，就会同时影响到两个实例对象。

> 　　**DOG.prototype.species = '猫科';** 
>
> 　　alert(dogA.species); // 猫科
>
> 　　alert(dogB.species); // 猫科

**总结**

由于所有的实例对象共享同一个prototype对象，那么从外界看起来，prototype对象就好像是实例对象的原型，而实例对象则好像"继承"了prototype对象一样。

这就是Javascript继承机制的设计思想。不知道我说清楚了没有，继承机制的具体应用方法，可以参考我写的系列文章：

　　* [《Javascript面向对象编程（一）：封装》](http://www.ruanyifeng.com/blog/2010/05/object-oriented_javascript_encapsulation.html)

　　* [《Javascript面向对象编程（二）：构造函数的继承》](http://www.ruanyifeng.com/blog/2010/05/object-oriented_javascript_inheritance.html)

　　* [《Javascript面向对象编程（三）：非构造函数的继承》](http://www.ruanyifeng.com/blog/2010/05/object-oriented_javascript_inheritance_continued.html)

二周前，我谈了[一点](http://www.ruanyifeng.com/blog/2011/06/designing_ideas_of_inheritance_mechanism_in_javascript.html)Javascript的历史。

今天把这部分补全，从历史的角度，说明Javascript到底是如何设计出来的。

只有了解这段历史，才能明白Javascript为什么是现在的样子。我依据的资料，主要是[Brendan Eich的自述](http://brendaneich.com/2008/04/popularity/)。

2.

[上一篇文章](http://www.ruanyifeng.com/blog/2011/06/designing_ideas_of_inheritance_mechanism_in_javascript.html)写道：

> "1994年，网景公司（Netscape）发布了Navigator浏览器0.9版。这是历史上第一个比较成熟的网络浏览器，轰动一时。但是，这个版本的浏览器只能用来浏览，不具备与访问者互动的能力。......网景公司急需一种网页脚本语言，使得浏览器可以与网页互动。"

![img](http://www.ruanyifeng.com/blogimg/asset/201106/bg2011062401.jpg)

网页脚本语言到底是什么语言？网景公司当时有两个选择：一个是采用现有的语言，比如Perl、Python、Tcl、Scheme等等，允许它们直接嵌入网页；另一个是发明一种全新的语言。

这两个选择各有利弊。第一个选择，有利于充分利用现有代码和程序员资源，推广起来比较容易；第二个选择，有利于开发出完全适用的语言，实现起来比较容易。

到底采用哪一个选择，网景公司内部争执不下，管理层一时难以下定决心。

3.

就在这时，发生了另外一件大事：1995年Sun公司将Oak语言改名为Java，正式向市场推出。

Sun公司大肆宣传，许诺这种语言可以"一次编写，到处运行"（Write Once, Run Anywhere），它看上去很可能成为未来的主宰。

![img](http://www.ruanyifeng.com/blogimg/asset/201106/bg2011062402.png)

网景公司动了心，决定与Sun公司结成联盟。它不仅允许Java程序以applet（小程序）的形式，直接在浏览器中运行；甚至还考虑直接将Java作为脚本语言嵌入网页，只是因为这样会使HTML网页过于复杂，后来才不得不放弃。

总之，当时的形势就是，网景公司的整个管理层，都是Java语言的信徒，Sun公司完全介入网页脚本语言的决策。因此，Javascript后来就是网景和Sun两家公司一起携手推向市场的，这种语言被命名为"Java+script"并不是偶然的。

4.

此时，34岁的系统程序员Brendan Eich登场了。1995年4月，网景公司录用了他。

Brendan Eich的主要方向和兴趣是函数式编程，网景公司招聘他的目的，是研究将Scheme语言作为网页脚本语言的可能性。Brendan Eich本人也是这样想的，以为进入新公司后，会主要与Scheme语言打交道。

![img](http://www.ruanyifeng.com/blogimg/asset/201106/bg2011060503.jpg)

仅仅一个月之后，1995年5月，网景公司做出决策，未来的网页脚本语言必须"看上去与Java足够相似"，但是比Java简单，使得非专业的网页作者也能很快上手。这个决策实际上将Perl、Python、Tcl、Scheme等非面向对象编程的语言都排除在外了。

Brendan Eich被指定为这种"简化版Java语言"的设计师。

5.

但是，他对Java一点兴趣也没有。为了应付公司安排的任务，他只用10天时间就把Javascript设计出来了。

由于设计时间太短，语言的一些细节考虑得不够严谨，导致后来很长一段时间，Javascript写出来的程序混乱不堪。如果Brendan Eich预见到，未来这种语言会成为互联网第一大语言，全世界有几百万学习者，他会不会多花一点时间呢？

总的来说，他的设计思路是这样的：

> 　　（1）借鉴C语言的基本语法；
>
> 　　（2）借鉴Java语言的数据类型和内存管理；
>
> 　　（3）借鉴Scheme语言，将函数提升到"第一等公民"（first class）的地位；
>
> 　　（4）借鉴[Self语言](http://en.wikipedia.org/wiki/Self_(programming_language))，使用基于原型（prototype）的继承机制。

所以，Javascript语言实际上是两种语言风格的混合产物----（简化的）函数式编程+（简化的）面向对象编程。这是由Brendan Eich（函数式编程）与网景公司（面向对象编程）共同决定的。

6.

多年以后，Brendan Eich还是看不起Java。

他说：

> "Java（对Javascript）的影响，主要是把数据分成基本类型（primitive）和对象类型（object）两种，比如字符串和字符串对象，以及引入了Y2K问题。这真是不幸啊。"

把基本数据类型包装成对象，这样做是否可取，这里暂且不论。Y2K问题则是直接与Java有关。根据设想，Date.getYear()返回的应该是年份的最后两位：

> 　　var date1 = new Date(1999,0,1);
>
> 　　var year1 = date1.getYear();
>
> 　　alert(year1); // 99

但是实际上，对于2000年，它返回的是100！

> 　　var date2 = new Date(2000,0,1);
>
> 　　var year2 = date2.getYear();
>
> 　　alert(year2); // 100

如果用这个函数生成年份，某些网页可能出现"19100"这样的结果。这个问题完全来源于Java，因为Javascript的日期类直接采用了java.util.Date函数库。Brendan Eich显然很不满意这个结果，这导致后来不得不添加了一个返回四位数年份的Date.getFullYear()函数。

如果不是公司的决策，Brendan Eich绝不可能把Java作为Javascript设计的原型。作为设计者，他一点也不喜欢自己的这个作品：

> "与其说我爱Javascript，不如说我恨它。它是C语言和Self语言一夜情的产物。十八世纪英国文学家约翰逊博士说得好：'它的优秀之处并非原创，它的原创之处并不优秀。'（the part that is good is not original, and the part that is original is not good.）"

（完）





























#### 2.2 <u>有哪些相似技术？</u>

- TS：这个强类型的JS，全称TypeScript
- 

## 二、使用场景及方法

### 1. 常见使用场景

- **Web开发**：基于 HTML 和 CSS 构建的网站上提供交互功能
- **桌面应用**：一个不错的听歌软件就是Javascript做的，叫 [Listen1](http://listen1.github.io/listen1/)（悄悄的：它可以听全平台的音乐哦）
- **移动应用**：uni-app了解一下，web渲染、原生渲染都支持，还可以同时开发小程序。当然还有不少其他的框架，都可以做移动端应用
- **服务器和 API**：使用 Node.js 你可以获得一个可构建服务器的，高度且可扩展的 JS 运行时。长久以来，Express 一直是服务器端渲染 Web 应用或 API 的首选框架。
- **游戏开发**：JS 究其本源就是面向 UI 的，因此通过 JS,HTML 和 CSS 就已经能写出简单的网页游戏。
- **机器学习**：使用 TensorFlow.js，可以开发图像分类，语音识别或预测性分析的机器学习模型。
- **物联网 IoT**：Johnny-Five 平台为各种 Arduino 开发板提供了一个易用的 API。如果你对机器人更感兴趣，不妨试试 Cylon.js。

### 2. 简单使用示例

**使用场景**：Web开发

**实现步骤**：

1. 



## 三、总结

> ​	以上内容都是个人在校习得、业余积累、工作所学而来，有些还是一家之言，有更好的见解或不解之处，欢迎评论区讨论！(/•ิv•ิ)/
>
> ​	没有公众号，准备写完自己所了解的就改行了，兴趣、精力有限\_(：3 」∠ )_

- 

---

## 附录：扩展及参考

- [今日的 JavaScript 都能做什么？](https://www.sohu.com/a/344004372_120297818)

- [JavaScript的起源故事](https://blog.csdn.net/kese7952/article/details/79357868)

- [Javascript继承机制的设计思想](http://www.ruanyifeng.com/blog/2011/06/designing_ideas_of_inheritance_mechanism_in_javascript.html)
- [JavaScript 的历史](https://www.w3school.com.cn/js/pro_js_history.asp)
- [弱类型语言和强类型语言](https://blog.csdn.net/qq_36192099/article/details/79464196)