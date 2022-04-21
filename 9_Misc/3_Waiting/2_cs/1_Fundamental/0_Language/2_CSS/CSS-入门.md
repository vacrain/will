

## 一、介绍

### 科班/工作必会（学着玩的话，了解即可）

1. <u>**它**是什么？</u>

CSS是**层叠样式表**

所谓层叠，就是因为HTML本身就是层叠的，一层套一层的

样式就是页面内容长什么样

CSS就是这样一种可以控制页面内容（HTML）各部分长什么样子的这么一种语言，甚至可以做一些动画或根据鼠标点击悬浮等状态让内容变个模样，但这不叫动态网页哦

2. <u>相关的**行话、术语**有哪些？</u>（每篇文章下的该内容会持续更新，想起来了我就加上~）

- **样式**：就是长什么样，比如文字的大小、颜色，图片的长宽等

- **盒子模型**：可以去查查图片，就是每个HTML元素，都不简单就是一个矩形区域，都是有内容区域、留白区域(padding)、边框区域(border)以及外边距区域(margin)的

- **清除默认样式**：要清楚很多HTML元素是默认自带一些CSS样式的，容易影响使用者对CSS模型的判断，所以在使用前要清除默认样式

- **选择器**：要修改一个内容的样式的时候，肯定是要有选择的进行修改的，比如只修改div标签或只修改class为big的标签等等。CSS选择器提供了多种多样的选择器，如：id, class, 标签, 组合, 包含, 伪选择器, 超链接选择器...

- **预处理器**：原生的CSS如果行数少还好，如果行数多的话，可读性非常差，并且难以维护!

  所以出现了像SASS、SCSS这样的CSS预处理器，他们是新的语言，为 CSS 增加了一些编程的特性，比如可以使用变量了

  不过大部分和原生CSS还是基本相同且兼容的，与原生CSS相比，代码结构看起来更加清晰，可读性强，易于维护~

  程序员只需编写.sass或是.scss这样的文件，.css文件由系统自动编译生成~

  最终渲染页面使用的还是CSS文件！

3. <u>现在流行的版本是？特征是什么？</u>

**现流行版本**：CSS3

**特征**：最明显的特征就是**圆角矩形**

4. <u>大小写是否敏感？注释方法是什么？</u>

大小写**不敏感**

**单行注释方法**：

```CSS
/* 注释内容 */
```

**多行注释方法**：

```CSS
/* 
注
释
内
容 
*/
```

6. <u>样式表分类，哪个最常用？</u>

共三种，内联式、内部样式表以及外部样式表。

一般都用**外部样式表**。

### 其他了解（吹:cow::beer:用）

#### 为什么会出现

直接贴参考链接了：[CSS 二十年发展简史](https://baijiahao.baidu.com/s?id=1637397152152961209&wfr=spider&for=pc)

下面摘一些我认为有用的（或者可以吹牛B的）点：

- **1996 年 12 月，W3C 推出了 CSS 规范的第一版本。** 这跟我一个月诞生的...
- **IE6，前端工程师的痛**，2001 年，微软发布了 IE6，在 Windows 普及的年代 IE6 浏览器占据了高达 80% 的市场，因为 IE6 的用户量大，开发者们就选择了以大众为准，许多开发者竭尽全力把 IE6 下的页面做好，这样导致许多页面根本不是 W3C 标准，因为 IE6 有一套自己的解析渲染体系。最终 IE6 的庞大市场最终成为了 Web 开发者的一大绊脚石。
- 到现在CSS样式的兼容问题依旧折磨着一部分前端开发人员！（详见下图）
- 现在一大批 CSS 预处理和后处理工具涌现，比较流行的 CSS 预处理器有 Sass、Less，CSS 后处理器诸如 clean-css、AutoPrefixer、Rework、PostCSS 等。

#### 相似技术

**flash**：这个上过[4399.com](http://www.4399.com/)的都应该熟悉，这是一套整体的解决方案，因为太多bug，也是自己作的，在2020年12月31日彻底黄了。国内一家代理公司还想折腾一下，不过也不用看了，最后瞎折腾而已（可以了解一下：https://news.mydrivers.com/1/735/735418.htm）

## 二、使用场景及方法

### 常见的使用场景

- CSS主要用来设计网页的样式，美化网页
- 动画
- 小游戏

### 简单使用

*画个心吧*

1. **内联式样式表的写法：**

```html
<div stylt="transform: rotate(45deg);margin: 300px;">
    <div style="width: 100px;height: 100px;border:1px solid red;background-color: red;margin:300px 0px 0px 300px;border-radius:100%;float:left;"></div>
    <div style="width: 100px;height: 100px;border:1px solid red;background-color: red;margin:250px 0px 0px 0px;border-radius:100%;float:left;position: relative;right: 50px;"></div>
    <div style="width: 100px;height: 100px;border:1px solid red;background-color: red;margin: 300px 0px 0px 0px;float: left;position: relative;right: 152px;"></div>
</div>
```

2. **内部样式表的写法：**

```html

<head>
    <style>
    *{
        margin: 0px;
        padding: 0px;
    }
    .main{
        transform: rotate(45deg);
        margin: 300px;
    }
    .disc1{
        width: 100px;
        height: 100px;
        border:1px solid red;
        background-color: red;
        margin:300px 0px 0px 300px;
        border-radius:100%;
        float:left;
    }
    .disc2{
        width: 100px;
        height: 100px;
        border:1px solid red;
        background-color: red;
        margin:250px 0px 0px 0px;
        border-radius:100%;
        float:left;
        position: relative;
        right: 50px;
    }
    .square{
        width: 100px;
        height: 100px;
        border:1px solid red;
        background-color: red;
        margin: 300px 0px 0px 0px;
        float: left;
        position: relative;
        right: 152px;
    }
    </style>
</head>
<body>
    <div class="main">
        <div class="disc1"></div>
        <div class="disc2"></div>
        <div class="square"></div>
    </div>
</body>
```

2. **外部样式表的写法：**

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <link href="css/square.css" rel="stylesheet" type="text/css">
        <title></title>
    </head>
    <body>
        <div class="main">
            <div class="disc1"></div>
            <div class="disc2"></div>
            <div class="square"></div>
        </div>
    </body>
</html>
```

```css
// 这是square.css文件啦
*{
    margin: 0px;
    padding: 0px;
}
.main{
    transform: rotate(45deg);
    margin: 300px;
}
.disc1{
    width: 100px;
    height: 100px;
    border:1px solid red;
    background-color: red;
    margin:300px 0px 0px 300px;
    border-radius:100%;
    float:left;
}
.disc2{
    width: 100px;
    height: 100px;
    border:1px solid red;
    background-color: red;
    margin:250px 0px 0px 0px;
    border-radius:100%;
    float:left;
    position: relative;
    right: 50px;
}
.square{
    width: 100px;
    height: 100px;
    border:1px solid red;
    background-color: red;
    margin: 300px 0px 0px 0px;
    float: left;
    position: relative;
    right: 152px;
}
```

**三种CSS写法，都可以实现一样的效果~：**

![](https://images2015.cnblogs.com/blog/1035652/201704/1035652-20170417111315462-567520790.png)

## 三、总结

> 以上内容都是个人在校习得、业余积累、工作所学而来，有些还是一家之言，有更好的见解或不解之处，欢迎评论区讨论！(/•ิv•ิ)/
>
> 没有公众号，准备写完自己所了解的就改行了，兴趣、精力有限\_(：3 」∠ )_

- 想要网站美观，就离不开CSS
- CSS也同HTMl一样，没有太深的概念，只需熟能生巧
- 调整样式还是很费心神的一件事，除非想做UI设计（好像UI设计也不用调整CSS，都用各种UI设计软件AXURE、Sketch之类的），一般原理基本了解以后，可以采用网上现有的一些CSS框架，比如Bootstrap、ElementUI、Ant Design等等，都有现成的小按钮，各种小精致小组件...
- **Ant Design慎用**。。。还挺搞笑的，可以了解一下：[antd组件的圣诞节彩蛋事件](https://www.jianshu.com/p/24e39e97ae8f)
- 普遍的标准都是CSS3以前的，CSS3的新特性也可以作为扩展自己百度了解一下，还是有很常用的，比如边框圆角...

---

## 附录：参考

- 自己过去的CSS总结~

- [CSS 二十年发展简史](https://baijiahao.baidu.com/s?id=1637397152152961209&wfr=spider&for=pc)

- [antd组件的圣诞节彩蛋事件](https://www.jianshu.com/p/24e39e97ae8f)

  ## 今日午餐：酱香麻辣鸡腿烧+米饭

  



