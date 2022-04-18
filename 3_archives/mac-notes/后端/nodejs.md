# 0 常用指令



Node常用指令

  //终端启动node

  $node



  //退出当前终端

  ctrl-c



  //退出 Node REPL

  ctrl + c 按下两次



  //使用下划线(_)获取上一个表达式的运算结果：

  var sum = _



  //查看输入的历史命令

  向上/向下 键



  //- 列出当前命令

  tab 键 



  //列出使用命令

  .help



  //退出多行表达式

  .break



  //退出多行表达式

  .clear



  //保存当前的 Node REPL 会话到指定文件

  .save filename

   

  //载入当前 Node REPL 会话的文件内容。

  .load filename







Npm常用命令：

  //Npm版本查询

  npm -v



  //初始化package.json配置文件

  npm init -y



  //Npm安装模块

  npm i [moudlename]



  //Npm安装已经依赖的模块

  npm i



  //Npm更新模块

  npm update [moudlename<@0.1><@latest>]



  //Npm卸载模块

  npm uninstall [moudlename]



  //Npm查找模块

  npm search [moudlename]



  //Npm命令

  npm run 命令名

  命令在 package.json 中scripts中查看操作

# 0 说明



**官网：**http://nodejs.cn/learn



**菜鸟教程：**

[**https://www.runoob.com/nodejs/nodejs-tutorial.html**](https://www.runoob.com/nodejs/nodejs-tutorial.html)



**npm install --save 、--save-dev 、-D、-S 的区别与NODE_ENV的配置：**

 https://blog.csdn.net/jwl_willon/article/details/81054978



node能做什么： https://blog.csdn.net/wang_kai_7/article/details/88286429



对于node.js非常好的一篇介绍的文章,英文比较好的朋友可以直接去阅读：

https://www.sitepoint.com/node-js-is-the-new-black/



**Node.js到底是用来做什么的** https://www.jianshu.com/p/fac1fa66a00a





**从零开始nodejs系列文章：** http://blog.fens.me/series-nodejs/







- Node.js是一个开源且跨平台的JS运行时环境。
- 是一个可用于几乎任何项目的流行工具
- 可在浏览器外运行V8 JS引擎（Google Chrome的内核），使得Node.js表现得非常出色
- 运行单个进程，无需为每个请求创建新的线程。
- 在其标准库中提供了一组异步的I/O原生功能（用于防止JS代码被阻塞）
- 其中的库通常是使用，非阻塞的范式编写的（使阻塞成为例外，而不是规范）
- 执行I/O操作时（如从网络读取、访问数据库或文件系统），它会在响应返回时恢复操作，而不是阻塞线程并浪费CPU循环等待
- Node具有独特的优势，使前端开发者，可以编写服务器端代码，而无需学习完全不同的语言
- NodeJS内置npm（node package manager），即node 包管理工具





## npm说明：

- Node.js安装好后，终端输入npm -v即可查看npm版本
- 用于管理项目依赖的资源
- npm的简单结构有助于Node.js生态系统的激增，现在npm仓库托管了超过1,000,000个可以自由使用的开源库包
- 开发者将写好的源码上传npm官网，当其他人需要使用的时候，通过npm的命令安装即可





## Node.js 应用程序的示例：

- Node.js 最常见的 Hello World 示例是 Web 服务器：



const http = require('http')



const hostname = '127.0.0.1'

const port = 3000



const server = http.createServer((req, res) => {

 res.statusCode = 200

 res.setHeader('Content-Type', 'text/plain')

 res.end('你好世界\n')

})



server.listen(port, hostname, () => {

 console.log(`服务器运行在 http://${hostname}:${port}/`)

})



# 0安装及使用技巧







## （1）配置npm淘宝镜像：



**终端中，打开**npm设置：



open ~/.npmrc



**编辑器中将** http://r.cnpmjs.org/ ，改为：



http://registry.npm.taobao.org





## （2）终端查看node历史命令



**终端：**



open ~/.node_repl_history







(1)安装nodejs

node -v

npm -v



(2)安装cnpm镜像



npm config set registry "http://registry.npmjs.org/"



npm install -g cnpm --registry=http://registry.npm.taobao.org



cnpm -v



(3)安装webpack

cnpm install webpack -g

cnpm install webpack-cli -g

webpack -v



(4)安装vue-cli

cnpm install vue-cli -g

vue -V



(5)安装iview

d:		回车

cd iview	回车

cd iview	回车

cnpm install	安装依赖



(6)运行node

cnpm run dev





# 1 .npmrc 配置



.npmrc就是用来配置npm源的



# 1 自动启动服务器





npm install -g supervisor

安装supervisor

cd ~/downloads/xms/vue/assets/js

打开server.js所在文件夹



supervisor /Users/wangxiansheng/Downloads/xms/vue/assets/js/server.js

用supervisor启动服务器

# Node常用指令



​	//终端启动node

​	node



​	//退出 Node REPL

​	ctrl + c 按两次



​	//使用下划线(_)获取上一个表达式的运算结果：

​	var sum = _



​	//查看输入的历史命令

​	向上/向下 键



​	//- 列出当前命令

​	tab 键 



​	//列出使用命令

​	.help



​	//退出多行表达式

​	.break



​	//退出多行表达式

​	.clear



​	//保存当前的 Node REPL 会话到指定文件

​	.save filename

​	

​	//载入当前 Node REPL 会话的文件内容。

​	.load filename



1.buffer 

​	- 缓冲区各种操作

2.@3

3.EventEmitter 

​	- 事件绑定模块

4.express 

​	- 网站整体搭建方案模块

5.get/post 

​	- 实现

6.mysql

7.@13

8.util 

​	- 对象继承 对象检查

9.web模块 

​	- 网页端 服务器 终端的连接

10.全局变量 

​	- 通过console显示出操作细节数据，没啥用

11.函数 

​	- 函数语法 服务器最简单实现 回调函数读取文件

12.@11

13.文件系统 

​	- 实现了各种文件操作🧞‍♂️🧞‍♀️🧟‍♂️🧟‍♀️👨🏿‍🚀👨‍✈️👩‍✈️👨‍🚒

14.模块系统 

​	- 模块的出口 和 模块的载入 与模块的方法使用 路由系统

15.@14





# NPM常用命令及CNPM安装



​	//Npm版本查询

​	npm -v



​	//初始化package.json配置文件

​	npm init -y



​	//Npm安装模块

​	npm i [moudlename]



​	//Npm安装已经依赖的模块

​	npm i



​	//Npm更新模块

​	npm update [moudlename<@0.1><@latest>]



​	//Npm卸载模块

​	npm uninstall [moudlename]



​	//Npm查找模块

​	npm search [moudlename]



​	//Npm命令

​	npm run 命令名

​	命令在 package.json 中scripts中查看操作





# mac安装并配置cnpm

前提：已经安装node



淘宝镜像：

--registry=https://registry.npm.taobao.org



1、打开终端app

cd ~



2、安装cnpm

npm install -g cnpm --registry=https://registry.npm.taobao.org



3、配置路径

open .bash_profile



如果没有该文件，则创建该文件，之后重复上一步打开文件

touch .bash_profile



在文本编辑器中粘贴下面内容，”PATH:”后面接的是cnpm的bin文件夹所在路径

export PATH=$PATH:/Users/wangxiansheng/bin



执行配置文件

source .bash_profile



查看cnpm版本

cnpm -v 



显示乱七八糟一大堆中有cnpm版本号！

成功！



一、模式



运行webpack命令时，一定要指定模式。



- 开发模式：有缩进，无压缩

webpack --mode development



- 生产模式：无缩进，有压缩

webpack --mode production







--save -dev

--save：将保存配置信息到pacjage.json。默认为dependencies节点中。

--dev：将保存配置信息devDependencies节点中。





--save：将保存配置信息到pacjage.json的dependencies节点中。

--save-dev：将保存配置信息到pacjage.json的devDependencies节点中。

dependencies：运行时的依赖，发布后，即生产环境下还需要用的模块

devDependencies：开发时的依赖。里面的模块是开发时用的，发布时用不到它。





