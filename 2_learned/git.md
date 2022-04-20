# GIT

[toc]

### 修改commit信息

https://www.cnblogs.com/daodaotest/p/13841951.html



### 【Git】Git 报 OpenSSL SSL_read: Connection was reset, errno 10054 的错误如何解决

https://blog.csdn.net/qq_42351033/article/details/114643286



### 代码管理

[win生成公钥并使用](https://blog.csdn.net/a419419/article/details/80021684)



### 怎么引入github中的资源

[怎么使用github的js文件,css文件](https://blog.csdn.net/qq_27517377/article/details/86687289)

![image-20210809161629917](https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2021-08-09 16-16-35_image-20210809161629917.png)



![image-20210809161656711](https://gitee.com/vacrain/typora_img/raw/master/assets/imgs/2021/2021-08-09 16-16-58_image-20210809161656711.png)



这个文件的地址：https://raw.githubusercontent.com/lilei10101010/static/master/js/ckeditor5.js
如果你直接使用这个地址的话是会报错的：because its MIME type ('text/plain') is not executable, and strict MIME type checking is enabled
解决：把https://raw.githubusercontent.com/ 替换成：http://raw.githack.com/就可以了
这样引用github的js文件就行了 ：

<script src="http://raw.githack.com/lilei10101010/static/master/js/ckeditor5.js"></script>
2021/8/9 17:19:37 试了一下，上面这个方法不太行呀



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







### git其他

[摸清 Git 的门路，就靠这 22 张图](https://mp.weixin.qq.com/s/shGoT9oRn62YSyCO9VEzDQ)

[如何开始在 github 上学习东西？](https://www.zhihu.com/question/30119197)

[在IDEA上Git的入门使用（IDEA+Git)](https://blog.csdn.net/weixin_39274753/article/details/79722522)

[git](https://blog.csdn.net/weixin_44689154/article/details/107811710?spm=1001.2014.3001.5501)

[Git基本操作流程](https://tophub.today/link?url=https%3A%2F%2Fwww.cnblogs.com%2Fdechinphy%2Fp%2Fgit.html)

[在gitee上创建你的第一个仓库](https://gitee.com/help/articles/4169)

[同上，这个更具体,看到第五步移步下面的教程](https://www.cnblogs.com/mingfeng002/p/8316659.html)

[【git】【eclipse】免密/SSH 方式连接免登录](https://blog.csdn.net/sayyy/article/details/99957973?utm_medium=distribute.pc_relevant.none-task-blog-baidujs_title-0&spm=1001.2101.3001.4242)

[关于Git这一篇就够了](https://blog.csdn.net/bjbz_cxy/article/details/116703787)

