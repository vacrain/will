[toc]

# 常用快捷键 - shortcuts

## Common

### 文本编辑

全局搜索：ctrl + shift + F

选中当前位置的单词：ctrl + D



### 其他



## Vscode

### 常用

1. 聚焦到文件树： ctrl/com + shift + E
   1. 聚焦后，可以直接输入部分文件名进行快速锁定文件，进行操作
2. 打开终端：ctrl + \`
3. 打开设置：ctrl/com + ,



### 注释 koro1FileHeader

函数注释 快捷键：(对剪头函数不是很友好)

- `window`：`ctrl+win+t`
- `mac`：`ctrl+cmd+t`,
- `linux`: `ctrl+meta+t`,
- `Ubuntu`: `ctrl+super+t` 





# OS 常用命令 - os commands

[toc]





## Mac



### 终端

清除上一个命令输出：com + L

清屏：alt + com + L 或者 com + k



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





## Linux / Mac

### 生成目录结构

```
除了这个文件夹
> tree -I "node_modules"

只显示目录
> tree -d
```

### 进程

```
查看 pid：
> pgrep -f ‘文件名’
或者
> lsof -i:端口号|grep LISTEN

根据pid杀进程：
> kill -9 进程号

```

### 文件/压缩包 操作

```

创建文件
touch

解压
tar -zxvf xxxxxxxx.tar.gz
```

### 查看（文件内容类）

```
more
less
cat
```

### rpm yum包相关操作

```
查看安装
rpm -qa | grep xxx

卸载
rpm -e 包名
rpm -e mysql-libs --nodeps xxx

看rpm包，安装的详细路径
rpm -ql 包名

查看软件版本
rpm -qa | grep java

yum已安装
yum list installed 
```



### 查看（非文件内容）

```





网络,查询指定端口号情况
> netstat -tnlp | grep :80

环境变量
> echo $PATH

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

### >> vim <<

常用

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

跳到最后，一定是大写的g!
G

```



光标移动(Cursor Movement)

```
命令    作用（解释）
h,j,k,l    h表示往左，j表示往下，k表示往右，l表示往上
Ctrl+f    上一页
Ctrl+b    下一页
w, e, W, E    跳到单词的后面，小写包括标点
b, B    以单词为单位往前跳动光标，小写包含标点
O    开启新的一行
^    一行的开始
$    一行的结尾
gg    文档的第一行
[N]G    文档的第N行或者最后一行
```

插入模式(Insert Mode)

```
命令    作用（解释)
i    插入到光标前面
I    插入到行的开始位置
a    插入到光标的后面
A    插入到行的最后位置
o, O    新开一行
Esc    关闭插入模式
```

编辑(Editing)

```
命令    作用（解释）
r    在插入模式替换光标所在的一个字符
J    合并下一行到上一行
s    删除光标所在的一个字符, 光标还在当行
S    删除光标所在的一行，光标还在当行，不同于dd
u    撤销上一步操作
ctrl+r    恢复上一步操作
.    重复最后一个命令
~    变换为大写
[N]>>    一行或N行往右移动一个tab
[N]<<    一行或N行往左移动一个tab
```

关闭(Exiting)

```
命令    作用（解释)
:w    保存
:wq, :x    保存并关闭
:q    关闭（已保存）
:q!    强制关闭
```

搜索(Search)

```
命令    作用（解释)
/pattern    搜索（非插入模式)
?pattern    往后搜索
n    光标到达搜索结果的前一个目标
N    光标到达搜索结果的后一个目标
```

视觉模式(Visual Mode)

```
命令    作用（解释)
v    选中一个或多个字符
V    选中一行
```

剪切和复制(Cut and Paste)

```
命令    作用（解释)
dd    删除一行
dw    删除一个单词
x    删除后一个字符
X    删除前一个字符
D    删除一行最后一个字符
[N]yy    复制一行或者N行
yw    复制一个单词
p    粘贴
```





# 其他常用命令 - others commands

## Mysql

### root登录

```sh
Linux登录方式：
先切换用户（命令运行后，输入开机密码）
su - mysql
登录mysql（命令运行后，输入mysql密码）
mysql -uroot -p  -P 3306 -S /mysql/data/mysql3306/socket/mysql.sock

mac登录方式：
mysql -uroot -p
然后输入密码
```

### 修改密码

> 前提是登录了mysql

```mysql
alter user root@'localhost' identified by '新密码';

注意，如果要改远程连接的用户密码，需要改另一个！！
alter user root@'%' identified by '新密码';
```

### 查看信息

```mysql
查看版本
select version()

```





## Node

### 常用

查看全局安装

```
npm ls -g
```

全局安装 或 升级

```
npm install -g xxxxxx@a.b.c
```





### win 切换 node版本 NVM

> #### Win 需要管理员权限才能切换 ！ ！ ！

```
nvm list
nvm use [version]

nvm root
```



## tools



### Git

```
git-cz

git log - 查看历史提交记录。
git blame <file> - 以列表形式查看指定文件的历史修改记录。
git log --reverse --oneline

切换仓库、重命名、指定仓库的分支进行提交
git remote
git remote -v
git remote rename origin xxx
git remote add yyy repoUrl
git push xxx

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

