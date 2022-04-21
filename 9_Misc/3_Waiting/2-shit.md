
# 踩过的坑

[toc]







## 基本常识



### 开源协议

https://zhuanlan.zhihu.com/p/51331026



### Git原理

这原理真没啥可说的。。照着教程啥的做一遍就啥都懂了

![](https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2022-04-14_19-26-57_988e1c532f632385f5d24627cce833e038725d7e.jpg)



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






## 无解问题

### mac 第三方中文输入法 vscode终端 大小写问题

vscode终端里用百度、搜狗这种输入法，按大写键切换中英文，会把中文切换到大写

2022-04-16 至今没有解决办法[Mac VS Code 命令行输入问题](https://segmentfault.com/q/1010000018329741)

改成shift切换吧，正好上班也是win系统。。





