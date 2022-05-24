# 1 JavaScript

## JS 说明：

-   是一种脚本语言
-   弱类型：声明不需要确定类型，第一次赋值确定类型

## （一）数据类型

| 字符串 | ‘0’              | string    |
| ------ | ---------------- | --------- |
| 数字   | 0.0/0            | number    |
| 布尔   | true/false       | boolean   |
| 对象   | {a:’a’}/null     | object    |
| 未定义 | undefined/var u; | undefined |

## （二）运算符

1.  算数运算符

2.  -   \+ - \* / %

3.  比较运算符

4.  -   \> >= < <= == !=

5.  逻辑运算符

6.  -   && || !

7.  赋值运算符

8.  -   += -= \*= /= %= =

9.  自增自减运算符

10. -   ++ —

11. 三目运算符

12. -   ? :

## （三）流程控制语句

if 分支语句

for(v in list)

in 可以取出数组的下标

for(var i in a){}

for(I in list)

of 可以取出数组的元素

for(var i of a){}

## （四）事件

单击事件：onclick=””

键盘抬起事件：onkeyup=””

双击事件：ondblclick=””

## （五）方法

无返回值：function m(){ }

有返回值：function m(){return 1;}

## （六）外部方法

通过<script src="js01.js" ></script>导入外部 js 文件，随后该文件中的方法都可以使用了

## （七）DOM

-   JS 也是面向对象语言，内置了很多对象，DOM 对象最重要

-   DOM：文档对象模型，就是 document 对象，浏览器会把页面中所有内容都封装到 DOM 对象中

-   页面和该封装的 DOM 对象映射，类似数据库与 mybatis

## DOM 能实现增删改查

​ 查：

document.getElementById(‘a’);

​ 或直接 :

a

​ 改：

Img01.setAttribute(‘src’,’img/2.jpg)

​ 增：select 标签中加一个 option 标签

var opt = document.createElement(‘option’);

var text = document.createTextNode(‘大连’);

opt.appendChild(text)

select.appendChild(opt)

​ 删除：ul 的 id 为 ul，删除 id 为 li01 的 li 标签

ul.removeChile(li01)

## （八）JSON

-   JSON 是 JS 的对象表示方式
-   JSON 是前后台交互的数据格式的标准

**JSON**表示一个对象：（单个对象）

var person = {id:1,name:’abc’,age:23};

**JSON**表示一个数组：（多个对象，不常用）

var arr = [{name:’abc’},{name:’bcd}]

**综合：（常用）**

var obj = {

​ count:99,

​ list:[

​ {name:’abc’},

​ {name:’bcd’}

​ ]

}

## （九）JSON 遍历

遍历数组：for(var i = 0;i<arr.length;i++)

遍历对象：for(var v in person)

# JS 框架目录

-   NodeJS
-   Vue
-   ES6
-   Axios
-   jQuery

# 10 URL 中%2F,%2B 等特殊字符

#

参考： http://www.mamicode.com/info-detail-2375323.html

-   下表中列出了一些 URL 特殊符号及编码 十六进制值

\1) + URL 中+号表示空格 %2B

\2) 空格 URL 中的空格可以用+号或者编码 %20

\3) / 分隔目录和子目录 %2F

\4) ? 分隔实际的 URL 和参数 %3F

\5) % 指定特殊字符 %25

\6) # 表示书签 %23

\7) &amp; URL 中指定的参数间的分隔符 %26

\8) = URL 中指定参数的值 %3D

常见用%2F 代表/

# 4 AJAX

## 说明：

-   AJAX 是一种在无需重新加载整个网页的情况下，能够更新部分网页的技术。
-   AJAX = 异步 JavaScript 和 XML。
-   AJAX 是一种用于创建快速动态网页的技术。
-   通过在后台与服务器进行少量数据交换，AJAX 可以使网页实现异步更新。这意味着可以在不重新加载整个网页的情况下，对网页的某部分进行更新。
-   传统的网页（不使用 AJAX）如果需要更新内容，必需重载整个网页面。

## 使用步骤：

**1.**创建请求函数：

function loadXMLDoc(){

**2-1.** 无需做老版本 IE：

-   创建 XMLHttpRequet 对象
-   如果做 IE7 前的前端，可以采取 2-2 的创建方式

var xmlhttp = new XMLHttpRequest();

**2-2.**如需做老版本 IE：

-   判断浏览器版本创建对象
-   如果不做 IE7 以前的可以忽略此步

var xmlhttp

if (window.XMLHttpRequest)

{// code for IE7+, Firefox, Chrome, Opera, Safari

xmlhttp=new XMLHttpRequest();

}

else

{// code for IE6, IE5

xmlhttp=new ActiveXObject("Microsoft.XMLHTTP");

}

**3.**如需要 post 方式请求：

-   需要添加请求头，然后在 send 方法中规定发送到数据
-   header：规定头的名称，如：”Content-type”
-   valve：规定头的值，如：”application/x-www-form-urlencoded”

xmlhttp.setRequestHeader(header,value)

**4.**如需异步处理响应：

-   当使用异步时，需要规定响应处理，在 onreadystatechange 事件中的就绪状态时执行的函数中处理

-   **responseText 属性**

-   -   如果来自服务器的响应并非 XML，请使用 responseText 属性。
    -   responseText 属性返回字符串形式的响应

-   **responseXML 属性**

-   -   如果来自服务器的响应是 XML，而且需要作为 XML 对象进行解析
    -   使用方法自己百度看看就好

-   XHR 的属性介绍：

-   -   **注释：**onreadystatechange 事件被触发 5 次（0 - 4），对应着 readyState 的每个变化。

| **属性**           | **描述**                                                                                                                                     |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| onreadystatechange | 存储函数（或函数名），每当 readyState 属性改变时，就会调用该函数。                                                                           |
| readyState         | 存有 XMLHttpRequest 的状态。从 0 到 4 发生变化。 0: 请求未初始化 1: 服务器连接已建立 2: 请求已接收 3: 请求处理中 4: 请求已完成，且响应已就绪 |
| status             | 200: "OK" 404: 未找到页                                                                                                                      |

xmlhttp.onreadystatechange=function()

{

if (xmlhttp.readyState==4 && xmlhttp.status==200)

{

document.getElementById("myDiv").innerHTML=xmlhttp.responseText;

}

}

**4.**配置请求：

-   method（请求方式）：get、post
-   url（请求地址）
-   async（同步/异步）：true（异步）、false（同步）

xmlhttp.open(method,url,async)

**5.**发送请求到服务器：

-   string 仅用于 post 请求，如：

-   -   ”username=abc&password=123”
    -   “{name:abc,age:23}”

send(string)

**6.**如需同步处理：

-   直接处理响应

myDiv.innerHTML=xmlhttp.responseText;

**7.**请求方法结束：

}

## 例子：

-   方式：post
-   请求头：
-   同步/异步：异步
-   浏览器：IE7+

function load(){

​

​ var xmlhttp = new XMLHttpRequest();

​ xmlhttp.setRequestHeader(“Content-Type”,”application/Json”)

​ xmlhttp.onreadystatechange = function(){

​ if(xmlhttp.readyState==4&&xmlhttp.status==200){

​ myDiv.innerHTML = xmlhttp.responseText

​ }

​ }

​ var url = ‘localhost:8080”

​ var user = {username:abc,password:123)

​ xmlhttp.open(“post”,url,true)

​ xmlhttp.send(user)

}

# 3 Get 和 Post 对比说明

|                  | GET                | POST               |
| ---------------- | ------------------ | ------------------ |
| ⭐️ 回退时       | 无害               | 再次提交           |
| ⭐️ 缓存         | 主动缓存           | 无（除非手动设置） |
| ⭐️ 历史记录     | 保留               | 不保留             |
| ⭐️ 是否长度限制 | 有（因浏览器而定） | 无                 |
| ⭐️ 传递参数媒介 | url                | request.body       |
| 收藏             | 可以               | 不可               |
| 编码             | url                | json 等等          |
| 使用字符         | ASC2               | 无限制             |
| 安全             | 较不安全           | 较安全             |

# 2 原型链

参考：https://www.jb51.net/article/30750.htm

## js 原型链原理看图说明

更新时间：2012 年 07 月 07 日 16:53:22 作者：

任何一个对象都有一个 prototype 的属性，在 js 中可以把它记为：**proto**

当初 ECMAscript 的发明者为了简化这门语言，同时又保持继承的属性，于是就设计了这个链表。。

在数据结构中学过链表不，链表中有一个位置相当于指针，指向下一个结构体。

于是乎**proto**也一样，每当你去定义一个 prototype 的时候，相当于把该实例的**proto**指向一个结构体，那么这个被指向结构体就称为该实例的原型。

文字说起来有点儿绕，看图说话

var foo = {

x: 10,

y: 20

};

![image-20220418062444003](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-04-18_06-24-44_image-20220418062444003.png)

当我不指定**proto**的时候，foo 也会预留一个这样的属性，

如果有明确的指向，那么这个链表就链起来啦。

很明显，下图中 b 和 c 共享 a 的属性和方法，同时又有自己的私有属性。

**proto**默认的也有指向。它指向的是最高级的 object.prototype，而 object.prototype 的**proto**为空。

var a = {

x: 10,

calculate: function (z) {

return this.x + this.y + z

}

};

var b = {

y: 20,

**proto**: a

};

var c = {

y: 30,

**proto**: a

};

// call the inherited method

b.calculate(30); // 60

![image-20220418062512089](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-04-18_06-25-12_image-20220418062512089.png)

理解了**proto**这个属性链接指针的本质。。再来理解 constructor。

当定义一个 prototype 的时候，会构造一个原形对象，这个原型对象存储于构造这个 prototype 的函数的原形方法之中.

function Foo(y){

this.y = y ;

}

Foo.prototype.x = 10;

Foo.prototype.calculate = function(z){

return this.x+this.y+z;

};

var b = new Foo(20);

alert(b.calculate(30));

![image-20220418062541298](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-04-18_06-25-41_image-20220418062541298.png)

【参考文档】

http://dmitrysoshnikov.com/ecmascript/javascript-the-core/
