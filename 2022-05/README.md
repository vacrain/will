# Will-2022-05

[toc]

## Learned













### monorepo 策略说明

参考：https://segmentfault.com/a/1190000039157365

统一管理js项目，有点像是spring cloud，比它更好，小项目的话



### springboot是什么，一个图诠释



![什么是Spring Boot](https://raw.githubusercontent.com/vacrain/typora_img/main/2022/2022-05-24_09-31-52_1629261.png)



### 图床替换方案 Typora + picgo + gitee 改成 github

采用cdn代理，自定义格式：https://cdn.jsdelivr.net/gh/user/repo



用 vscode 打开笔记项目

```
把
gitee.com/vacrain/typora_img/raw/master
替换成
github.com/vacrain/typora_img/raw/main
```

![image-20220523070322361](https://cdn.jsdelivr.net/gh/vacrain/typora_img/2022/2022-05-23_07-03-22_image-20220523070322361.png)



参考：

https://zhuanlan.zhihu.com/p/353775844

https://zhuanlan.zhihu.com/p/76951130





### fira code 连字字体 vscode 安装及使用

1. https://github.com/tonsky/FiraCode
2. 打开上面的链接，然后点 Download & Install 下面的下载链接
    1. 或者https://github.com/tonsky/FiraCode/releases/download/6.2/Fira_Code_v6.2.zip
3. 解压缩后，里面有一个 ttf 文件夹，然后选择全部文件，进行安装，安装方式如下：
    1. win：右键，安装
    2. Mac：右键，打开方式，选择 fontbook.app
4. 在 vscode 中，打开设置，转成 json 格式进行编辑，粘贴下面代码在大括号里面即可

```
    "editor.fontFamily": "Fira Code",
    "editor.fontLigatures": true
```

### 英语口语面试

个人介绍

1. 个人 info
2. 学历
3. 工作经历
4. 项目介绍
5. 擅长、优点、为什么是我
6. 缺点、失误

### 2022/5/13 离职前记录一下自己用的工具

![image-20220513155150415](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2022/2022-05-13_15-52-00_image-20220513155150415.png)

### IDEA 创建 springboot 项目

idea 用不起，算了。。用 vscode

### IDEA、Pycharm、Webstorm 激活

https://idea.medeming.com/jihuoma/

日更的很快就失效了。。啧啧

![IDEA专用激活码（含永久激活）](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-05-12_21-18-07_IDEA%E4%B8%93%E7%94%A8%E6%BF%80%E6%B4%BB%E7%A0%81%EF%BC%88%E5%90%AB%E6%B0%B8%E4%B9%85%E6%BF%80%E6%B4%BB%EF%BC%89.jpg)

![Pycharm专用激活码（含永久激活）](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-05-12_21-18-27_Pycharm%E4%B8%93%E7%94%A8%E6%BF%80%E6%B4%BB%E7%A0%81%EF%BC%88%E5%90%AB%E6%B0%B8%E4%B9%85%E6%BF%80%E6%B4%BB%EF%BC%89.jpg)

![Webstorm专用激活码（含永久激活）](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-05-12_21-18-35_Webstorm%E4%B8%93%E7%94%A8%E6%BF%80%E6%B4%BB%E7%A0%81%EF%BC%88%E5%90%AB%E6%B0%B8%E4%B9%85%E6%BF%80%E6%B4%BB%EF%BC%89.jpg)

### mac or win 截图 并 贴图 显示在一边

https://zh.snipaste.com/

官网下载即可

基本使用：

-   F1 截屏
-   点击图钉按钮 📌 可以把截图直接显示在所有软件最顶层，可以来回移动~
-   esc 或 鼠标右键 退出
-   进入截图后，按 , 或 . 可以查看历史截图！

其他：

-   保存到剪贴板 ( ![img](https://www.snipaste.com/img/copy16.svg) / Ctrl + C / Enter / 双击 截屏区域)
-   保存到文件 ( ![img](https://www.snipaste.com/img/save16.svg) / Ctrl + S)
-   保存到贴图 ( ![img](https://www.snipaste.com/img/pin16.svg) / Ctrl + T)
-   快捷保存 (Shift + ![img](https://www.snipaste.com/img/save16.svg)/ Ctrl + Shift + S)

### eclipse debug 说明

https://baijiahao.baidu.com/s?id=1709030904973465262&wfr=spider&for=pc

### sts eclipse 上面 安装过的插件

Quick Search

MyBatis Generator

MyBatipse

JRebel

### mac 终端去掉 last login 消息

打开终端，直接输入

```shell
touch .hushlogin
```

关闭后重新打开就行~

### 搞开发还得是 win

开发还的是 win

数据库、Linux 啥的可以装虚拟机玩

mac 也就搞搞图、音乐、文档还行吧

### Nodejs 开发后端的好处

天然支持 json！！！

### 腾讯云开放 3306 端口 不必关防火墙啥的

点进云服务器，点防火墙

添加规则，选 3306mysql ，确定完成即可！

### 开发体验影响因素 简单总结

1. logger
2. debug
3. exception
4. aop
5. 类型提示，静态语言
6. 代码提示
7. 代码格式化

8. mvc
9. orm
10. http
11. 分页
12. mysql （有了 http 自然有这个能力）
13.

### vscode debug npm 项目

在要 debug 的代码行号左边点一下小圆点：![image-20220508171927050](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-05-08_17-19-27_image-20220508171927050.png)

然后 debug 启动方式：

![image-20220508171841538](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-05-08_17-18-41_image-20220508171841538.png)

乐哈哈了就

![image-20220508172121622](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-05-08_17-21-21_image-20220508172121622.png)

### Mac ssh ftp 远程连接 Linux 神器 electerm

win 上有一个叫 m 啥的，很好用，可惜没有 mac 版

不过 mac 上也有好用的开源软件 electerm，省去下载过程，github 自己找一下

下面是新建连接过程：（**鼠标放在 + 上即可！不用点**）

![image-20220508170703006](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-05-08_17-07-03_image-20220508170703006.png)

依次填写 ip、user、password，然后 test 一下，ok 了，还是上面那个图，鼠标**放在** + 上即可，就能看见啦，可以随意切换 ssh 和 sftp

![image-20220508171038231](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-05-08_17-10-38_image-20220508171038231.png)

### vscode 新项目 直接 git push 到新仓库 repo

初始化：

```
git init
touch .gitignore
```

```
.gitignore文件里写入：

# Logs
logs
*.log
npm-debug.log*
yarn-debug.log*
yarn-error.log*
pnpm-debug.log*
lerna-debug.log*

node_modules
.DS_Store
dist
dist-ssr
coverage
*.local
stats.html

/cypress/videos/
/cypress/screenshots/

# Editor directories and files
.vscode/*
!.vscode/extensions.json
!.vscode/settings.json
.idea
*.suo
*.ntvs*
*.njsproj
*.sln
*.sw?
```

提交到本地

```
git add .
git commit -m "xxxx初体验~"
```

提交到 github 新仓库：

1. vscode 可以登录 github，登录上，在左下角那个小人那
2. 确认一下安装了 gitlens 插件，就第一个，现在有 1400 多万下载了
3. 确认已经 commit 完了，打开侧边栏![image-20220508170403040](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-05-08_17-04-03_image-20220508170403040.png)
4. 然后点蓝色图标（其实就是 push）
5. 选一下提交到私有还是 public 就完事了

### Linux 7.6 安装 mysql8

**步骤实在太多，不想写了（还是写了，太不容易了，看似只是安装个 mysql，把 Linux 命令全复习了一遍），没有 Linux 基础不能搞啊！！！**

有基础的直接参考：[Linux7.6 二进制安装 Mysql8.0.27_IT 邦德的博客-CSDN 博客](https://blog.csdn.net/weixin_41645135/article/details/121526797?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165200295016781683955682%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fblog.%2522%257D&request_id=165200295016781683955682&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~blog~first_rank_ecpm_v1~rank_v31_ecpm-3-121526797-null-null.nonecase&utm_term=linux&spm=1018.2226.3001.4450)

**注意！！** 版本可能不太一样，不能直接复制这位老哥的命令哈！比如我现在的 mysql 版本就是 8.0.29 那位老哥是 27

开搞开搞！

#### 确认一下环境

```
> cat /etc/redhat-release
CentOS Linux release 7.6.1810 (Core)

> df -TH
Filesystem     Type      Size  Used Avail Use% Mounted on
devtmpfs       devtmpfs  952M     0  952M   0% /dev
tmpfs          tmpfs     964M   50k  964M   1% /dev/shm
tmpfs          tmpfs     964M  586k  963M   1% /run
tmpfs          tmpfs     964M     0  964M   0% /sys/fs/cgroup
/dev/vda1      ext4       43G   13G   29G  30% /
tmpfs          tmpfs     193M     0  193M   0% /run/user/0

> cat /etc/hosts
127.0.0.1 VM-16-5-centos VM-16-5-centos
127.0.0.1 localhost.localdomain localhost
127.0.0.1 localhost4.localdomain4 localhost4
::1 VM-16-5-centos VM-16-5-centos
::1 localhost.localdomain localhost
::1 localhost6.localdomain6 localhost6

> hostname
VM-16-5-centos

卸载MariaDB
查看：
> rpm -qa |grep mariadb
这个命令会出现软件包全名（可能版本和你的不一样）：mariadb-libs-5.5.60-1.el7_5.x86_64
然后卸载：
> rpm -e --nodeps mariadb-libs-5.5.60-1.el7_5.x86_64

yum准备好咯
能来安mysql这玩意应该都没问题吧。。配置源就略过了哈

```

#### 创建目录、用户组

```
注：可以部署多个实例，通过端口区分root 用户操作

创建目录
mkdir -p /mysql/data/mysql3306
mkdir -p /mysql/app/
mkdir -p /mysql/conf/
mkdir -p /mysql/data/mysql3306/pid/
mkdir -p /mysql/data/mysql3306/socket/
mkdir -p /mysql/data/mysql3306/log/
mkdir -p /mysql/data/mysql3306/binlog/
mkdir -p /mysql/data/mysql3306/errlog
mkdir -p /mysql/data/mysql3306/relaylog/
mkdir -p /mysql/data/mysql3306/slowlog/
mkdir -p /mysql/data/mysql3306/tmp/

用户组：
groupadd mysql
useradd -g mysql mysql

授权、改密码
chown -R mysql:mysql /mysql
passwd mysql

查看：
cat /etc/group | grep mysql
cat /etc/passwd | grep mysql

切换成mysql用户操作
su - mysql
```

#### 下载 mysql8

打开官网 https://dev.mysql.com/downloads/mysql/

照着选：

![image-20220508202914306](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-05-08_20-29-14_image-20220508202914306.png)

然后下载第一个，**Compressed TAR Archive**

今天是 2022-05-08 ，我下载的是 8.0.29 ，大小 515.1M

#### 上传并安装

上传操作省略，各种 sftp 骚操作一下

```
复制到/mysql/app
> cp 你上传的那个压缩包.tar.xz /mysql/app

来到mysql软件安装目录
> cd /mysql/app

md5验证一下，以免有坏蛋加塞病毒
> md5sum 你复制过来那个压缩包.tar.xz
验证完：
13bb219c9ab74b3c8ea8c41c204cbef4  mysql-8.0.29-linux-glibc2.12-x86_64.tar.xz

解压软件包
> tar xvf 你复制过来那个压缩包.tar.xz

重命名
> mv 解压完的目录名 mysql8.0.29

查看一下
> ls
应该是一个压缩包、一个目录
把压缩包删了
> rm 压缩包名.tar.xz

配置环境变量，好些个方法，我比较喜欢vim 或者直接通过远程工具打开文件编辑
/home/mysql/.bash_profile 文件最后加上：
MYSQL_HOME=/mysql/app/mysql8.0.27
PATH=$PATH:$HOME/.local/bin:$HOME/bin:$MYSQL_HOME/bin

刷新配置
source ~/.bash_profile

查看命令位置
which mysql

```

#### 填写配置文件

用 vim 或者小骚工具都行，把下面内容整进 /mysql/conf/my3306.cnf ，第一行必须是[mysqld]

```
[mysqld]
server_id = 80273306
default-storage-engine= InnoDB
basedir=/mysql/app/mysql8.0.29  # 这个要自己改一下哈！！
datadir=/mysql/data/mysql3306/data/
socket=/mysql/data/mysql3306/socket/mysql.sock
log-error=/mysql/data/mysql3306/log/mysqld.log
pid-file=/mysql/data/mysql3306/pid/mysqld.pid
port=3306
default-time_zone='+8:00'
default_authentication_plugin=mysql_native_password
transaction_isolation=READ-COMMITTED
max_connections=1500
back_log=500
wait_timeout=1800
max_user_connections=800
innodb_buffer_pool_size=1024M
innodb_log_file_size=512M
innodb_log_buffer_size=40M
slow_query_log=ON
long_query_time=5

slow_query_log = ON
slow_query_log_file = /mysql/data/mysql3306/slowlog/slow3306.log
log_error = /mysql/data/mysql3306/errlog/err3306.log
log_error_verbosity = 3
log_bin = /mysql/data/mysql3306/binlog/mysql_bin
log_bin_index = /mysql/data/mysql3306/binlog/mysql_binlog.index
general_log_file = /data/mysql/mysql3306/generallog/general.log
log_queries_not_using_indexes = 1
log_slow_admin_statements = 1
expire_logs_days = 90
binlog_expire_logs_seconds = 2592000
long_query_time = 2
min_examined_row_limit = 100
log_throttle_queries_not_using_indexes = 1000
innodb_flush_log_at_trx_commit=1
```

#### 数据库初始化

下面的 mysql8.0.29 看看和自己版本能对上不，可能需要改改

```
mysqld --defaults-file=/mysql/conf/my3306.cnf --initialize --user=mysql --basedir=/mysql/app/mysql8.0.29 --datadir=/mysql/data/mysql3306/data/
```

#### 查看密码

```
cat /mysql/data/mysql3306/errlog/err3306.log | grep localhost

上面命令执行完，应该就会显示一行，在 root@localhost: 后面 就是密码，我的是：
l?)<I,SYP2M%
```

#### 启动

```
mysqld_safe --defaults-file=/mysql/conf/my3306.cnf --user=mysql &
```

#### 登录

执行完把初始化得到的奇怪密码粘贴进去即可，**登录完别退出，直接去改密码**

```
mysql -uroot -p  -P 3306 -S /mysql/data/mysql3306/socket/mysql.sock
```

#### 改本地登录密码

```
alter user root@'localhost' identified by '你自己编一个密码';

没事闲的也可以看看mysql状态：
status
```

#### 远程登陆设置

```
使用如下语句创建 root 用户是无法通过 navicat 等客户端登录的，
由于从 MySQL8 开始，身份验证插件发生改变，
默认的 “caching_sha2_password” 不允许远程登录，
故需将此插件修改为 “mysql_native_password” 便可登录。

mysql> create user root@'%' identified with mysql_native_password by '再编一个密码';
mysql> grant all on *.* to root@'%' with grant option;
mysql> flush privileges;

查看mysql用户，里面有一个root 后面是% ，这就是可以远程登录的用户
mysql> select user,host,plugin from mysql.user;

如果想修改远程登录密码:
mysql> alter user root@'%' identified by '再再编一个密码';
```

#### 远程登录

填写 ip、user、密码，都是上面设置的

user 是 root，如果你没写别的话

#### 退出 Bye

```
quit
```

![image-20220508201250794](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-05-08_20-12-50_image-20220508201250794.png)

### github 实用 小技巧

1. 高级搜索

进入 github，按 s 会自动聚焦到搜索框，然后直接回车，再选择 [advanced search](https://github.com/search/advanced)

2. 查找仓库内文件

打开指定仓库，按 t，可以找文件

打开指定文件后，按 L，可以跳到指定行数 ，按 B，可以查看变动记录

点击行号，还可以复制或生成连接

3. 在线 vscode

打开指定仓库，按下句号即可

### mysql、mongodb、redis 根据场景选择

一般就都得带上 mysql

日志、评论等疯狂写入大数据量的用芒果

redis 缓存 token、今日新闻啥的，给 mysql 顶一下短期不变的数据

### vscode 快捷打开文件

com + p

or

ctrl + p

然后写文件名即可

### 一般指令 命令行查看 使用方式

下面以 npm 指令为例

```
直接终端运行 npm

然后会有一堆选项 ，比如 install、run等
最后会有一个help <term> 这个就是可以详细介绍一个选项如何使用
如：npm help run  可以给出npm run的使用方式

退出方式：写个q就行 quit的意思
```

### vscode 智能 js 提示 插件 TabNine.tabnine-vscode

https://marketplace.visualstudio.com/items?itemName=TabNine.tabnine-vscode

就安完正常打代码会发现提示更加智能了！

有的是在代码下方提示，按上下键选择，回车选择，有的是在代码后面，按 tab 健可以自动补全

### js vscode 函数 注释 添加类型

示例：

```

/**
 * @description:
 * @param {import('fastify').FastifyInstance} fastify
 * @param {*} opts
 * @return {*}
 */
export default async function (fastify, opts) {
    fastify.get("/test1", async (req, reply) => {
        reply.code(200).send("got test1 route");
    });
}
```

### vscode 添加代码模板 快捷剪头函数

首选项（preference）> 用户片段（user snipetts） > 新建全局（global）

起名叫 ES6-snipetts 吧，随便起名，自己能认识就 ok

清空文件，下面的粘进去，保存就 ok 了

```
{
    "箭头函数": {
        //代码片段名称
        "prefix": "ff", //快捷键唤醒代码片段 可以自己设置成别的
        "body": [
            //body里面的内容就是代码段内容
            "($1) => {$2}" // $1和$2为占位符
        ],
        "description": "Arrow Function" //代码片段的介绍描述
    }
}

```

测试：随便打开一个文件，按 ff 就有提示了

### npm 镜像 源 配置 nrm 源管理工具

通过 nrm

```
npm install nrm -g

查看源，比如淘宝的 http://registry.npm.taobao.org  官方的 http://www.npmjs.org
nrm ls

nrm use xxxxx
```

或者知道域名的话，直接配置：

```
npm install --registry=[源地址]
```

或者修改配置文件 .npmrc（mac 端的在 ~ 目录，win 的找找吧，应该在 user 里），或者直接在当前项目中创建也是 ok 的

```
# .npmrc

# 通用的
registry=[源地址]

# 专门的
electron_mirror=https://npm.taobao.org/mirrors/electron/
```

### Alpha、Beta、RC 版本说明

Alpha、Beta、RC（release candidate）分别是内测、公测 和 发布候选版本

α、β、λ 常用来表示软件测试 过程中的三个阶段，α 是第一阶段，一般只供内部测试使用；β 是第二个阶段，已经消除了软件中大部分的不完善之处，但仍有可能还存在缺陷和漏洞，一般只提供给特定的用户群来测试使用；λ 是第三个阶段，此时产品已经相当成熟，只需在个别地方再做进一步的优化处理即可上市发行。

### chrome debug 技巧

重发请求，这有一种简单到发指的方式。

1. 选中`Network`
2. 点击`Fetch/XHR`
3. 选择要重新发送的请求
4. 右键选择`Replay XHR`

在控制台快速发起请求

还是联调或修 BUG 的场景，针对同样的请求，有时候需要**修改入参**重新发起，有啥快捷方式？

1. 选中`Network`
2. 点击`Fetch/XHR`
3. 选择`Copy as fetch`
4. 控制台粘贴代码
5. 修改参数，回车搞定

调试网页时通过`Elements`面板选中元素后，如果想通过`JS`知道它的一些属性，如`宽`、`高`、`位置`等怎么办呢？

1. 通过`Elements`选择要调试的元素
2. 控制台直接用`$0`访问

使用`$_`引用上一次操作的结果，不用每次都复制一遍

```javascript
// 第1步
"fatfish".split(""); // ['f', 'a', 't', 'f', 'i', 's', 'h']
// 第2步
$_.reverse(); // ['h', 's', 'i', 'f', 't', 'a', 'f']
// 第3步
$_.join(""); // hsiftaf
```

### vueuse/core

一个工具包吧算是：https://www.npmjs.com/package/@vueuse/core

```
pnpm i @vueuse/core
```

安装完使用，比如复制功能：

```
// 某某vue文件里

// template里
<input v-model:value="source" placeholder="请输入要复制的内容吧" />

// js部分
import { useClipboard } from '@vueuse/core';
const { copy, isSupported } = useClipboard();

function handleCopy() {
  if (!isSupported) {
    window.$message?.error('您的浏览器不支持Clipboard API');
    return;
  }
  if (!source.value) {
    window.$message?.error('请输入要复制的内容');
    return;
  }
  copy(source.value);
  window.$message?.success(`复制成功：${source.value}`);
}
```

其他玩法：

https://blog.csdn.net/xgangzai/article/details/122677773

### 备案号放置

备案成功后会收到短信提示：

**根据工信部要求：已通过备案的用户，在网站开通时应在网站首页底部放置正确的备案号，并链接到工信部网址：beian.miit.gov.cn，供公众查询核对。**

就是在底部放个链接即可，类似这样的：

```
<a href="https://beian.miit.gov.cn/" target="_blank">蜀ICP备XXXXX号-X</a>
```

### 魔改 typora 的大纲

还不太行，而且这个是把大纲整右边去了

参考：

https://github.com/XiLaiTL/typora-theme-bothview-tabbar

![header](https://github.com/vacrain/typora_img/raw/main/assets/imgs/2021/2022-05-06_19-43-56_bothview-tabbar.jpg)

### Angular 提交规范、commitlint、git-cz 辅助提交工具

开源社区的大项目，一般使用的是 Angular 的提交规范

使用 commitlint 可以规范我们每一次的 commit，我们可以用来自动生成 changeLog 等文件，方便代码管理。

-   Angular 的提交规范（例：fix(account): 修复 xxx 的 bug ）

```
<type>(<scope>): <subject>  // 这都是header
// 空一行
<body>
// 空一行
<footer>

第一行是Header，是必需的
Body 和 Footer 是可以省略
Header中，type、subject是必须的，scope是可省略的

type 只能是下面其中之一：
  'feat', // 新特性、新功能（feature）
  'fix', // 修bug
  'style', // 代码格式修改,代码格式化，注意不是 css 修改（不影响代码运行的变动）
  'chore', // 构建过程或辅助工具的变动
  'docs', // 文档构建与修改
  'conf', // 配置文件修改
  'refactor', // 代码重构（即不是新增功能，也不是修改bug的代码变动）
  'test', // 增加测试、测试用例修改
  'perf', // 优化相关，比如提升性能、体验

scope 是提交代码涉及的领域、影响的范围
	比如后端的controller、service、database，前端的views、config等等

subject是对  此次提交内容的简短描述，需要自己编，啊不，写

Body 是对本次 commit 的详细描述，可以分成多行，一般就懒的写

Footer 有两种情况
1. 当前提交会产生不兼容反应，应该补充兼容方法，以BREAKING CHANGE开头
2. 关闭issue，例：Closes #123, #245, #992，

还有一种特殊情况，恢复之前的某次提交，以revert开头，后面是被恢复的那次提交信息的header
例：revert: type(scope):  some comment
This reverts commit bfe307ce57d87677c6c473c228e6c2ed8b81dcec.
```

> 上面这些提交规范，因为规范只是口头上的，需要工具来约束，于是有了 commitlint/cli、git-cz 之类的提交工具

-   安装及配置

```
全局安装git-cz
> npm install -g git-cz

项目中使用commitlint：
> pnpm install --save-dev @commitlint/config-conventional @commitlint/cli

根目录创建一个文件.commitlintrc.js，里面加入：
module.exports = {
    extends: ['@commitlint/config-conventional'],

    rules: {
        'type-enum': [
            2,
            'always',
            [
                'feat', // 新特性、新功能（feature）
                'fix', // 修bug
                'style', // 代码格式修改,代码格式化，注意不是 css 修改（不影响代码运行的变动）
                'chore', // 构建过程或辅助工具的变动
                'docs', // 文档构建与修改
                'conf', // 配置文件修改
                'refactor', // 代码重构（即不是新增功能，也不是修改bug的代码变动）
                'test', // 增加测试、测试用例修改
                'perf', // 优化相关，比如提升性能、体验
            ],
        ],

        'header-max-length': [2, 'never', 72], // header 最长72

        'type-empty': [2, 'never'], // <type> 不能为空
        'type-case': [2, 'always', 'lower-case'], // <type>格式小写

        // 'scope-empty': [2, 'never'], // <scope> 不能为空
        'scope-case': [2, 'always', 'lower-case'], // <scope> 格式 小写

        // <subject> 格式
        // 可选值
        // 'lower-case' 小写 lowercase
        // 'upper-case' 大写 UPPERCASE
        // 'camel-case' 小驼峰 camelCase
        // 'kebab-case' 短横线 kebab-case
        // 'pascal-case' 大驼峰 PascalCase
        // 'sentence-case' 首字母大写 Sentence case
        // 'snake-case' 下划线 snake_case
        // 'start-case' 所有首字母大写 start-case
        'subject-empty': [2, 'never'], // <subject> 不能为空
        'subject-full-stop': [2, 'never', '.'], // <subject> 以.为结束标志
        'subject-case': [2, 'never', []],

        'body-leading-blank': [2, 'always'], // body换行

        'footer-leading-blank': [1, 'always'], // <footer> 以空行开头
    },
}


还要为 git 配置 husky ，对 git 的 commit 操作进行校验
husky继承了Git下所有的钩子，在触发钩子的时候，husky可以阻止不合法的commit，push等等
！！！安装一定要是4.3.8版本的，现在最新是7.x.y，7代的不好用，拦截不下来（ctmd血坑
> pnpm install husky@4.3.8 --save-dev


package.json里面引入husky。。下面这段配置告诉了git hooks，当我们在当前项目中执行 git commit -m '测试提交' 时将触发commit-msg事件钩子并通知husky，从而执行 commitlint -E HUSKY_GIT_PARAMS命令
也就是我们刚开始安装的./node_modules/.bin/commitlint，它将读取commitlint.config.js配置规则并对我们刚刚提交的测试提交这串文字进行校验，若校验不通过，则在终端输出错误，commit终止。
{
  ...
  ...
  "husky": {
    "hooks": {
      "commit-msg": "commitlint -E HUSKY_GIT_PARAMS"
    }
  }
}

这是最后一步了，坚持一下，马上就能用了
git-cz的提示信息也要配置一下，项目根目录创建文件changelog.config.js，然后写入：
module.exports = {
    disableEmoji: false,
    format: '{type}{scope}: {emoji}{subject}',
    list: [
        'feat', // 新特性、新功能（feature）
        'fix', // 修bug
        'chore', // 构建过程或辅助工具的变动
        'docs', // 文档构建与修改
        'style', // 代码格式修改,代码格式化，注意不是 css 修改（不影响代码运行的变动）
        'perf', // 优化相关，比如提升性能、体验
        'refactor', // 代码重构（即不是新增功能，也不是修改bug的代码变动）
        'ci', // 自动集成
        'test', // 增加测试、测试用例修改
    ],
    maxMessageLength: 64,
    minMessageLength: 3,
    questions: [
        'type',
        'scope',
        'subject',
        // 'body',
        // 'breaking',
        // 'issues',
        // 'lerna',
    ],
    scopes: ['', 'config', 'router', 'dependence'],
    types: {
        chore: {
            description: 'Build process or auxiliary tool changes',
            emoji: '🛠',
            value: 'chore',
        },
        ci: {
            description: 'CI related changes',
            emoji: '🎡',
            value: 'ci',
        },
        docs: {
            description: 'Documentation only changes',
            emoji: '✏️',
            value: 'docs',
        },
        feat: {
            description: 'A new feature',
            emoji: '🎸',
            value: 'feat',
        },
        fix: {
            description: 'A bug fix',
            emoji: '🐛',
            value: 'fix',
        },
        perf: {
            description: 'A code change that improves performance',
            emoji: '⚡️',
            value: 'perf',
        },
        refactor: {
            description:
                'A code change that neither fixes a bug or adds a feature',
            emoji: '💡',
            value: 'refactor',
        },
        release: {
            description: 'Create a release commit',
            emoji: '🏹',
            value: 'release',
        },
        style: {
            description:
                'Markup, white-space, formatting, missing semi-colons...',
            emoji: '💄',
            value: 'style',
        },
        test: {
            description: 'Adding missing tests',
            emoji: '💍',
            value: 'test',
        },
    },
}


```

-   使用

```
香香时刻到，在要提交的时候，只需要一个命令，然后按照提示选择、填写提交信息即可！！
> git-cz
```

### HhuilderX Vscode 跳到 变量定义处

> 不同的编辑器里不太一样，自己试吧

alt + 左键

ctrl + 左键

command + 左键


### 辽宁企业登记实名验证活体检测 一直不出摄像是什么原因？

手机的时间不准确，关闭一下自动同步时间，再开启就好了