# Will-2022-06

[toc]



## Learned















### monorepo项目的git菜单设置，按照文件树展示

由于monorepo是超多项目的集合，如果一次修改了多个项目，混在一起是很难code review的，必须要按照文件树显示

清晰不犯错~

![image-20220608071104350](https://raw.githubusercontent.com/vacrain/typora_img/main/2022/2022-06-08_07-11-04_image-20220608071104350.png)



### vscode 实用菜单说明

这些都要打开！！！

![image-20220608070553898](https://raw.githubusercontent.com/vacrain/typora_img/main/2022/2022-06-08_07-05-54_image-20220608070553898.png)



依次是：

1. Open editors：现在打开的文件
2. Folders：打开的文件夹（这个默认是隐藏不了的）
3. Outline：当前聚焦的文件内的大纲，除了脚本文件几乎都有大纲，很好用，不需要折叠文件内代码了
4. Timeline：文件修改历史，打开后将本地历史关掉（如果用了git的话）
5. npm script：npm脚本（如果是node项目，这太实用了）





### npm 发布

参考：https://segmentfault.com/a/1190000022116379





### shell脚本 函数  if 参数

```

# 函数：
  # source 是内置命令，用途是读取文件中内容，并在当前shell中逐条执行。这种方式执行的脚本无须执行权限。source命令可以缩写为一个小数点
  #   可以说点命令的作用， 确实就等价于source命令。请注意看". ./a.sh", 前面一个点是点命令，等价于source, 后面一个点是和/一起的，./表示当前目录， 而且， 千万要注意， 这两个点之间必须有空格。
  # dirname可以获取参数路径 的上级目录路径
  #   dirname /usr/bin => /usr , 若没有上级目录，返回 .
  # export 用于设置或显示环境变量

# if
# 整数变量表达式：
  # -eq 等于
  # -ne 不等于
  # -gt 大于
  # -ge 大于等于
  # -lt 小于
  # -le 小于等于
# 字符串变量表达式：
  # If  [ $a = $b ]                 如果string1等于string2，则为真
  #                                 字符串允许使用赋值号做等号
  # if  [ $string1 !=  $string2 ]   如果string1不等于string2，则为真       
  # if  [ -n $string  ]             如果string 非空(非0），返回0(true)  
  # if  [ -z $string  ]             如果string 为空，则为真
  # if  [ $sting ]                  如果string 非空，返回0 (和-n类似) 
  #     逻辑非 !                     条件表达式的相反
  # if [ ! 表达式 ]
  # if [ ! -d $num ]                如果不存在目录$num
  #     逻辑与 –a                    条件表达式的并列
  # if [ 表达式1  –a  表达式2 ]
  #     逻辑或 -o                    条件表达式的或
  # if [ 表达式1  –o 表达式2 ]

# 参数、选项、表达式：
  # $0 	当前脚本的文件名
  # $n 	传递给脚本或函数的参数。n 是一个数字，表示第几个参数。例如，第一个参数是$1，第二个参数是$2。
  # $# 	传递给脚本或函数的参数个数。
  # $* 	传递给脚本或函数的所有参数。
  # $@ 	传递给脚本或函数的所有参数。被双引号(" ")包含时，与 $* 稍有不同，下面将会讲到。
  # $? 	上个命令的退出状态，或函数的返回值。
  # $$ 	当前Shell进程ID。对于 Shell 脚本，就是这些脚本所在的进程ID。
  # -e filename 如果 filename存在，则为真
  # -d filename 如果 filename为目录，则为真 
  # -f filename 如果 filename为常规文件，则为真   检测文件是否是普通文件（既不是目录，也不是设备文件），如果是，则返回 true。
  # -L filename 如果 filename为符号链接，则为真
  # -r filename 如果 filename可读，则为真 
  # -w filename 如果 filename可写，则为真 
  # -x filename 如果 filename可执行，则为真
  # -s filename 如果文件长度不为0，则为真
  # -h filename 如果文件是软链接，则为真
  # -z [ -z STRING ] “STRING” 的长度为零则为真。
  # -n 相反的判断用-n zero, non-zero
  # readonly 定义只读
  # basename 即去除文件名的目录部分和后缀部分
  # -- - 可以处理短选项（-）又可以处理长选项（--），如：--help, -h

```





### vscode 自动添加注释

参考：https://github.com/OBKoro1/koro1FileHeader/wiki/



### sh脚本函数

```
# 定义
fn() {
	# do something
	...
	
	# 使用第一个参数
	$1
	
	# 使用第二个参数
	$2
}

# 调用
fn 参数1 参数2
```



### vscode 中使用 todo

先下载todo tree插件

然后在代码中写注释，如 // TODO 这个地方有空要优化一下

之后在侧边栏中，点击按钮即可看到

![image-20220602005629248](https://raw.githubusercontent.com/vacrain/typora_img/main/2022/2022-06-02_00-56-29_image-20220602005629248.png)



### Turborepo monorepo  学习资料

[使用Turborepo进行复杂拓扑关系的monorepo最优构建](https://blog.csdn.net/qq_21567385/article/details/122019974)

