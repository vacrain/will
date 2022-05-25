# 0 说明

vue3 体验说明：https://zhuanlan.zhihu.com/p/139590941

# 1 Vue 说明

-   数据驱动、组件

参考（**手摸手，带你用 vue 撸后台 系列二(登录权限篇)）**：https://segmentfault.com/a/1190000009506097#articleHeader10

参考（vue 项目 构建 打包 发布 三部曲）：https://www.cnblogs.com/hi-shepherd/p/6911098.html

参考（vue 项目打包发布 通过 nginx）：https://www.cnblogs.com/hzozj/p/12937634.html

## 注意

-   使用 v-for 时，用 index 作为 key 的方式除了第一个数据可以复用之前的之外,其他项都需要重新渲染，所以建议用 id 作为 key，即:key="id"

## 文件引用路径说明

**@/a.vue**

表示：src/a.vue

**./a.vue**

表示：当前文件所在文件夹/a.vue

**@/**的意思：

表示的是相对路径(当然这也是简写啦)，vue.config.js 文件中配置：

configureWebpack: {

// provide the app's title in webpack's name field, so that

// it can be accessed in index.html to inject the correct title.

name: name,

resolve: {

alias: {

​ '@': resolve('src')

}

}

}

## Vue 对象属性

-   el：vue 的 view 层作用域

-   data：数据，vue 的 model 层

-   methods：函数集

-   watch：监听器

-   -   是一个对象，其中用键值对表示

    -   键：监听的变量

    -   值：函数或单引号包裹的函数名

    -   值可以包含：

    -   -   handler：回调函数，及监听变化后执行的函数，有两个参数（变化后的值，变化前的值），有一个参数（变化后的值）
        -   deep：true 或 false，表示是否深入监听
        -   immediate：true 或 false，表示是否在声明时执行 handler

    -   必要时候，跳转了路由需要注销监视器

-   钩子函数，一共八个：

-   -   beforeCreate
    -   Created
    -   beforeMount
    -   mounted
    -   beforeUpdate
    -   updated
    -   beforeDestroy
    -   destroy

-   computed：计算函数

-   过滤器

-   路由

# Vue 指令

1. v-html
2. v-text
3. v-show
4. v-if
5. v-else
6. v-ifelse
7. v-for
8. v-on
9. v-bind
10. v-model
11. v-slot
12. v-pre
13. v-cloak
14. v-once

#

# Vue 项目配置

## （1）修改端口：

**在根目录修改或新建** vue.config.js 文件：

module.exports = {

devServer: {

​ port: 8888, // 端口

}

};

<li>（1）HTML5超文本标记语言</li>

​

   <li>（2）CSS3层叠样式表</li>

   <li>（3）JavaScript脚本语言</li>、

​

   <li>（4）ES6标准</li>

​

   <li>（5）jQuery3框架（JavaScript框架</li>

​

   <li>（6）Bootstrap3框架（CSS框架）</li>

​

​

​

   <li>（7）Vue框架（JavaScript框架）</li>

​

   <li>（8）Axios框架（JavaScript框架）</li>

​

## <li>（9）Restful 开发风格（协议）</li>

  <h3>Vue框架</h3>

  <h2>Vue框架概念:Vue是一个基于[MVVM]原理的JavaScript框架.</h2>

  <h2>M-Model-模型-后台发往前台的JSON数据</h2>

  <h2>V-View-视图-HTML页面</h2>

  <h2>VM-ViewModel-视图模型-Vue对象</h2>

  <h3>Axios框架</h3>

  <h2>Axios框架是用来和服务器交互的JavaScript框架. Vue + Axios.</h2>

  <h3>Result API</h3>

  <h2>前后台交互的编程风格, 不是强制的.</h2>

  <h2>查询功能:get请求</h2>

  <h2>删除功能:delete请求</h2>

  <h2>添加功能:post请求</h2>

  <h2>修改功能:put请求</h2>

## main.js 文件中：

**（1）Vue.config.productionTip = false**

-   阻止启动生产消息，常用作指令
-   消息提示的环境配置，设置为开发环境或者生产环境

# 2 Vue 项目启动总结

-   安装创建工程

-

⭐️ 说明：

-   node 是用来管理项目资源的
-   vue-cli 是用来创建项目的
-   通过 IDEA 可以配置快捷启动，如下图

![Screen Shot 2020-09-14 at 09.26.09.png](/blob:file:/bcd3b46a-e414-466d-91a7-403f32a070c7)

-   一般依赖使用过程：

-   1.  npm i onedepandency
    2.  import xxx from 'xxx'
    3.  Vue.use(xxx)
    4.  userXxx in views or components

⭐️ 相关终端命令：

-   node 版本：

node -v

-   node 安装目录：

which node

-   通过淘宝安装依赖：(在 npm install xx 依赖后加）

--registry https://registry.npm.taobao.org install express

-   vue-cli 版本：

vue -V

-   vue-cli-service: command not found

-   -   导致原因：跨平台直接导入项目
    -   直接删除 node_models 文件夹
    -   之后，重新安装依赖，运行下面代码即可

npm install --registry https://registry.npm.taobao.org install express

-   启动项目：

npm run serve

-   打包，会生成一个 dist 文件夹：（该文件夹中的内容可直接放入 spring 项目的 static 文件夹中）

npm run build

**无用代码：**

sudo rm -rf node_modules package-lock.json && npm install

sudo npm global remove @vue/cli

sudo npm i -g @vue/cli --registry https://registry.npm.taobao.org install express

## （一）Vue-cli

-   vue 脚手架、vue 基础框架，类似 SpringBoot

**第一种安装**vue-cli：

**1.**先进入工作空间：

cd 工作空间地址

**2.**安装 vue-cli：

npm install -g @vue/cli --registry https://registry.npm.taobao.org install express

**3.**进入 bin 文件夹中查看 vue 是否安装成功：

cd bin

vue -V

⭐️ 第二种安装 vue-cli：

**1.**打开终端，进入 vue-cli 根目录：

cd /Library/vue/vue-cli

**2.**安装 vue-cli：

-   安装后会多出两个文件夹，分别为 bin 和 lib

-   -   bin 存放 vue-cli 命令
    -   lib 存放 vue-cli 运行环境

npm install -g @vue/cli --registry https://registry.npm.taobao.org install express

**3.**配置环境变量，先打开配置文件：

cd ~

open .zshrc

**4.**粘贴配置：

\# Vue-cli 3

export VUE=/Library/vue/vue-cli

export PATH=$PATH:$VUE/bin

**5.**关闭配置文件后，使其生效

source .zshrc

**6.**查看 vue 版本，确认配置成功：

vue -V

**第一种创建**vue-cli 工程：

-   通过 vue create 直接创建

vue create 项目名

遇到询问配置，直接回车选择默认即可

**第二种创建**vue-cli 工程：

-   通过 UI 界面创建 vue 工程

vue ui

之后在可视化界面（网页）中创建 vue 工程即可

**Tip**：vue-cli 工程创建完成后，可通过 npm install 添加依赖：如 vuex、axios、vue-router 等，格式如下

npm install 依赖名称

## （二）Vue-cli 目录结构说明：

![Pasted Graphic.pdf](/blob:file:/96eadc73-d2c1-4436-b18b-1510d628ba89)

-   node_modules：存放 npm install 命令下载的开发环境和生产环境的各种依赖

-   public：存放打包好的项目，即静态文件

-   -   index.html：工程首页

-   src：工程项目的源码以及资源，包括页面图片、路由组件、路由配置、vuex、入口文件等

-   -   assets：静态资源，图片、音频等

    -   components：组件库，用于路由调用

    -   App.vue：主组件，页面出口文件 ，所有页面都是在该文件下进行切换的

    -   main.js：项目入口脚本，存放项目唯一的 vue 对象

    -   -   渲染方式：render:h=>h(App)
        -   绑定要渲染的标签：$mount(‘#app’)

-   package.json：配置运行及依赖信息，修改依赖配置后，通过 npm install 即可更新依赖

## （三）Vue-cli 工程启动、停止及打包

-   在 package.json 文件中可以修改命令，如下图：

![Screen Shot 2020-09-12 at 23.32.11.png](/blob:file:/53101592-1cbf-4164-a2a9-4e981944a5c0)

**Vue**项目起服务器

npm run serve

**Vue**项目打包

npm run build

**Vue**项目停止

ctrl + C

##

## （四）Vue 组件的创建及引用

-   组件创建格式：

**例子：**components/LoginPage.vue

<template>

    <div>

​ <input type=“text” v-model=“username” placeholder=“用户名” /><br />

​ <input type=“password” v-model=“password” placeholder=“密码” /><br />

​ <button>Login</button>

​ </div>

</template>

<script>

// export需要提前命名组件，export可以在引入组件的时候再命名

export default{

​	name : ‘login’,

​	data(){

​		return{

​			username : ‘’,

​			password : ‘’

​		}

​	}

}

</script>

-   组件导入格式

**例子：**App.vue 中导入组件

<template>

    <div id=“app”>

​ <login />

​ </div>

</template>

<script>

​	import Login from ‘@/components/LoginPage”



​	export default{

​		name : ‘App’,

​		components : {

​			Login

​		}

​	}

</script>

## （五）Vue-router

-   vue 路由，vue 前端页面跳转配置和权限配置工具

**通过**npm 安装 vue-router

npm install vue-router

**vue-router**提供两个标签

-   <router-link :to=“”></router-link>

-   -   用于跳转

-   <router-view />

-   -   路由导航出口，用于显示

**路由使用步骤：**

**1.src**文件夹中，新建文件夹，名为：router

**2.router**文件夹中，创建 js 文件，名为 index.js

**3.index.js**文件中，配置路由

import Vue from ‘vue’

import router from ‘vue-router’

import HelloWorld2 from ‘@/components/HelloWorld’

// vue 对象使用路由

Vue.use(router)

// 配置路由装载

export default new router({

​ routes : [

​ { // 重令项，配置默认显示组件

​ path : ‘/‘,

​ redirect : ‘/LoginPage’ // 默认 path，重新定向

​ },

​ { // 方式一，直接设置路由

​ path : ‘/LoginPage’, // path 是 localhost:8080/#/LoginPage 末尾的地址

​ component : ()=>import(‘@/components/LoginPage’),

​ name : ‘Login’

​ },

​ { // 方式二，通过引入设置路由

​ path : ‘/HelloWorld’,

​ component : HelloWorld2,

​ name : ‘HelloWorld’

​ }

​ ]

})

**4.main.js**文件中，加入路由

import router from ‘./router’

new Vue({

​ router,

​ …

})

**5.App.vue**文件中，配置路由出口，div 中添加

<router-view />

**6.**测试路由，启动 vue 工程

## （六）Axios

-   http 管理库，管理数据请求 及 响应

**通过**npm 安装 Axois：

npm install axios

Axios 使用步骤：以 LoginPage.vue 文件为例

1.<script>标签中引入 axios

import axios from ‘axios’

2.在 vue 对象中写方法

data(){},

methods : {

​ Login(){

​ axios.request({

​ url : ‘http://127.0.0.1:8080/user/login',

​ data : {

​ username : this.username,

​ password : this.password

​ },

​ method : ‘post’

​ }).then( (res) => {

​ alert(res);

​ }).catch();

​ }

}

3.在标签中绑定方法

<button @click=“login”>Login</button>

## （七）其他

##

## NodeJS

-   项目开发环境及依赖管理工具

## Vuex

-   vue 状态管理工具

vuex：专为 Vue.js 应用程序开发的**状态管理模式**。：

https://vuex.vuejs.org/zh/

## ES6

-   JS 编码标准

## Less

-   新样式表

## Webpack

-   JS 静态打包工具，打包好的文件夹内的内容可以直接做前端根目录

**4** [Vue 中 import 用法](https://www.cnblogs.com/BAHG/p/12775156.html)

-   可用于写工具

**1. 引入第三方插件**

第三方常用插件参考https://blog.csdn.net/vbirdbest/article/details/86527886

**2. 导入 css 文件**

import 'iview/dist/styles/iview.css';

如果是在.vue 文件中导入，那么是在 vue 组件的 style 里面导入，且 import 前面需要加@符号

<style>

　　@import 'iview/dist/styles/iview.css';

</style>

**3. 导入 js 文件**

import tools from './tools.js'

**4. 导入函数、字符串、数字、类**

假设有一个 js 文件，代码如下：

let aa = 'aaaaaaa',

bb = ( () => {

​ return '这是函数 bbbbb'

})

export {aa,bb};

这里 aa 是字符串，bb 是函数，当我们想要引入它们的时候，

import {aa,bb} from “js 文件的路径”；

import {aa} from “js 文件的路径”；

import {bb} from “js 文件的路径”；

**5. 导入整个模块(该模块中导出了多个方法和变量）**

假设有一个 tools.js 文件，

export const sqrt = Math.sqrt;

export function square(x) {

return x \* x;

}

export function diag(x, y) {

return sqrt(square(x) + square(y));

}

由于该文件导出不止一个函数，所以不能采用上面方法。此时应该导入整个模块，把 tools 文件里所有 exports 的方法都导入：

import \* as tools from "js 文件的路径"

然后使用 tools.sqrt、tools.square()

在这里顺便说一下 export 和 export default 的区别：

-   如果是 export 导出的文件，在导入时可以一次导入一个，也可以导入多个，但必须加上花括号！

import {add} from './math'

import {add, sub} from './math'

-   如果是 export default 导出的文件，只能一个一个的导入，且不需要加上花括号。一个模块中只能有一个 export default 默认输出。

import {add} from './math'

import {sub} from './math'

**6. 导入组件**

（1）导入内部组件。通常在 vue 文件中导入组件、注册组件、使用组件。

<template>

<name1></name1>

</template>

<script>

import name1 from './name1'

import name2 from './name2'

 components:{

   name1,

   name2,

 },

</script>

（2）导入外部组件。

// 引入全部组件

import Vue from 'vue'

import Router from 'vue-router' // vue-router 是 Vue.js 官方的路由插件

import Mint from 'mint-ui' // Mint UI 是一个基于 Vue.js 的移动端组件库。

Vue.use(Router)

Vue.use(Mint)

// 按需引入部分组件

import {Cell, Checklist} from 'mint-ui'

Vue.component(Cell.name, Cell)

Vue.component(Checklist.name, Checklist)

# 6 Router

-   路由

**route**和 router 区别：

https://blog.csdn.net/wangguoyu1996/article/details/80628135

**router**跳转传参数：

https://blog.csdn.net/qq_36727756/article/details/90450891

**vue-router 各个属性的作用及用法：**

[**https://blog.csdn.net/sinat_41882906/article/details/84847041**](https://blog.csdn.net/sinat_41882906/article/details/84847041)

**# 动态路由匹配**

https://router.vuejs.org/zh/guide/essentials/dynamic-matching.html#响应路由参数的变化

⚠️ 不建议用 Safari 浏览器进行测试！

**什么是路由呢？**

-   可以参照下官方的解释：https://router.vuejs.org/zh/guide/#html

-   路由允许我们通过不同的 URL 访问不同的内容。该 URL 可以是我们自己设置的,在项目中并没有这样的文件夹,这种功能就是路由.

-   路由的本质是 hash 值!

-   vue 中的路由设置分为四步曲 :

-   1. 定 : 定义路由组件
    2. 配 : 配置路由
    3. 实 : 实例化路由
    4. 挂 : 挂载路由

## Router 对象配置内容说明：

-   src/router/index.js 文件中进行配置：

export defult new Router({

*// mode: 'hash',//hash*模式下，浏览器地址不规整*,*带有*#*

*// mode: 'history',//history*模式下，浏览器地址规整，但需要后台支持

**mode: 'history',**

// 借助 vue-router 提供的 scrollBehavior，可以来管理组件滚动行为

// 进阶使用：https://www.jianshu.com/p/c805b74e1f14?utm_campaign

**scrollBehavior: () => ({x: 0, y: 0}),**

// 通过 routes 可以配置路由逻辑及样式

**routes:[**

**{// 第一个路由**

// 可以通过 path 或 name 来跳转路由

**path: '/',**

**name: 'root',**

**// hidden 是 elemenUI 自定义的，用来判断可不可以进入该 path 的路由，默认 false，即不隐藏该路由**

**hitdden: true/flase,**

// 该属性指向的页面/组件，或指向引入的页面/组件（如下 Layout）

**component: Layout,**

**// component: import('@/layout/index.js'),**

// 重定向，改变上面的路径（也就是’/‘）,变成 '/dashboard'

**redirect: '/dashboard',**

// **meta 第一种使用**：配置显示样式

**meta: {**

​ **title:"主页面", //配置 title**

​ **content: 'disable' //配置 content**

​ **keepAlive: true //是否缓存**

**},**

*// main.js*里面的代码：（*ElementUI*中已经写好，可以直接配置*meta*即可）

router.beforeEach((to, from, next) => {

*/\*\* 路由发生变化修改页面*meta \*/\*

if(to.meta.content){

let head = document.getElementsByTagName('head');

let meta = document.createElement('meta');

meta.content = to.meta.content;

head[0].appendChild(meta)

}

*/\*\* 路由发生变化修改页面*title \*/\*

if (to.meta.title) {

document.title = to.meta.title;

}

// 效果如下：

![image-20220418064313386](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-04-18_06-43-13_image-20220418064313386.png)

// **meta 第二种使用**：配置导航

![image-20220418064412910](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-04-18_06-44-13_image-20220418064412910.png)

// **meta 第三种使用**：控制公共组件的显示或隐藏

![image-20220418064355397](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-04-18_06-43-55_image-20220418064355397.png)

// 通过 children 可以配置子路由：

**children: [{**

**path: 'dashboard',**

**name: 'Dashboard',**

**component: () => import('@/views/dashboard/index'),**

**meta: { title: 'Dashboard', icon: 'dashboard' }**

**}]// children end**

**}// 第一个路由 配置结束**

**})//配置 router 结束**

# 11 mock

-   模仿后端服务器

参考：https://www.jianshu.com/p/c5568910e946

# 11 MVVM 的优点和缺点

-   MVVM 里，controller 将不再直接和真实的 model 进行绑定了，而通过 ViewModel,viewModel 进行持有真实的 Model。

## 方便测试

-   在 MVC 下，Controller 基本是无法测试的，里面混杂了个各种逻辑，而且分散在不同的地方。有了 MVVM 我们就可以测试里面的 viewModel，来验证我们的处理结果对不对（Xcode7 的测试已经越来越完善了）。

## 便于代码的移植

-   比如 iOS 里面有 iPhone 版本和 iPad 版本，除了交互展示不一样外，业务逻辑的 model 是一致的。这样，我们就可以以很小的代价去开发另一个 app。（以前做公司 iPad 的时候就深深感觉到，全部在 VC 里面是多么的痛苦和重新开发一个没有啥区别）。

## 兼容 MVC

-   MVVM 是 MVC 的一个升级版，目前的 MVC 也可以很快的转换到 MVVM 这个模式。VC 可以省去一大部分展示逻辑。

##

## 缺点：

**类会增多**

-   每个 VC 都附带一个 viewModel，类的数量\*2
-   viewModel 会越来越庞大
-   我们把逻辑给了 viewModel，那势必 Model 也会变得很复杂，里面的属性和方法越来越多。可能重写的方法比较多，因为涉及到一些数据的转换以及和 controller 之间的通信。

**调用复杂度增加**

-   由于数据都是从 viewModel 来，想想突然来了一个新人，一看代码，不知道真实的模型是谁。比如常用 tableview 的数据源，一般都是一个数组，如果不断的通过 viewModel 去取，沟通上没有那么直接。况且每封一层，意味着要写很多代码去融合他们的转换。

# 12 Vue Loader 处理资源路径

ck： [https://vue-loader.vuejs.org/zh/guide/asset-url.html#%E8%BD%AC%E6%8D%A2%E8%A7%84%E5%88%99](https://vue-loader.vuejs.org/zh/guide/asset-url.html#转换规则)

# 15 watch

**Vue 中对 watch 的理解（尤其是 immediate 和 deep 属性）:**

[**https://blog.csdn.net/qq_40323256/article/details/101907326**](https://blog.csdn.net/qq_40323256/article/details/101907326)

99 资源

[16 款优秀的 Vue UI 组件库推荐\_书写人生-CSDN 博客](https://blog.csdn.net/yelin042/article/details/104811844)
