

# Code Tools







## Node



### npm使用

win的.npmrc 在哪

https://zhidao.baidu.com/question/1499004587754875659.html



或者直接改

https://www.cnblogs.com/yiweiyihang/p/8064604.html

安装完node.js并配置环境变量。在cmd窗口检查npm安装是否成功。

安装淘宝npm：

#### 1.临时使用

```
npm --registry https://registry.npm.taobao.org install express
```

#### 2.持久使用

```
npm config set registry https://registry.npm.taobao.org
```

- 配置后可通过下面方式来验证是否成功 
  `npm config get registry`
- 或 
  `npm info express`

#### 3.通过cnpm使用

```
npm install -g cnpm --registry=https://registry.npm.taobao.org
```

- - 使用 
    `cnpm install express`

#### win很重要一点！

配置npm全局安装的目录到环境变量中， 查看npm全局安装目录：

```
npm config get prefix
```

用上面的命令，可以查到下面的目录：

```
C:\Users\ys1222\AppData\Roaming\npm
```

在全局变量中添加上面的目录即可，之后就可随处使用npm安装的软件了 ！！！





### Mac node 升级

https://www.jianshu.com/p/acd316dceeb8

控制台打印：也就是我之前的给无视了。。重新找了个默认目录安装新的，也行

```
Note: the node command changed location and the old location may be remembered in your current shell.
         old : /Library/code/tools/node/bin/node
         new : /usr/local/bin/node
If "node --version" shows the old version then start a new shell, or reset the location hash with:
hash -r  (for bash, zsh, ash, dash, and ksh)
rehash   (for csh and tcsh)
```



### npm设置

查看默认安装目录

```
npm config get prefix
```

设置默认安装目录(不配置好，会出现npm install -g的时候摸不到头脑的问题)

```
npm config set prefix "/usr/local/lib/node_modules"
```





### Npm、yarn、pnpm

pnpm说明：

https://blog.csdn.net/Dylan666d/article/details/114002666

安装和yarn一样



Node安装问题

https://blog.csdn.net/rheostat/article/details/7614451

官网下载 了一个tar.xz文件，和往常见到的tar.gz不太一样，原来是新的压缩格式，上面的网站比较详细的讲了咋解压

**先 xz -d xxx.tar.xz 将 xxx.tar.xz解压成 xxx.tar 然后，再用 tar xvf xxx.tar来解包。**

然后通过下面的命令，把命令变成全局可用的

```
ln -s 命令的绝对路径 /usr/local/bin       
```

Yarn

```
npm install yarn -g
```

linux然后记得加软连接



mac配置bashrc或zshrc等文件，比如我用的zsh，所以安装下面操作：

```
cd ~
open .zshrc
上两步会打开一个记事本，然后把yarn的路径填进去，路径在哪要看npm的默认安装目录配置
我的是/usr/local/lib/node_modules

所以在.zshrc文件中写入如下
# yarn
export yarn=/usr/local/lib/node_modules
export PATH=$PATH:$yarn/bin

保存退出即可，然后在任何地方都可以用yarn了
```







## vscode 

### 超出一行的代码，自动换行

设置里搜 editor.wordWrap，如果分workspace了的话，需要点一下划线部分

![image-20211115154257595](https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2021-11-15 15-43-02_image-20211115154257595.png)




### vs code SVN


安装SVN时命令功能全选上，这样在vs code 中的插件才能使用



### 文本一行装不下时，自动换行显示，怎么设置

文本超出显示时,会溢出, 文本超出范围,不能自动换行 

进入文件>首选项>设置,打开设置界面,在常用设置下找到Editor:Word Wrap选项,默认为off,设置为on即可。 文档超范围是否隐藏选项 

完成自动换行




-
### VS code 插件：  


- Coding:

Auto Close Tag  
Auto Rename Tag  
Bracket Pair Colorizer  
Chinese (Simplified) Language Pack for  Visual Studio Code  
Debugger for Chrome  
EJS language support  
ESLint 
Japanese Language Pack for Visual Studio Code  
Path Intellisense  
Prettier - Code formatter  
TortoiseSVN   
Vetur  

Java Extension Pack

- VS code Markdown：  

Markdown All in One  
Markdown Preview Github Styling  
Markdown PDF
Markdown TOC
    https://blog.csdn.net/u014171091/article/details/89629634


- VS code 主题：

Tiny Light  

- 其他：

LeetCode

VSCode Rainbow Fart

小霸王

Zhihu On VSCode

daily anime

WeReadForVSCode   按ctrl + f3开启



### mac 第三方中文输入法 vscode终端 大小写问题

vscode终端里用百度、搜狗这种输入法，按大写键切换中英文，会把中文切换到大写

2022-04-16 至今没有解决办法[Mac VS Code 命令行输入问题](https://segmentfault.com/q/1010000018329741)

改成shift切换吧，正好上班也是win系统。。




### 记录代码时间vscdoe工具

https://wakatime.com/


### vscode插件集合

- gitlens



### vscode打开一个新文件后旧文件自动关闭

https://blog.csdn.net/weixin_41838721/article/details/115391516

取消打勾即可



### VSCode中使用Git忽略提交代码设置

https://blog.csdn.net/Strive_For_Future/article/details/120952325



### 大坑！！！VSCODE 终端 取消右键粘贴 快速模式取消

https://blog.csdn.net/akapinkman/article/details/108960835



### vscode左侧的source control自动检测文件

把  .git 文件删掉就好了！



## Eclipse



### Eclipse窗口样式保存与双击窗口最大化 视图重置

参考：https://blog.csdn.net/qq_43021380/article/details/98316455

**window->Perspective->Reset Perspective** 

### link with editer

参考：[eclipse点击正在编辑的文件时，左边的目录树自动定位到文件所在的目录树的位置](https://blog.csdn.net/thinkingmyself/article/details/88113441)




### 快捷键

参考：[eclipse快捷键以及使用技巧大全](https://www.cnblogs.com/xiaohh/p/4793510.html)

https://www.runoob.com/eclipse/eclipse-shortcuts.html

| 分类                 | 快捷键[^pr/po]                     | 说明                                                         |
| -------------------- | ---------------------------------- | ------------------------------------------------------------ |
| **一般常用快捷键**   | ctrl + O[^pr1]                      | 显示类中方法和属性的大纲，能快速定位类的方法和属性，在查找Bug时非常有用。 |
|                      | ctrl + /[^pr2]                      | 注释一行                                                     |
|                      | ctrl + D[^pr2]                      | 删除一行                                                     |
|                      | ctrl + M[^pr3]                      | 窗口最大化，也可以直接双击窗口                               |
| **查看和定位快捷键** | 【Ctrl+K】、【Ctrl++Shift+K】[^pr4] | 快速向下和向上查找选定的内容，从此不再需要用鼠标单击查找对话框了。 |
|                      | Ctrl+Shift+T[^po1]                 | 查找工作空间（Workspace）构建路径中的可找到Java类文件，不要为找不到类而痛苦，而且可以使用“*”、“？”等通配符。*代表多个字符，?代表单个字符，和sql里的%和_类似 |
|                      | Ctrl+Shift+R[^po2]                 | 和【Ctrl+Shift+T】对应，查找工作空间（Workspace）中的所有文件（包括Java文件），也可以使用通配符。 |
|                      | Ctrl+Shift+G[^pr5]                | 查找类、方法和属性的引用。这是一个非常实用的快捷键，例如要修改引用某个方法的代码，可以通过【Ctrl+Shift+G】快捷键迅速定位所有引用此方法的位置。 |
|                      | Ctrl+Shift+O[^pr1]              | 快速生成import，当从网上拷贝一段程序后，不知道如何import进所调用的类，试试【Ctrl+Shift+O】快捷键，一定会有惊喜。 |
|                      | ALT+Shift+W[^pr1]                 | 查找当前文件所在项目中的路径，可以快速定位浏览器视图的位置，如果想查找某个文件所在的包时，此快捷键非常有用（特别在比较大的项目中）。 |
|                      | Ctrl+L[^pr1]                       | 定位到当前编辑器的某一行，对非Java文件也有效。               |
|                      | 【Alt+←】<br>【Alt+→】[^pr1]       | 后退历史记录和前进历史记录，在跟踪代码时非常有用，用户可能查找了几个有关联的地方，但可能记不清楚了，可以通过这两个快捷键定位查找的顺序。 |
|                      | F3[^pr5]                           | 快速定位光标位置的某个类、方法和属性。                       |
|                      | F4[^pr1]                         | 显示类的继承关系，并打开类继承视图。                         |
| **调试快捷键**[^pr6] | Ctrl+Shift+B[^pr1][^pr2] | 在当前行设置断点或取消设置的断点。 |
|  | F11[^pr7] | 调试最后一次执行的程序。 |
|  | Ctrl+F11[^pr7] | 运行最后一次执行的程序。 |
| | F5 | 跟踪到方法中，当程序执行到某方法时，可以按【F5】键跟踪到方法中。 |
|  | F6 | 单步执行程序。 |
|  | F7 | 执行完方法，返回到调用此方法的后一条语句。 |
|  | F8 | 继续执行，到下一个断点或程序结束。 |
| 编辑快捷键 | Ctrl+Z | 撤销 |
|  | Ctrl+Y | 重复 |
|  | Ctrl+F | 查找 |
|  | Ctrl+C、X、V | 复制、剪切、粘贴 |
|  | Ctrl+S | 保存 |
| 其他 | Ctrl+Shift+F                       | 格式化代码，书写格式规范的代码是每一个程序员的必修之课，当看见某段代码极不顺眼时，选定后按【Ctrl+Shift+F】快捷键可以格式化这段代码，如果不选定代码则默认格式化当前文件（Java文件）。 |
|                      | 如果为空 |                                                              |
|                      |                                    |                                                              |



[^pr/po]: pr是前置操作、po是后置操作

**Preconditions** :

[^pr1]:单击已打开的文件窗口
[^pr2]:单击目标代码行
[^pr3]:单击目标窗口
[^pr4]:选中（或双击）目标代码
[^pr5]:单击类、方法和属性
[^pr6]:单击`Debug`视图
[^pr7]:debug启动项目时用，需查看服务器已停止
[^pr8]:单击
[^pr9]:单击
[^pr10]:单击
[^pr11]:单击
[^pr12]:单击
[^pr13]:单击
[^pr13]:单击
[^pr14]:单击
[^pr15]:单击
[^pr16]:单击
[^pr17]:单击



**Postcondition** :
[^po1]:输入Class名
[^po2]:输入文件名
[^po3]:输入
[^po4]:输入
[^po5]:输入
[^po6]:输入
[^po7]:输入
[^po8]:输入
[^po9]:输入
[^po10]:输入
[^po11]:输入
[^po12]:输入
[^po13]:输入
[^po13]:输入
[^po14]:输入
[^po15]:输入
[^po16]:输入
[^po17]:输入





意义|快捷键
--|--
文件内搜索|ctrl + F
全局搜索| ctrl + H
自动导入所有正确的包|Ctrl + Shift + O

------------------------




### 自定义快捷键

参考：[eclipse快捷键的设置和使用 写的非常好](https://blog.csdn.net/wenzhi20102321/article/details/52396086)

点击window菜单->preferences子菜单->general->keys，进入快捷键管理界面

在这里可以查找所有功能的快捷键，需要修改或新增时，点击需要修改或新增的命令，在binding里设置快捷键

设置完快捷键后，还需要设置在什么时候可以使用该快捷键，eclipse提供各种场景供选择，一般选择In Windows(即在eclipse窗口激活状态)即可



### 输入时自动补全功能设置

1. 打开MyEclipse 6.0.1,然后“window”→“Preferences” 

2. 选择“java”,展开,“Editor”,选择“Content Assist”。

3. 选择“Content Assist”,然后看到右边,右边的“Auto-Activation”下面的“Auto  Activation triggers for java”这个选项。其实就是指触发代码提示的就是“.”这个符号。

4.  “Auto Activation triggers for java”这个选项,在“.”后加abc等26个字母,方便后面的查找修改。然后“apply”,点击“OK”。

设置完成，我们每次输入代码都会有相应的提示！




### Eclipse插件：



#### Mybatis Dao层跳转XML：
    安装说明：
    https://blog.csdn.net/hehaimingg/article/details/93628423
    使用说明：
    https://blog.csdn.net/qq_30693057/article/details/88914918

#### eclipse 热部署  
https://blog.csdn.net/weixin_42245930/article/details/83443287

过期了看这个：https://www.jb51.net/article/201533.htm

服务器地址：https://jrebel.qekang.com/

随机uuid网址：https://www.guidgen.com/



#### Eclipse设置护眼色：
https://blog.csdn.net/qq_36007926/article/details/85098177




---
### 怎么在eclipse中搜索文件？

在eclipse顶部菜单条中有一个Search 按钮，点进去，然后在弹出的对话框中选择File Search 选项卡


在里面有很多参数，其中：

Containing text ： 指定自己要搜索的关键字，文本控件后面有Regular expression 和 Case sensitive 表示是否支持正则表达式 和区分大小写

File name patterns : 指定自己要搜索的文件格式，比如以Servlet为后缀的Servlet 那么输入：*Servlet.java 

Scope : 指定所有的目录，默认是在当前的工作空间

然后点击Search ，就会在自己选择目录中根据自己输入的关键字搜索指定的文件是否存在，存在则会在Search 结果页面展示出来。


--------------------------
### debug

https://blog.csdn.net/u011781521/article/details/55000066



Eclipse 显示面包屑栏：  

> <kbd>alt</kbd>+<kbd>shift</kbd>+<kbd>B</kbd>



[eclipse console自动弹窗问题](https://blog.csdn.net/aodeng110/article/details/80693048)

[关于svn与eclipse，更新、与资源库同步、提交](https://blog.csdn.net/wallace1992/article/details/77839672/)





## git





### Git原理

这原理真没啥可说的。。照着教程啥的做一遍就啥都懂了

![](https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2022-04-14_19-26-57_988e1c532f632385f5d24627cce833e038725d7e.jpg)






### git命令

```
git add .  日志
git log

查看用户名、邮箱设置
git config --global --list

设置用户名、邮箱
git config --global user.name "xxx"
git config --global user.email "xxx"

查看你的所有分支
git branch -vv

删除分支
git branch -d 分支名

查看远程仓库
git remote -v

查看状态
git status

查看文件修改内容
git diff 文件名

============================================
一般全提交交过程：

全部修改内容加载到暂存
git add .

将代码全部提交，这时还没有推到远端
git commit -m"你的描述"  

将代码推到远端分支
git push origin 你的分支名

git push成功会显示：
Counting objects: 4, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 556 bytes | 0 bytes/s, done.
Total 4 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/vacrain/learning.git
   5427cae..17e8925  main -> main



```


### Git提交三连

```
git add .
git commit -m"msg"
git push
```












### 修改commit信息

https://www.cnblogs.com/daodaotest/p/13841951.html



### 【Git】Git 报 OpenSSL SSL_read: Connection was reset, errno 10054 的错误如何解决

https://blog.csdn.net/qq_42351033/article/details/114643286



### [win生成公钥并使用](https://blog.csdn.net/a419419/article/details/80021684)



### git 安装及配置

[参考：win git 安装及配置， 及IDEA中配置以及使用Git Step By Step](https://www.cnblogs.com/bigc008/p/9858201.html)

安装完进行配置：

生成SSH的key：

```
生成命令：
ssh-keygen -t rsa –C "github里注册的邮箱"
填写存放目录，及文件名，目录（/f/ssh）文件名(rsa_1)随便起名哈：
/f/ssh/rsa_1
之后一路回车即可！
```

最后生成类似这些东西，就说明完成了：

```
Your identification has been saved in /f/ssh/qq726_rsa
Your public key has been saved in /f/ssh/qq726_rsa.pub
The key fingerprint is:
SHA256:GrhIVZ1d+p0DDvbvOu6NAXNS7SSafrKv7I1H2X42ZBI 726866011@qq.com
```

git全局配置：

```
git config --global user.name "用户名"

git config --global user.email "邮箱地址"

下面的可先不做：
git config --global color.ui true

git config --global push.default simple

git config --global core.editor vim

git的全局变量会存放在：~/.gitconfig （这个好像是Linux下的存放位置）

以上的命令，会保存成这样，所以也可以直接按格式在这里填写，或者保存这个文件，以便保存到别的计算机上。

[user]
    name = litifeng
    email = litifeng@example.com
[color]
    ui = true
[push]
    default = simple
[core]
    editor = vim

```

打开github、登录、进入设置界面，点【SSH and GPG keys】，然后点【New SSH key】：

![image-20210806101055106](https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2021-08-06 10-10-56_image-20210806101055106.png)

下面这个公钥，就是之前我们保存的那个：

```
填写描述：
for vac-commit
填写公钥：
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDQAMLnsy+5nMFZ3U3+DmGi1hT2TKsklYISm4sMhFE8Hye86QWkb03+a5wFVP+rMh61CtnUImLO1oMentHDTKi2KRLWCACX02UrA0gZmP2Wn5T24Z4D0wB086t1MCZLIY7pn9ng9VVYr+0p1x3Jo6mUAddIOp8y8tsY9h1GSf6fLTrSjHDAL3DQan3UzrV3r2NLs0khtvIh7KPjswZBn8+8endBRrJKvXiz8X9VKlOwvuvjJx/23I48xme+K4lR7SRiwNduw4+zjXqpCSSU+lbW+nH1Q9sVk05Emo+RYAQpompahPEEJtNX3437M7R1VMTtA/PgWGfE2KKDq2uIizGpyu9Rfm/cXXnwXPe/aosKna2CvybDNyMnfWewKJM4H2QuHgO8jmpNAe5iXvkzv2jDYfe6PVM9r2fzs2qkMuGRpTTCREftJ7Zc6ojrNgaCDIeXXAgorz44Z2kNkqtmh7Q4iBWY/S/JaCK8S2xrm0TAuww5xrvwDUI6sP9VmL7QQVE= 726866011@qq.com


这个公钥的查看方法：
第一步：
cd 到生成密钥的目录，我是【/f/ssh】，要是忘了，那就先挂个脑科的号，然后再从头做一遍
第二步：
cat 自己起的文件名.pub
```



![image-20210806101707374](https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2021-08-06 10-17-08_image-20210806101707374.png)

填写完成：

![image-20210806103422916](https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2021-08-06 10-34-24_image-20210806103422916.png)



**之后就可以用`git clone`命令去下载你需要的项目了~**

查看git配置：

```
 git config --global -l 
```







### git相关文章

[摸清 Git 的门路，就靠这 22 张图](https://mp.weixin.qq.com/s/shGoT9oRn62YSyCO9VEzDQ)

[如何开始在 github 上学习东西？](https://www.zhihu.com/question/30119197)

[在IDEA上Git的入门使用（IDEA+Git)](https://blog.csdn.net/weixin_39274753/article/details/79722522)

[git](https://blog.csdn.net/weixin_44689154/article/details/107811710?spm=1001.2014.3001.5501)

[Git基本操作流程](https://tophub.today/link?url=https%3A%2F%2Fwww.cnblogs.com%2Fdechinphy%2Fp%2Fgit.html)

[在gitee上创建你的第一个仓库](https://gitee.com/help/articles/4169)

[同上，这个更具体,看到第五步移步下面的教程](https://www.cnblogs.com/mingfeng002/p/8316659.html)

[【git】【eclipse】免密/SSH 方式连接免登录](https://blog.csdn.net/sayyy/article/details/99957973?utm_medium=distribute.pc_relevant.none-task-blog-baidujs_title-0&spm=1001.2101.3001.4242)

[关于Git这一篇就够了](https://blog.csdn.net/bjbz_cxy/article/details/116703787)









### 修改提交仓库地址

打开.git 文件夹中的 config 文件，直接修改地址即可

### 如何将代码同时提交到Github和码云Gitee上

https://blog.csdn.net/gozhuyinglong/article/details/113861993

- 配置好后，每次提交下面两个命令各用一次就好，或者用vscode 点点点就行

```
git push
git push gitee
```

- vscode 点点点提交，正常同步github（如果github是第一个remote库的话），再点一下下面的按钮，然后选gitee提交一下

![image-20220420073253948](https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2022-04-20_07-32-54_image-20220420073253948.png)



**配置说明** ：

- 查看

这个origin就是一个指向远程仓库的名称，是你在clone时 git 为你默认创建的。

```
> git remote
origin
```

```
> git remote -v
origin	https://github.com/vacrain/naive-ui-steppp.git (fetch)
origin	https://github.com/vacrain/naive-ui-steppp.git (push)
```

- 重命名，然后查看一下

```
> git remote rename origin github
> git remote
github
> git remote -v
github	https://github.com/vacrain/naive-ui-steppp.git (fetch)
github	https://github.com/vacrain/naive-ui-steppp.git (push)
```

- 添加同名库链接，然后再查看一下

```
> git remote add gitee https://gitee.com/vacrain/naive-ui-steppp.git
> git remote
gitee
github
> git remote -v
gitee	https://gitee.com/vacrain/naive-ui-steppp.git (fetch)
gitee	https://gitee.com/vacrain/naive-ui-steppp.git (push)
github	https://github.com/vacrain/naive-ui-steppp.git (fetch)
github	https://github.com/vacrain/naive-ui-steppp.git (push)
```

- pull push 带分支提交(==一般gitee 默认分支是master喔！！== 可以去仓库主页设置一下，把main设置成默认仓库，或者通过下一步绑定的时候 用git branch --set-upstream-to=gitee/master main)

```
git push github main
git pull github main

git push gitee main
git pull gitee main
```

- 想不带分支提交，就绑定一下

```
git branch --set-upstream-to=gitee/main main
格式说明
git branch --set-upstream-to=<remote>/<remote_branch> <local_branch>
```

- 移除

```
git remote remove gitee
```













```
git push
git push gitee
```



### git 全局忽略配置

```
vim ~/.gitignore_global
```

![image-20220417155839308](https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2022-04-17_15-58-39_image-20220417155839308.png)

在 ~/.gitconfig 中引入 .gitignore_global

```
[core]
	excludesfile = ~/.gitignore_global
```







### 生成SSH key

查找当前系统是否已经安装

```
rpm -qa |grep ssh
```

配置 https://blog.csdn.net/fish_skyyyy/article/details/119213714



### Mac git push报错令牌过期

报错内容：

```
➜ notes (main) git push

Username for 'https://github.com': vacrain

Password for 'https://vacrain@github.com': 

remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.

remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.

fatal: Authentication failed for 'https://github.com/vacrain/notes.git/'
```

参考：

https://stackoverflow.com/questions/68775869/support-for-password-authentication-was-removed-please-use-a-personal-access-to#





按照这个创建个人令牌以后，git push 输入用户名和刚才的令牌就可以了~




### Git提交问题

github 不配置好ssh 是提交不了的哦！！！具体过程就是：（需要基本的网络安全知识，即 非对称加密技术，科班期末必考了属于是）

1. 本机生成ssh私钥、公钥
2. github配置本机公钥
3. git clone项目
4. git提交项目
5. 首次提交还会弹出这个页面（同意授权就完事了~ 反正不同意也用不了。。）：<img src="https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2022-04-14_16-09-49_Screenshot 2022-04-14 at 16-08-31 Build software better together.png" alt="Screenshot 2022-04-14 at 16-08-31 Build software better together" style="zoom: 50%;" />



vscode左侧那个竖条里的图标，就这个![img_20220414](https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2022-04-14_15-40-27_img_20220414.png)，只能做到git add 和git commit ，git push到远端github 还是要手动来（无语）



如果push返回443延迟、超时了，不要紧张，真的就八成是连不上github，毕竟有wall~ 2022/4/14今日就到这里吧，学点别的了！







# Other Tools



## 浏览器 



### 火狐上不去谷歌

启用了被称为 HTTP 严格传输安全（HSTS）的安全策略，Firefox 只能与其建立安全连接

https://blog.csdn.net/weixin_46504044/article/details/105136645

1. 地址栏输入 about:config
2. 点击接受风险
3. 输入 security.enterprise_roots.enabled
4. 双击false 改成 true
5. 重启浏览器
6. ok



### Firefox 

安装完立刻切换到全球服务！！！否则登录不上





### 谷歌浏览器插件

1. chrome://extensions/
2. 右上角开关打开
3. 弹出的按钮第一个
4. 选择插件的chrome文件夹
5. ok

### 火狐插件

- [extension workstop](https://extensionworkshop.com/?utm_content=footer-link&utm_medium=referral&utm_source=addons.mozilla.org)
- [Working with the Tabs API](https://extensionworkshop.com/?utm_content=footer-link&utm_medium=referral&utm_source=addons.mozilla.org)
- [Content scripts](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Content_scripts)
- [User interface](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/user_interface)
- [如何给Firefox 火狐浏览器安装自己的插件](https://jingyan.baidu.com/article/c1a3101e9806fd9f646deb71.html)









## Other






### 日语输入法


> 参考：https://wenku.baidu.com/view/d22175176edb6f1aff001f1d.html



日语切换英文  

> <kbd>caps</kbd> + <kbd>shift</kbd>



日语输入法基本使用

**假名-罗马字对照表：**

|  あアa   |   いイi    |   うウu    | えエe  | おオo  |
| :------: | :--------: | :--------: | :----: | :----: |
|  かカka  |   きキki   |   くクku   | けケke | こコko |
|  さサsa  | しシsi/shi |   すスsu   | せセse | そソso |
|  たダta  | ちチti/chi | つツtsu/tu | てテte | とトto |
|  なナna  |   にニni   |   ぬヌnu   | ねネne | のノno |
|  はハha  |   ひヒhi   | ふフfu/hu  | へヘhe | ほホho |
|  まマma  |   みミmi   |   むムmu   | めメme | もモmo |
|  やヤya  |            |   ゆユyu   |        | よヨyo |
|  らラra  |   りリri   |   るレru   | れルre | ろロro |
|  わワwa  |            |            |        | をヲwo |
| んンn/nn |            |            |        |        |
|  がガga  |   ぎギgi   |   ぐグgu   | げゲge |  ごゴ  |
|  ざザza  | じジzi/ji  |   ずズzu   | ぜゼze | ぞゾzo |
|  だダda  |   ぢヂdi   |   づヅdu   | でデde | どドdo |
|  ばバba  |   びビbi   |   ぶブbu   | べベbe | ぼボbo |
|  ぱパpa  |   ぴピpi   |   ぷプpu   | ぺペpe | ぽポpo |

|
|きゃキャkya|きゅキュkyu|きょキョkyo
|しゃシャsya|しゅシュsyu|しょショsyo
|ちゃチャcya|ちゅチュcyu|ちょチョcyo
|にゃニャnya|にゅニュnyu|にょニョnyo
|ひゃヒャhya|ひゅヒュhyu|ひょヒョhyo
|みゃミャmya|みゅミュmyu|みょミョmyo
|りゃリャrya|りゅリュryu|りょリョryo
|ぎゃギャgya|ぎゅギュgyu|ぎょギョgyo
|じゃジャzaya/ja|じゅジュzyu/ju|じょジョzyo/jo
|びゃビャbya|びゅビュbyu|びょビョbyo
|ぴゃピャpya|ぴゅピュpyu|ぴょピョpyo



日语输入法使用技巧


1. 拨音(ん／ツ)用【n】表示。如：新聞(しんぶん)、民族(minzoku)。
2. 促音(小つ)将后面的子音重写两个来表示，如：国家（こっか）kokka、雑誌（ざっし）zassi。但在つ的前面则加“t”来表示，如：発着（はっちゃく）hattaku。
3. 小写的あいうえお用lalilulelo即可。如：ぁぃぅぇぉ
4. “ユーヒー”中的【ー】是【P】右上角的【-】
5. 切换到英语：<kbd>SHIFT</kbd>+<kbd>CapsLock</kbd> 
6. F6：转换为平假名。F7：转换为片假名。F8：转换为半角片假名。F9转换为全角英文数字。F10转换为半角英文数字。
7. 偏旁发音输入大法：只要懂偏旁发音可以很快输出怪癖字，如：“軾”用くるま加F5，之后选择即可。
8. 常用符号输入法：
   1. きごう加F5        得到所有记号
   2. たんい            得到所有单位符号
   3. すうがく          得到所有数学符号
   4. ぎりしゃ          得到希腊字母符号



### 欧陆词典

win系统下，有一点很坑，他会占用 ctrl + W

这样导致 无法通过该快捷键去关闭窗口！！！

win系统下，鼠标划词也关了吧，

鼠标划词时会自动 ctrl + c 导致与复制快捷键冲突，复制时无法一次复制成功



官网：https://www.eudic.net/v4/home/profile



### 有道词典

截图比较好用，可以配合欧陆的背单词一起使用

