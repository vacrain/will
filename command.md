# 常用命令 - commands

[toc]



## tools



### Git

```
git-cz

git log - 查看历史提交记录。
git blame <file> - 以列表形式查看指定文件的历史修改记录。
git log --reverse --oneline

```



### jenkins

```
基本使用 
service jenkins 后面可以加start、stop、status、restart

修改配置文件
vi /etc/sysconfig/jenkins

配置重载
systemctl daemon-reload

systemctl启动，检查状态
systemctl start jenkins
systemctl enable jenkins
systemctl status jenkins.service
```



### nginx

```
配置文件（不建议使用vi，这玩意有点多，还是用vscode或者其他编辑器远程 编辑）
vi /usr/local/nginx/conf/nginx.conf

检查配置文件格式
nginx -t

其他
nginx -s reload
nginx -s quit
nginx -s stop
```



## Linux

### 生成目录结构

```
除了这个文件夹
> tree -I "node_modules"

只显示目录
> tree -d
```





### 文件/软件包 操作

```



创建文件
touch

卸载
rpm -e 包名

解压
tar -zxvf xxxxxxxx.tar.gz
```

### 查看（文件内容类）

```
more
less
cat
```



### 查看（非文件内容）

```






看rpm包，安装的详细路径
rpm -ql +包名

网络,查询指定端口号情况
> netstat -tnlp | grep :80

环境变量
> echo $PATH

查看软件版本
>rpm -qa | grep java

查看内核版本
> arch

文件系统  容量  已用  可用  已用占比   挂载点
> df -h

最占地方的文件是谁
du -sh *

查询系统日志的工具
> journalctl -xe

系统版本
> cat /etc/redhat-release
```

### vim

```
剪切当前行
dd

粘贴
p

编辑
i

退出
q

保存
w

跳到最后，一定是大写的，shif
G

```



## Node

### win 切换 node版本用的 NVM

> #### Win 需要管理员权限才能切换 ！ ！ ！

```
nvm list
nvm use [version]

nvm root
```



## Mac





### mac安装软件打不开

比如vscode安装完，移动到应用里，然后终端输入下面代码即可

```
xattr -d com.apple.quarantine /Applications/Visual\ Studio\ Code.app
```

其他类似的也一样

```
xattr -d com.apple.quarantine /Applications/软件名.app
xattr -d com.apple.quarantine /Applications/Sublime\ Text.app
```





### Mac os 文件隐藏与显示

在终端中输代码,即可显示隐藏文件。

```
defaults write com.apple.finder AppleShowAllFiles -boolean true;killall Finder
```

再次隐藏文件，可以输入命令

```
defaults write com.apple.finder AppleShowAllFiles -boolean false;killall Finder
```





