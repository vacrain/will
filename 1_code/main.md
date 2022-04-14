# menu

[toc]

# Todo

## 环境准备

### 博客

- [X] 知乎专栏
- [X] 公众号
- [X] b站
- [X] 开发学习记录，保存到一个平台，git
- [ ] 



### 域名

- [X] 选购
- [X] 实名
- [ ] 实名成功3天后，备案
- [ ] dns解析
- [ ] https
- [ ] 



### 服务器

- [ ] ~~mac 系统下 Iterm2下载安装，设置，连接服务器~~
- [ ] ci/cd 环境搭建
  - [ ] GitHub action
  - [ ] Jskin+webhook
- [X] 玩坏了，重装系统：https://boke112.com/post/7841.html
- [X] 服务器选择、租
- [X] 服务器IP ： http://101.43.138.54/

```
101.43.138.54
ssh root@101.43.138.54
```

- [X] vscode 通过ssh远程连接Linux 服务器 https://blog.csdn.net/zhaxun/article/details/120568402
- [X] 安装node
- [X] 安装git https://www.imooc.com/article/44583  解压后少了一步，进入文件夹 cd git文件夹

<img src="https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2022-04-11_21-35-10_WX20220410-101307@2x.png" alt="WX20220410-101307@2x" style="zoom:25%;" />

- [X] 重置密码
- [X] MobaXterm下载安装

  - [X] 设置键盘，可以粘贴
  - [X] ssh连接服务器
  - [X] ftp功能 https://cloud.tencent.com/developer/article/1974355
- [X] yum

  - [ ] http://mirrors.163.com/centos/8-stream/BaseOS/x86_64/os/Packages/  在这个网站找自己对应版本的yum进行安装

    - [ ] 比如，我的是8.2，那就在 http://mirrors.163.com/centos 找 8
    - [ ] 来到http://mirrors.163.com/centos/8-stream/
    - [ ] 再找os，再找64编码的，然后packages，里面搜索 yum ，右键第一个链接， 复制链接
    - [ ] 最后在服务器终端中输入： rpm -ivh 加上刚复制的链接
  - [ ] 安装完查看版本：yum --version

  - ```
    下面的 Centos-7 根据自己的版本号来，我是8.2所以写成Centos-8就行
    wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
    ```

## 技术准备

### centos 服务器

- [X] Linux 学习，b站兄弟连视频
- [X] 基本命令
- [X] 包概念，yum概念

- 前端复习

- [X] vue复习
  - [X] [vue基本语法](https://www.runoob.com/vue3/vue3-tutorial.html)
  - [ ] vue3基础学习，b站
- [ ] ui选择、项目学习
  - [ ] 选择标准：一个月内有人维护，样式还行，pc和移动端可以用一套的
  - [ ] vuetify
  - [ ] element
  - [ ] vant
  - [ ]

### 后端服务器

- [ ] mysql复习
  - [ ] 安装、远程连接
  - [ ]
- [ ] spring全家桶复习
  - [ ] springboot搭建
  - [ ]

### 工具

- [X] [vscode自动格式化](https://baijiahao.baidu.com/s?id=1704599223959464441&wfr=spider&for=pc)
- [X] idea激活
- [X] ftp 文件系统连接远程服务器
- [X] shell远程连接
- [ ] vscode 实现所见即所得 markdown编辑器
  - [ ] Office Viewer 很多人强烈推荐的替代typora的插件！
    - [ ] 实际上远不及Typora，不太建议了
- [ ] 取消Windows搜索文件工具 everything

- 其他

- [ ] 测试驱动开发学习
- [ ] 敏捷开发
- [ ] CI/CD

## schedule

- [ ] demo

  - [ ] 单次todo
  - [ ] 循环todo
  - [ ] 主题显示、调整
  - [ ] 日记
- [ ] 框架、数据库搭建
- [ ] 本地开发

  - [ ] 0.1.1 提醒功能
    - [ ] 添加提醒
  - [ ] 0.2.1 日记功能
  - [ ] 0.3.1 todo-日记功能
  - [ ] 0.4.1 主题功能
  - [ ] 0.5.1 导出功能
  - [ ] 0.6.1 日历功能
