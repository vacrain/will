# Main ！

[toc]



## Temp



### tarui初体验

参考：https://www.jianshu.com/p/71a4054e0b58

这个类似electron，打包大小胎心动了！

安装过程，略长，徐耐心、、、

```
假设有node环境，么有rust环境~

1. 创建项目
> yarn create @umijs/umi-app

安装依赖
> yarn

安装rust环境
> curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

上一步会显示：
1) Proceed with installation (default)
2) Customize installation
3) Cancel installation
输入1即可：
> 1

然后又是漫长的等待...
最后显示 Rust is installed now. Great! 就是好了 
继续梭哈：
> source $HOME/.cargo/env

这就算配置好了，查看版本，看好是 rustc ccccccc带上c，无语。。。找了半天，以为安装错位置了
> rustc -V

查看包管理器
> cargo -V

注意：使用vscode编辑rust时需要安装c/c++扩展才能正常启动调试器

全局安装rust打包工具，在这个过程中可能会报某些包没有，不要慌，缺什么就安装什么。。。这个也挺慢的...开封菜这wifi太慢了，用流量，芜湖！起飞！
> cargo install tauri-bundler --force

5分钟终于搞定了：
    Finished release [optimized] target(s) in 5m 57s
  Installing /Users/wangxiansheng/.cargo/bin/cargo-tauri-bundler
   Installed package `tauri-bundler v0.9.4` (executable `cargo-tauri-bundler`)
```

使用wifi和流量下载速度对比：![image-20220420193630022](https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2022-04-20_19-36-30_image-20220420193630022.png)

使用tauri

```
在直接在当前项目下 执行
> yarn add tauri -S
或者
> npm install tauri -S

初始化..一样，初始化过程中，如果报错缺少什么模块，缺什么装什么。。这个也很慢。。这个真的非常非常慢！！
> npx tauri init

输出如下：
[tauri]: running init
? What is your app name? tauri-001
? What should the window title be? tauri-test-001
? What is the url of your dev server? http://localhost:4000
? Where are your web assets (HTML/CSS/JS) located, relative to the "<current dir>/src-tauri" folder that will be created? ../di
st
 dependency:manager Installing missing dependencies... +0ms
 dependency:cargo-commands "tauri-bundler" is already installed +2s
 app:spawn [sync] Running "cargo generate-lockfile" +3ms

    Updating crates.io index

等了好一会告诉我没网了：
warning: spurious network error (2 tries remaining): SecureTransport error: connection closed via error; class=Net (12)



执行完成，会自动生成一个 rust 项目 src-tauri
src-tauri/tauri.conf.json文件内容：
  "build": {
      "distDir": "../build", //打包后的路径
      "devPath": "http://localhost:8080", // 此为 dev 启动时的url
      "beforeDevCommand": "",
      "beforeBuildCommand": ""
    },
配置package.json
  scripts:{
    ...
    "start": "concurrently \"npm run start:web\"  \"npm run start:tauri\"",
    "start:web": "umi dev",
    "start:tauri": "tauri dev",
    "build": "npm run build:web &&  npm run build:tauri",
    "build:web": "umi build",
    "build:tauri": "tauri build",
    ...
  }

再按一次依赖 npm就npm i 用yarn就yarn

依赖安装运行..这时，cargo 会给 rust 项目安装依赖。过程会比较慢，有可能会因为网络问题导致安装失败，不要慌，多尝试几次。安装完成后。ctrl+c 推出，然后再使用 npm run start 一次性启动整个项目
> npm run start:tauri
```













