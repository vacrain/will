# Vue3 全家桶

[toc]

## Learn

### volar 插件安装完设置

Volar › Code Lens: Script Setup Tools 这个要打开

### vite.config.js 配置相关

vite.config.js 配置入门详解 https://www.jb51.net/article/236293.htm

### [pinia 对比 vuex ](https://blog.csdn.net/duninet/article/details/118945362)

### vite 创建、安装命令

创建 vue3 + vite 项目

```
pnpm create vite@latest
or
npm init @vitejs/app 项目名称
or
yarn create @vitejs/app 项目名称
```

安装依赖，按需安装

```
pnpm install @types/node

pnpm i -D naive-ui

pnpm install vue-router

// 这个vicons不太好用啊
pnpm i -D @vicons/fluent
pnpm i -D @vicons/ionicons4
pnpm i -D @vicons/ionicons5

pnpm install @iconify/vue


```

### 参考项目

### start

-   [x] vue 复习
    -   [x] [vue 基本语法](https://www.runoob.com/vue3/vue3-tutorial.html)
    -   [x] [csdn vue3](https://blog.csdn.net/qq1195566313/article/details/122768533?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165006722516780269878741%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=165006722516780269878741&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-1-122768533.142^v9^pc_search_result_cache,157^v4^control&utm_term=%E5%B0%8F%E6%BB%A1&spm=1018.2226.3001.4187)
    -   [ ] [vue3 新特性，b 站](https://www.bilibili.com/video/BV1dS4y1y7vd?p=7&spm_id_from=333.1007.top_right_bar_window_history.content.click) 不看了，太慢了，直接 clone 几个项目学
-   [ ] ui 选择、项目学习。选择标准：一个月内有人维护，样式还行，pc 和移动端可以用一套的
    -   [ ] vuetify，没有啥好项目
    -   [ ] element，没人维护了
    -   [ ] vant，vue3 支持不太好
    -   [x] naive

## Shit

### allowSyntheticDefaultImports

当 allowSyntheticDefaultImports 设置为 true 的时候，允许下面的导入：

`import React from "react";`
用来替代:

```
import * as React from "react";
```

### ts(2307)

vue vite ts Cannot find module or its corresponding type declarations.ts(2307)

vscode 里 f1 然后输入 select Typescript version，然后选 workspace，下面这俩最好都选上

![image-20220416105015389](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-04-16_10-50-15_image-20220416105015389.png)

### Volar - vue 终极开发神器！

Vue3 template 里不是必须要写一个 div 了

在使用前需要禁用 `vetur` 以避免冲突

可以这样说， `volar` 是 `vue3` 的配套，`vetur` 是 `vue2` 的配套，所以，建议大家在使用的时候依据自己使用的 `vue` 版本来选择。

https://juejin.cn/post/6966106927990308872

https://blog.csdn.net/qq_41800366/article/details/120363622

https://blog.csdn.net/weixin_48165407/article/details/124077516

### invalid host header

vue3 项目 启动完，访问主页，显示 invalid host header

下面是最新的，看别的没用！disableHostCheck 已经被取消了！

https://www.cnblogs.com/chenzilong/p/16065185.html

### TS 检查关闭

https://www.jianshu.com/p/ece127ffc996

### Vetur(6133)

vscode 文件报错：‘xxxx‘ is declared but its value is never read.Vetur(6133)

https://blog.csdn.net/qq_43869822/article/details/122350854

Vetur Validation: Script

取消打勾

再重新打开页面即可 (vue3 这边建议是直接卸载该插件，改用 volar)

<img src="https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-04-16_14-24-54_2022-04-16_06-01-11_image-20220416060111524.png" alt="image-20220416060111524" style="zoom:50%;" />
