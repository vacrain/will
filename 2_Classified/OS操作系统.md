# OS 操作系统

[toc]

## Linux


### Linux命名坑

Linux系统里不能用中文命名文件，否则会出现大量未知的问题！！



### Linux安装软件记得加软连接

```
ln -s 目标软件 /usr/local/bin/软件名

或者 直接扔到bin里 : 
ln -s 目标软件 /usr/local/bin

```



### 软件包概念

分类

```
.rpm 是编译过后的包，也叫二进制包、RPM包、系统默认包 

源码包一般是 .c结尾
```

RPM包管理

```
包全名：
包名-版本-发布次数-适合的Linux平台-适合的硬件平台
noarch是任何都能安装

操作未安装的软件时，用 包全名
操作已安装的软件时，用 包名 即可


```

RMP包依赖性

```
树形依赖：a -> b -> c
环形依赖：a -> b ->c -> a
模块依赖：查询网站：www.rpmfind.net

```

安装命令

```
rpm 命令管理
rpm -ivh xxx.rpm
i	安装
v 显示安装信息
h	安装过程
-q 查询信息
-qR	查询依赖关系
-qf
-p	查询未安装的依赖包


如果没安装依赖包，会显示error，及提示安装依赖

```

yum在线管理

```
yum list
查看可安装的包

yum search 包名
sed -i -e '/mirrors.cloud.aliyuncs.com/d' -e '/mirrors.aliyuncs.com/d' /etc/yum.repos.d/CentOS-Base.repo
wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-8.repo

yum配置目录
/etc/yum.repos.d/
```





### Linux命令

- 命令格式： 命令 选项 参数，如 cat -n file1.html
- 通配符：
  - ?			匹配一个任意字符
  - \*           匹配0或多个
  - [abc]     匹配a或b或c
    - 如： ls \*abc   输出以abc结尾的文件名
- 执行顺序
  1. 绝对路径、相对路径
  2. 别名
  3. bash内部命令
  4. \$PATH 中定义的目录中查找到的第一个命令
- 快捷键
  - ctrl + c	终止当前命令
  - ctrl + L    清屏
  - ctrl + r    搜索历史命令
- 别名

```
alias vi='vim'
			快捷命令='原命令'
			命令行执行，只能临时生效，必须写入.bashrc文件才能永久生效

直接alias可以显示已有的别名指令

unalias 别名   	删除别名
```

常用

```
cd
pwd
ls
tab按键		自动补全

netstat -an		查看网络状态，listen表示监听，established表示正在连接

history  查看历史命令，历史命令存在 ~/.bash_history 文件中，缓存的不在这里

grep 	[选项] "搜索内容" 文件名  将文件中有搜索内容的行输出
	-i	忽略大小写
  -n	输出行号

!n		重复执行第n条历史命令
!!		重复执行上一条命令

rm -rf 

ctrl + c

umask		查看权限

date

cat /etc/redhat-release	查看当前centos版本  CentOS Linux release 8.2.2004 (Core)

mkdir -p /a/b/c		递归创建目录

tar -zxvf		解压

du -sh 文件夹名 文件夹大小

随意命令 > 文件名		随意命令的结果将写入文件，并删除文件原有内容
	双> 是添加
	单> 是覆盖

随意命令 2>> 文件名		将错误信息添加到文件中

命令1; 命令2  顺序执行
命令1 && 命令2 第一个正确执行，第二个才执行
命令1 || 命令2 第一个正确执行或不执行，第二个与第一个相反，比如第一个不执行，第二个就执行 

命令1 | 命令2   命令1的正确输出 作为 命令2的输入、参数
比如：命令1 | more


```

文件详细信息

```
ll
或者
ls -l

第一位：l是软连接（快捷方式）、d是目录、-是文件
第2-10位：作者、用户组、其他人的权限
	权限有三种，r、w、x，读、写、运行
再后面是： 计数、创建者、文件大小、最后修改时间、文件名、软连接还会显示指向目标

硬链接会完全复制，甚至同步更新，类似自动备份

```

复制

```
cp 文件或目录 目标目录
选项有 -r -p -rp
```

剪切、改名

```
mv
改名 mv 文件名1 文件名2
```

清屏

```
clear
或者快捷键 ctrl + L
```

创建文件

```
touch 文件名
```

查看文件、浏览文件

```
cat -n 文件名
-n 带行号

tac 文件名
倒着显示cat的内容

more 文件名
可以翻页，用空格或者f翻页，用回车一行一行翻
安q退出，非常常用，常用看帮助文档

less 文件名
和more一样，而且可以按pageup向上翻页
还能搜索内容，“/搜索的内容”，按 n 查找下一个

head -n 9 文件名
查看前9行，直接head 文件名，默认显示10行

tail -n 6 文件名
和head差不多，查看最后6行，默认10行
-f 动态显示末尾内容，常用查看日志

```

文件最后写一行内容

```
echo "xxxxxxxx" >> 文件地址
```

生成链接

```
软连接
ln -s 原文件 原文件.soft
硬链接
ln 原文件 原文件.hard

-s 软连接
不写-s 硬链接
硬链接不能跨区、不能指向目录
```

权限管理

```
权限修改
chmod

所有者修改
chown

```

搜索

```
find
locate 
which
whereis
apropos
```

帮助

```
man 命令名称
和more差不多
如：man date # 显示date命令的帮助信息

info 命令名称
和man差不多

help 命令名称、内置命令

1	命令的帮助
5	配置文件的帮助

命令 --help
获取命令的帮助
```

Vim 常见操作

```
vi 文件名
a、i、o 进入插入模式
:wq 退出
```

### Vim

```
i			插入
esc		退出编辑模式
:			准备执行命令和wq!等一起用
w			保存
q			退出
!			强制
```

### Nginx

购买的云服务器都自带yum 不用去折腾了，上传文件可以用各种工具上传，或者完全按照下面的安装方式也ok：

https://blog.csdn.net/weixin_50093343/article/details/116059305

保存目录

```
/usr/local/nginx
```

配置全局，通过创建软链接的方式实现

```
ln -s /usr/local/nginx/sbin/nginx /usr/local/bin/
```

修改配置文件，改写的都写全，不然问题大大的有

```
vi /usr/local/nginx/conf/nginx.conf
```

可用配置，不要乱改

```

worker_processes  1;

events {
    worker_connections  1024;
}

http {
    include       mime.types;
    default_type  application/octet-stream;
    sendfile        on;    
    keepalive_timeout  65;

    upstream vue_program{
    	server localhost:3000;
    }

    server {
        listen       80;
        server_name  localhost;

        location / {
            root   html;
            index  index.html index.htm;
            proxy_pass http://vue_program;
            proxy_redirect default;
        }

        location /vue3 {
            proxy_pass http://vue_program/;
	        proxy_redirect default;
        }

        location /birthday2019 {
                root    html;
                index  index.html index.htm;
        }

        location /img {
            root    /root/apps/static/; #root代表"/img/"中第一个"/"
        }

        error_page   500 502 503 504  /50x.html;
        
        location = /50x.html {
            root   html;
        }

    }

}
```



查看日志

```
tail -f /usr/local/nginx/logs/access.log
```

修改配置无法生效问题

重启电脑吧。。**重启也没用的话，那就是改错配置文件了**

可以用 whereis nginx 找到命令所在的文件夹  然后修改conf文件夹中的配置文件

日志 路径

/usr/local/nginx/logs/error.log



### yum安装、yum源问题

配置了好半天发现其实没有可以用的centos8的国内源，重置服务器吧，选一个7都行

https://blog.csdn.net/qq_43571807/article/details/122779470



### 监控文件数上限，npm run dev起不来项目

https://blog.csdn.net/lxyoucan/article/details/116736501

修改一下配置文件就好了

## Mac

### mac开机显示电量0%

https://www.somode.com/course/16989.html

1. 关机
2. 连接充电线
3. 同时按 **Shift+Control+Option和电源键**
4. 按下后，持续2s左右，松开这些按键。
5. 松开后，使用电源键打开电脑，就可以正常充电了。



### mac上 罗技鼠标 怎么设置

https://www.zhihu.com/question/28833060



### Mac连上了wifi无法上网

如果手机平板连上wifi都能正常使用, 电脑连上了却上不了网,
主要是因为换了WIFI, 要重新设置内网IP和DNS(如果之前自己手动设置过的话)

IP协议改成DHCP自动取内网IP
DNS解析地址都删了
之后就好了

