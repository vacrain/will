# 常用命令 - commands

[toc]





## Linux

文件操作

```
创建文件
touch

解压
tar -zxvf xxxxxxxx.tar.gz
```

查看（文件类）

```
more
less
cat
```



查看（非文件类）

```
查看软件版本
>rpm -qa | grep java

查看内核版本
> arch

系统版本
> cat /etc/redhat-release
```

vim

```
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

> #### Win 需要管理员权限才能切换

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







## Misc 

### 生成目录结构

```
除了这个文件夹
> tree -I "node_modules"

只显示目录
> tree -d
```



