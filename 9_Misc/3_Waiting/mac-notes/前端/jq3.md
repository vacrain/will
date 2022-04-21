# 0 jQuery



手册参考：https://jquery.cuishifeng.cn







- 基于JavaScript函数库

- 轻量级的“写的少，做得多”地JavaScript库

- 极大地简化了JavaScript编程

- 包含以下功能：

- - HTML 元素选取
  - HTML 元素操作
  - CSS 操作
  - HTML 事件函数
  - JavaScript 特效和动画
  - HTML DOM 遍历和修改
  - AJAX

- jQuery库是一个JavaScript文件（jquery.min.js）



# jQuery语法



## 基础语法：$(selector).action()

- 美元符号定义jQuery
- 选择符（selector）查找的HTML元素
- action()表示对元素的操作





## jQuery选择器

- jQuery选择器允许对HTML**元素组**或**单个元素**进行查找操作
- 基于元素的id、类、类型、属性、属性值等来查找，基于已存在的CSS选择器，除此之外还有一些自定义的选择器
- jQuery中所有的选择器都以美元💲符号开头：$()





## jQuery事件

- jQuery是为事件处理特殊设计的



**格式：**

$(“p”).click(function() {

​	// 动作触发后执行的代码！！

})



**常用事件：**

$(document).ready()方法允许文档完全加载完成后执行函数



## jQuery中的AJAX

**使用格式：**

$.ajax({

​	type: ”post”,

​	url: “/user/login/“,

​	data: “name=abc&password=123”,

​	success: function(res){

​		alert(res);

​	}

})



















jQuery3 

概念：jQuery是基于JavaScript语言的框架



1.选择器

$(‘#a’)id为a的标签

$(‘div:eq(1)’)第二个div

$(‘div:last’)最后一个div

$(‘div[name]’)有name属性的div





2.属性

$(‘#a’).html()

$(‘#a’).text()

$(‘#a’).val()





3.CSS

$(‘#a’).css(‘border’,’1px red solid’);

$(‘#a’).width(200);

$(‘#a’).height(200);







4.文档处理

在末尾处添加：$(‘#t’).append(‘<tr></tr>’);

在开头处添加：

$(‘#t’).append(‘<tr></tr>’);





5.事件

$(‘#a’).click(

​	function(){

​		alert(1);

}

)





6.AJAX

$(‘#a’).click(

​	$.ajax({

​	Type:”post”,

​	[url:”/user/login]("url:”)”,

​	data:”name=abc&age=30”,

​	success:function(res){

​		alert(res);

​	}

})

)





# 2 EasyUI

- 该组件库比较丑





## 使用步骤：





**（**1）从该文件夹中向页面中引入js

1. 1. jquery.min.js
   2. jquery.easyui.min.js
   3. themes/easyui.css
   4. themes/icon.css



**（**2）写一个jQuery方法，在加载js时运行



    <script>

​    function m1() {

​      $.ajax({

​        url: "/getAll",

​        success: function (res) {

​          $("#t1").datagrid({

​            columns: [[

​              {field:'empno',title:'员工编号'},

​              {field:'ename',title:'员工姓名'},

​              {field:'job',title:'职务'}

​            ]],

​            data:res

​          })

​        }

​      })

​    }



​    $(function (){

​      m1()

​    })



**（**3）写dom



    <table id="t1"></table>