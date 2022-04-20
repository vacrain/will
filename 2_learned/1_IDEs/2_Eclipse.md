# Eclipse

[toc]









## Eclipse窗口样式保存与双击窗口最大化 视图重置

参考：https://blog.csdn.net/qq_43021380/article/details/98316455

**window->Perspective->Reset Perspective** 

## link with editer

参考：[eclipse点击正在编辑的文件时，左边的目录树自动定位到文件所在的目录树的位置](https://blog.csdn.net/thinkingmyself/article/details/88113441)




## 快捷键

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




Eclipse插件：
---



Mybatis Dao层跳转XML：
--
    安装说明：
    https://blog.csdn.net/hehaimingg/article/details/93628423
    使用说明：
    https://blog.csdn.net/qq_30693057/article/details/88914918

eclipse 热部署  
--
https://blog.csdn.net/weixin_42245930/article/details/83443287

过期了看这个：https://www.jb51.net/article/201533.htm

服务器地址：https://jrebel.qekang.com/

随机uuid网址：https://www.guidgen.com/



Eclipse设置护眼色：
--
https://blog.csdn.net/qq_36007926/article/details/85098177




---
怎么在eclipse中搜索文件？
---

在eclipse顶部菜单条中有一个Search 按钮，点进去，然后在弹出的对话框中选择File Search 选项卡


在里面有很多参数，其中：

Containing text ： 指定自己要搜索的关键字，文本控件后面有Regular expression 和 Case sensitive 表示是否支持正则表达式 和区分大小写

File name patterns : 指定自己要搜索的文件格式，比如以Servlet为后缀的Servlet 那么输入：*Servlet.java 

Scope : 指定所有的目录，默认是在当前的工作空间

然后点击Search ，就会在自己选择目录中根据自己输入的关键字搜索指定的文件是否存在，存在则会在Search 结果页面展示出来。


--------------------------
debug
--

https://blog.csdn.net/u011781521/article/details/55000066



Eclipse 显示面包屑栏：  

> <kbd>alt</kbd>+<kbd>shift</kbd>+<kbd>B</kbd>



[eclipse console自动弹窗问题](https://blog.csdn.net/aodeng110/article/details/80693048)

[关于svn与eclipse，更新、与资源库同步、提交](https://blog.csdn.net/wallace1992/article/details/77839672/)

