# W-I-L-L

[toc]



## Now

## sh命令后无法退出

输入exit即可，而不是q

### git 自动提交脚本

先运行whereis bash，我用的是zsh 所以运行的是where is zsh，然后会输出 运行正常的地址 `bin/bash`或 `/bin/zsh` ，这就是下面第一行的内容

提交时，只需运行命令sh ./gitbash.sh '提交描述信息'

**补充说明：**

1、#! /bin/bash，声明脚本解释执行的方式，必须写在第一行；
2、运行报错，找不到sh命令如何解决？首先确保已正确安装好git工具，在git安装目录下有一个bin文件夹，里面找到sh.exe，在系统环境变量中添加相对应的环境，如C:\Program Files\Git\bin
3、一般shell的变量赋值的时候不用带“$”，$1值为 *sh ./gitbash.sh '提交描述信息'* 命令的第一个参数



在~目录创建文件，文件名自己定就好。。我是叫 git-auto.sh，内容如下

```
#! /bin/zsh

# 运行
# sh ./gitbash.sh '提交描述信息'

echo "请输入工程目录："
read project_dir
cd project_dir

git status

git add .

echo "请输入提交说明："
read msg
git commit -m msg

git push

# 空行
# echo ${br/* /}

echo "如果是will和steppp项目再git push gitee即可"



```



### pnpm

这个包管理器不管怎么说，vue团队在用、naive-ui团队也在用，还是值得试一下的~

## Path

- 百度、知乎、b站、谷歌、Github、Gitee
- 