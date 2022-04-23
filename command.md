# 常用命令 - commands

[toc]



## Misc 

### 生成目录结构

```
除了这个文件夹
> tree -I "node_modules"

只显示目录
> tree -d
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


