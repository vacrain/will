<i id="top"></i>

参考
==
https://blog.csdn.net/qq_23329167/article/details/83856430

https://huaweicloud.blog.csdn.net/article/details/112648614

[学习Linux的几点建议](https://www.iteye.com/blog/wellkingsen-1998417)

[Linux常用命令](https://www.iteye.com/blog/wellkingsen-1999272)

---
目录
==


<!-- TOC -->

- [一、基本命令](#一基本命令)
    - [1.1 关机和重启](#11-关机和重启)
            - [在最后加上](#在最后加上)
- [修改的内容如下：](#修改的内容如下)
- [修改的内容如下:](#修改的内容如下)
- [可通过ps -ef | grep nginx查看nginx是否已启动成功](#可通过ps--ef--grep-nginx查看nginx是否已启动成功)
- [!/bin/sh](#binsh)
- [nginx - this script starts and stops the nginx daemon](#nginx---this-script-starts-and-stops-the-nginx-daemon)
- [chkconfig:   - 85 15](#chkconfig-----85-15)
- [description:  NGINX is an HTTP(S) server, HTTP(S) reverse \](#description--nginx-is-an-https-server-https-reverse-\)
- [proxy and IMAP/POP3 proxy server](#proxy-and-imappop3-proxy-server)
- [processname: nginx](#processname-nginx)
- [config:      /etc/nginx/nginx.conf](#config------etcnginxnginxconf)
- [config:      /etc/sysconfig/nginx](#config------etcsysconfignginx)
- [pidfile:     /var/run/nginx.pid](#pidfile-----varrunnginxpid)
- [Source function library.](#source-function-library)
- [Source networking configuration.](#source-networking-configuration)
- [Check that networking is up.](#check-that-networking-is-up)
- [修改权限](#修改权限)
- [添加到服务列表](#添加到服务列表)
- [bind 127.0.0.1 # 将这行代码注释，监听所有的ip地址，外网可以访问](#bind-127001--将这行代码注释监听所有的ip地址外网可以访问)
- [!/bin/sh](#binsh-1)
- [chkconfig:   2345 90 10](#chkconfig---2345-90-10)
- [description:  Redis is a persistent key-value database](#description--redis-is-a-persistent-key-value-database)

<!-- /TOC -->






# 一、基本命令
## 1.1 关机和重启
关机
    shutdown -h now        立刻关机
    shutdown -h 5        5分钟后关机
    poweroff            立刻关机
重启
    shutdown -r now        立刻重启
    shutdown -r 5        5分钟后重启
    reboot                立刻重启

1.2 帮助命令
--help命令
  shutdown --help：
  ifconfig  --help：查看网卡信息

man命令（命令说明书） 
  man shutdown
  注意：man shutdown打开命令说明书之后，使用按键q退出

二、目录操作命令
2.1 目录切换 cd
命令：cd 目录

cd /        切换到根目录
cd /usr        切换到根目录下的usr目录
cd ../        切换到上一级目录 或者  cd ..
cd ~        切换到home目录
cd -        切换到上次访问的目录

2.2 目录查看 ls [-al]
命令：ls [-al]

ls                查看当前目录下的所有目录和文件
ls -a            查看当前目录下的所有目录和文件（包括隐藏的文件）
ls -l 或 ll       列表查看当前目录下的所有目录和文件（列表查看，显示更多信息）
ls /dir            查看指定目录下的所有目录和文件   如：ls /usr

2.3 目录操作【增，删，改，查】
2.3.1 创建目录【增】 mkdir
命令：mkdir 目录

mkdir    aaa            在当前目录下创建一个名为aaa的目录
mkdir    /usr/aaa    在指定目录下创建一个名为aaa的目录

2.3.2 删除目录或文件【删】rm
命令：rm [-rf] 目录

删除文件：
rm 文件        删除当前目录下的文件
rm -f 文件    删除当前目录的的文件（不询问）

删除目录：
rm -r aaa    递归删除当前目录下的aaa目录
rm -rf aaa    递归删除当前目录下的aaa目录（不询问）

全部删除：
rm -rf *    将当前目录下的所有目录和文件全部删除
rm -rf /*    【自杀命令！慎用！慎用！慎用！】将根目录下的所有文件全部删除

注意：rm不仅可以删除目录，也可以删除其他文件或压缩包，为了方便大家的记忆，无论删除任何目录或文件，都直接使用 rm -rf 目录/文件/压缩包

2.3.3 目录修改【改】mv 和 cp
一、重命名目录
    命令：mv 当前目录  新目录
    例如：mv aaa bbb    将目录aaa改为bbb
    注意：mv的语法不仅可以对目录进行重命名而且也可以对各种文件，压缩包等进行    重命名的操作

二、剪切目录
    命令：mv 目录名称 目录的新位置
    示例：将/usr/tmp目录下的aaa目录剪切到 /usr目录下面     mv /usr/tmp/aaa /usr
    注意：mv语法不仅可以对目录进行剪切操作，对文件和压缩包等都可执行剪切操作

三、拷贝目录
    命令：cp -r 目录名称 目录拷贝的目标位置   -r代表递归
    示例：将/usr/tmp目录下的aaa目录复制到 /usr目录下面     cp /usr/tmp/aaa  /usr
    注意：cp命令不仅可以拷贝目录还可以拷贝文件，压缩包等，拷贝文件和压缩包时不    用写-r递归

2.3.4 搜索目录【查】find
命令：find 目录 参数 文件名称
示例：find /usr/tmp -name 'a*'    查找/usr/tmp目录下的所有以a开头的目录或文件

三、文件操作命令
3.1 文件操作【增，删，改，查】
3.1.1 新建文件【增】touch
命令：touch 文件名
示例：在当前目录创建一个名为aa.txt的文件        touch  aa.txt

3.1.2 删除文件 【删】 rm
命令：rm -rf 文件名

3.1.3 修改文件【改】 vi或vim
【vi编辑器的3种模式】
    基本上vi可以分为三种状态，分别是命令模式（command mode）、插入模式（Insert mode）和底行模式（last line mode），各模式的功能区分如下：
1) 命令行模式command mode）
      控制屏幕光标的移动，字符、字或行的删除，查找，移动复制某区段及进入Insert mode下，或者到 last line mode。
      命令行模式下的常用命令：
      【1】控制光标移动：↑，↓，j
      【2】删除当前行：dd 
      【3】查找：/字符
      【4】进入编辑模式：i o a
      【5】进入底行模式：:
      
2) 编辑模式（Insert mode）
      只有在Insert mode下，才可以做文字输入，按「ESC」键可回到命令行模式。
      编辑模式下常用命令：
      【1】ESC 退出编辑模式到命令行模式；
      
3) 底行模式（last line mode）
     将文件保存或退出vi，也可以设置编辑环境，如寻找字符串、列出行号……等。
     底行模式下常用命令：
     【1】退出编辑：   :q
     【2】强制退出：   :q!
     【3】保存并退出：  :wq

打开文件

命令：vi 文件名
示例：打开当前目录下的aa.txt文件     vi aa.txt 或者 vim aa.txt

注意：使用vi编辑器打开文件后，并不能编辑，因为此时处于命令模式，点击键盘i/a/o进入编辑模式。

编辑文件

使用vi编辑器打开文件后点击按键：i ，a或者o即可进入编辑模式。

i:在光标所在字符前开始插入
a:在光标所在字符后开始插入
o:在光标所在行的下面另起一新行插入

保存或者取消编辑

保存文件：

第一步：ESC  进入命令行模式
第二步：:     进入底行模式
第三步：wq     保存并退出编辑

取消编辑：

第一步：ESC  进入命令行模式
第二步：:     进入底行模式
第三步：q!     撤销本次修改并退出编辑

3.1.4 文件的查看【查】
文件的查看命令：cat/more/less/tail

cat：看最后一屏

示例：使用cat查看/etc/sudo.conf文件，只能显示最后一屏内容
cat sudo.conf

more：百分比显示

示例：使用more查看/etc/sudo.conf文件，可以显示百分比，回车可以向下一行，空格可以向下一页，q可以退出查看
more sudo.conf

less：翻页查看

示例：使用less查看/etc/sudo.conf文件，可以使用键盘上的PgUp和PgDn向上    和向下翻页，q结束查看
less sudo.conf

tail：指定行数或者动态查看

示例：使用tail -10 查看/etc/sudo.conf文件的后10行，Ctrl+C结束  
tail -10 sudo.conf

3.2 权限修改
rwx：r代表可读，w代表可写，x代表该文件是一个可执行文件，如果rwx任意位置变为-则代表不可读或不可写或不可执行文件。

示例：给aaa.txt文件权限改为可执行文件权限，aaa.txt文件的权限是-rw-------

第一位：-就代表是文件，d代表是文件夹
第一段（3位）：代表拥有者的权限
第二段（3位）：代表拥有者所在的组，组员的权限
第三段（最后3位）：代表的是其他用户的权限

   421  421  421
-  rw-   ---     ---

命令：chmod +x aaa.txt
或者采用8421法
命令：chmod 100 aaa.txt
四、压缩文件操作
4.1 打包和压缩
Windows的压缩文件的扩展名  .zip/.rar
linux中的打包文件：aa.tar      
linux中的压缩文件：bb.gz    
linux中打包并压缩的文件：.tar.gz

Linux中的打包文件一般是以.tar结尾的，压缩的命令一般是以.gz结尾的。
而一般情况下打包和压缩是一起进行的，打包并压缩后的文件的后缀名一般.tar.gz。

命令：tar -zcvf 打包压缩后的文件名 要打包的文件
其中：z：调用gzip压缩命令进行压缩
  c：打包文件
  v：显示运行过程
  f：指定文件名

示例：打包并压缩/usr/tmp 下的所有文件 压缩后的压缩包指定名称为xxx.tar
tar -zcvf ab.tar aa.txt bb.txt 
或：tar -zcvf ab.tar  *

4.2 解压
命令：tar [-zxvf] 压缩文件    
其中：x：代表解压
示例：将/usr/tmp 下的ab.tar解压到当前目录下



示例：将/usr/tmp 下的ab.tar解压到根目录/usr下
tar -xvf ab.tar -C /usr------C代表指定解压的位置



五、查找命令
5.1 grep
grep命令是一种强大的文本搜索工具

使用实例：

ps -ef | grep sshd  查找指定ssh服务进程 
ps -ef | grep sshd | grep -v grep 查找指定服务进程，排除gerp身 
ps -ef | grep sshd -c 查找指定进程个数 
5.2 find
find命令在目录结构中搜索文件，并对搜索结果执行指定的操作。 

find 默认搜索当前目录及其子目录，并且不过滤任何结果（也就是返回所有文件），将它们全都显示在屏幕上。

使用实例：

find . -name "*.log" -ls  在当前目录查找以.log结尾的文件，并显示详细信息。 
find /root/ -perm 600   查找/root/目录下权限为600的文件 
find . -type f -name "*.log"  查找当目录，以.log结尾的普通文件 
find . -type d | sort   查找当前所有目录并排序 
find . -size +100M  查找当前目录大于100M的文件
5.3 locate
locate 让使用者可以很快速的搜寻某个路径。默认每天自动更新一次，所以使用locate 命令查不到最新变动过的文件。为了避免这种情况，可以在使用locate之前，先使用updatedb命令，手动更新数据库。如果数据库中没有查询的数据，则会报出locate: can not stat () `/var/lib/mlocate/mlocate.db': No such file or directory该错误！updatedb即可！

yum -y install mlocate 如果是精简版CentOS系统需要安装locate命令

使用实例：

updatedb
locate /etc/sh 搜索etc目录下所有以sh开头的文件 
locate pwd 查找和pwd相关的所有文件
5.4 whereis
whereis命令是定位可执行文件、源代码文件、帮助文件在文件系统中的位置。这些文件的属性应属于原始代码，二进制文件，或是帮助文件。

使用实例：

whereis ls    将和ls文件相关的文件都查找出来
5.5 which
which命令的作用是在PATH变量指定的路径中，搜索某个系统命令的位置，并且返回第一个搜索结果。

使用实例：

which pwd  查找pwd命令所在路径 
which java  查找path中java的路径 
六、su、sudo
6.1 su
su用于用户之间的切换。但是切换前的用户依然保持登录状态。如果是root 向普通或虚拟用户切换不需要密码，反之普通用户切换到其它任何用户都需要密码验证。

su test:切换到test用户，但是路径还是/root目录
su - test : 切换到test用户，路径变成了/home/test
su : 切换到root用户，但是路径还是原来的路径
su - : 切换到root用户，并且路径是/root
su不足：如果某个用户需要使用root权限、则必须要把root密码告诉此用户。

退出返回之前的用户：exit

6.2 sudo
sudo是为所有想使用root权限的普通用户设计的。可以让普通用户具有临时使用root权限的权利。只需输入自己账户的密码即可。

进入sudo配置文件命令：

vi /etc/sudoer或者visudo
案例：
允许hadoop用户以root身份执行各种应用命令，需要输入hadoop用户的密码。
hadoop  ALL=(ALL)   ALL 

案例：
只允许hadoop用户以root身份执行ls 、cat命令，并且执行时候免输入密码。 
配置文件中： 
hadoop  ALL=NOPASSWD:  /bin/ls, /bin/cat 
七、系统服务
service iptables status  --查看iptables服务的状态
service iptables start  --开启iptables服务
service iptables stop  --停止iptables服务
service iptables restart  --重启iptables服务

chkconfig iptables off  --关闭iptables服务的开机自启动
chkconfig iptables on  --开启iptables服务的开机自启动
八、网络管理
8.1 主机名配置
[root@node1 ~]# vi /etc/sysconfig/network
NETWORKING=yes
HOSTNAME=node1
8.2 IP 地址配置
[root@node1 ~]# vi /etc/sysconfig/network-scripts/ifcfg-eth0
8.3 域名映射
/etc/hosts文件用于在通过主机名进行访问时做ip地址解析之用。所以，你想访问一个什么样的主机名，就需要把这个主机名和它对应的ip地址。

[root@node1 ~]# vi /etc/hosts
#### 在最后加上
192.168.52.201  node1
192.168.52.202  node2
192.168.52.203  node3
九、定时任务指令crontab 配置
crontab是Unix和Linux用于设置定时任务的指令。通过crontab命令，可以在固定间隔时间,执行指定的系统指令或shell脚本。时间间隔的单位可以是分钟、小时、日、月、周及以上的任意组合。

crontab安装：

yum install crontabs
服务操作说明：

service crond start   ## 启动服务 
service crond stop    ## 关闭服务 
service crond restart ## 重启服务
9.1 命令格式
crontab [-u user] file

crontab [-u user] [ -e | -l | -r ]

参数说明：

-u user：用来设定某个用户的crontab服务  

file：file是命令文件的名字,表示将file做为crontab的任务列表文件

并载入crontab。

-e：编辑某个用户的crontab文件内容。如果不指定用户，则表示编辑当前

用户的crontab文件。

-l：显示某个用户的crontab文件内容。如果不指定用户，则表示显示当前

用户的crontab文件内容。

-r：删除定时任务配置，从/var/spool/cron目录中删除某个用户的crontab

文件，如果不指定用户，则默认删除当前用户的crontab文件。

命令示例：

crontab file [-u user] ## 用指定的文件替代目前的crontab
crontab -l [-u user]  ## 列出用户目前的crontab
crontab -e [-u user]  ## 编辑用户目前的crontab
9.2 配置说明、实例
命令：*   *    *   *   *   command  

解释：分  时  日  月  周  命令

第1列表示分钟1～59 每分钟用*或者 */1表示    

第2列表示小时0～23（0表示0点）

第3列表示日期1～31  

第4列表示月份1～12  

第5列标识号星期0～6（0表示星期天）  

第6列要运行的命令

配置实例：

先打开定时任务所在的文件：
crontab -e

每分钟执行一次date命令 
*/1 * * * * date >> /root/date.txt

每晚的21:30重启apache。 
30 21 * * * service httpd restart

每月1、10、22日的4 : 45重启apache。  
45 4 1,10,22 * * service httpd restart

每周六、周日的1 : 10重启apache。 
10 1 * * 6,0 service httpd restart

每天18 : 00至23 : 00之间每隔30分钟重启apache。
0,30   18-23    *   *   *   service httpd restart
晚上11点到早上7点之间，每隔一小时重启apache
*  23-7/1    *   *   *   service httpd restart
十、其他命令
10.1 查看当前目录：pwd
命令：pwd     查看当前目录路径

10.2 查看进程：ps -ef
命令：ps -ef    查看所有正在运行的进程

10.3 结束进程：kill
命令：kill pid 或者 kill -9 pid(强制杀死进程)           pid:进程号

10.4 网络通信命令：
ifconfig：查看网卡信息

命令：ifconfig 或 ifconfig | more

ping：查看与某台机器的连接情况

命令：ping ip

netstat -an：查看当前系统端口

命令：netstat -an

搜索指定端口
命令：netstat -an | grep 8080

10.5 配置网络
命令：setup

10.6 重启网络
命令：service network restart

10.7 切换用户
命令：su - 用户名

10.8 关闭防火墙
命令：chkconfig iptables off

或者：

 iptables -L;
 iptables -F;
 service iptables stop
10.9 修改文件权限
命令：chmod 777

10.10 清屏
命令：ctrl + l

10.11 vi模式下快捷键
esc后:

保存并退出快捷键：shift+z+z

光标跳到最后一行快捷键：shift+g

删除一行：dd

复制一行内容：y+y

粘贴复制的内容：p

十一、Linux项目部署
11.1 安装jdk1.8
先卸载open-jdk

java -version
rpm -qa | grep java

rpm -e --nodeps java-1.7.0-openjdk-1.7.0.45-2.4.3.3.el6.x86_64
rpm -e --nodeps java-1.6.0-openjdk-1.6.0.0-1.66.1.13.0.el6.x86_64

开始安装：
mkdir /usr/local/src/java
rz 上传jdk tar包
tar -zxvf jdk-8u181-linux-x64.tar.gz

yum install glibc.i686

配置环境变量：
 vi /etc/profile

 在末尾行添加
  #set java environment
  JAVA_HOME=/usr/local/src/jdk8/jdk1.8.0_181
  CLASSPATH=.:$JAVA_HOME/lib.tools.jar
  PATH=$JAVA_HOME/bin:$PATH
  export JAVA_HOME CLASSPATH PATH

保存退出
source /etc/profile  使更改的配置立即生效
java -version  查看JDK版本信息，如果显示出1.8证明成功

11.2 安装MySQL5.6
11.2.1 上传MySQL5.6的tar包
创建目录：mkdir /usr/local/src/mysql5.6

上传：MySQL-5.6.34-1.rhel5.x86_64.rpm-bundle.tar 到上面的目录中

11.2.2 安装
第一步：解压

     命令：tar -xvf MySQL-5.6.34-1.rhel5.x86_64.rpm-bundle.tar

第二步：检测是否已经安装了mysql

     命令：rpm -qa | grep mysql   
    
     如果已经安装了，将其卸载，如：
    
     rpm -e --nodeps  mysql-libs-5.1.71-1.el6.x86_64

第三步：安装MySQL的服务端

     命令：rpm -ivh MySQL-server-5.6.34-1.rhel5.x86_64.rpm

第四步：安装MySQL的客户端

     命令：rpm -ivh MySQL-client-5.6.34-1.rhel5.x86_64.rpm

第五步：查看MySQL服务运行状态

     命令：service mysql status

第六步：启动MySQL服务

     命令：service mysql start

第七步：使用root账号登录mysql

在安装mysql server时有句提示：



注意：这个密码是不安全的，所有需要修改初始密码。

使用密码登录mysql账号：mysql -uroot -p
修改root密码：SET PASSWORD = PASSWORD('root');
11.2.3 开机自动启动设置
加入到系统服务：

chkconfig --add mysql

自动启动：

chkconfig mysql on

查询列表：

chkconfig

说明：都没关闭（off）时是没有自动启动。

11.2.4 开启远程访问
登录：

mysql -uroot –proot

设置远程访问（使用root密码）：

grant all privileges on *.* to 'root' @'%' identified by 'root';

flush privileges;

退出mysql，在centos环境下打开3306防火墙

/sbin/iptables -I INPUT -p tcp --dport 3306 -j ACCEPT

/etc/rc.d/init.d/iptables save

/etc/init.d/iptables status

11.3 安装tomcat部署项目
准备工作：将web项目打成war包，改名为ROOT.war

11.3.1 创建ucenter用户
一般情况下，发布应用程序都不是使用root用户的，需要创建一个普通用户来发布程序；

创建ucenter用户：

useradd -d /ucenter ucenter

设置密码：

passwd ucenter （密码 ucenter）

切换用户：

su - ucenter

11.3.2 安装Tomcat
tomcat只要解压就可以使用。

1、创建web目录
mkdir /ucenter/web

2、上传apache-tomcat-7.0.57.tar.gz

3、解压：tar -xvf apache-tomcat-7.0.57.tar.gz

4、重命名：mv apache-tomcat-7.0.57 itcast-usermanage

5、启动tomcat：
     cd itcast-usermanage/bin/
     ./startup.sh 或者 sh startup.sh

6、查看日志：
     tail -f ../logs/catalina.out

7、查看效果 http://192.168.0.160:8080/

发现无法访问：



8、防火墙打开 8080 端口
     /sbin/iptables -I INPUT -p tcp --dport 8080 -j ACCEPT

     /etc/rc.d/init.d/iptables save

9、安装成功



11.3.3 部署用户管理项目
1、上传usermanage.sql和ROOT.war到/ucenter/web

2、执行数据库脚本

     cat user_manager.sql | mysql -uroot -p123456

3、部署web程序

3.1 删除webapps下的所有文件

     cd /ucenter/web/usermanage/webapps
    
     rm -rf *

3.2 拷贝ROOT.war到webapps

     cp /ucenter/web/ROOT.war .

3.3 重新启动tomcat

     cd ../bin/
    
     sh startup.sh && tail -f ../logs/catalina.out

3.4 启动浏览器测试

注意事项：Centos环境下部署项目中文乱码问题解决方案

    今天在一台新的CentOS机器上使用c3p0连接池操作mysql数据库出现中文乱码问题，具体表现为：查询时无中文乱码问题，写数据时中文乱码，查看了机器上数据库字符集也是UTF8，应该不会出现中文乱码才对，最后在c3p0配置文件中 jdbcUrl后加上：?useUnicode=true&amp;characterEncoding=UTF8 中文就不会乱码了。

【C3P0配置文件】

<?xml version="1.0" encoding="UTF-8"?>
<c3p0-config>
  <default-config>
    <property name="driverClass">com.mysql.jdbc.Driver</property>
	<property name="jdbcUrl">jdbc:mysql://localhost:3306/user_manager_yun6?useUnicode=true&amp;characterEncoding=UTF8 </property>
	<property name="user">root</property>
	<property name="password">root</property>
	<property name="acquireIncrement">2</property>
	<property name="initialPoolSize">5</property>
	<property name="minPoolSize">1</property>
	<property name="maxPoolSize">5</property>
  </default-config>
</c3p0-config>
11.4 Linux下使用FastDFS
相关的安装包我打包到云盘上了，链接：https://pan.baidu.com/s/13NDYYil4mgLhkb5CYsc2Ww  提取码：66tn

单节点FastDFS

整个安装过程非常复杂，很容易出错，建议进行多次备份。

我们这里不打算安装多台虚拟机，因此会把tracker和storage都安装在一起。

11.4.1 安装gcc
GCC用来对C语言代码进行编译运行，使用yum命令安装：

yum -y install gcc
后面会用到解压命令（unzip），所以这里可以用yum把unzip 也装一下

yum install -y unzip zip
11.4.2 安装libevent
yum -y install libevent
11.4.3 安装libfastcommon-master
解压刚刚上传的libfastcommon-master.zip
unzip libfastcommon-master.zip

进入解压完成的目录
cd libfastcommon-master

编译并且安装：
./make.sh 
./make.sh install

11.4.4 安装fastdfs
tar -zxvf FastDFS_v5.08.tar.gz
cd FastDFS
./make.sh
./make.sh install
如果安装成功，会看到/etc/init.d/下看到提供的脚本文件：

ll /etc/init.d/ | grep fdfs


fdfs_trackerd 是tracker启动脚本

fdfs_storaged 是storage启动脚本

能够在 /etc/fdfs/ 目录下看到默认的配置文件模板：

ll /etc/fdfs/


tarcker.conf.sample 是tracker的配置文件模板

storage.conf.sample 是storage的配置文件模板

client.conf.sample 是客户端的配置文件模板

11.4.5 配置并启动tracker服务
1）首先将模板文件复制

cp /etc/fdfs/tracker.conf.sample /etc/fdfs/tracker.conf
2）修改复制后的配置文件：

vim /etc/fdfs/tracker.conf 
# 修改的内容如下：

base_path=/项目名/tracker                 # 存储日志和数据的根目录
3）新建目录：

mkdir -p /项目名/tracker
注意：关闭防火墙：

chkconfig iptables off
4）启动和停止

service fdfs_trackerd start # 启动fdfs_trackerd服务，停止用stop
检查FastDFS Tracker Server是否启动成功：

ps -ef | grep fdfs_trackerd
设置tracker服务开机启动:

chkconfig fdfs_trackerd on
11.4.6 配置并启动storage服务
1）首先将模板文件复制

cp /etc/fdfs/storage.conf.sample /etc/fdfs/storage.conf
2）修改复制后的配置文件：

vim /etc/fdfs/storage.conf
# 修改的内容如下:

base_path=/项目名/storage                 # 数据和日志文件存储根目录 

store_path0=/项目名/storage           # 第一个存储目录 

tracker_server=192.168.56.101:22122       #  tracker服务器IP和端口 
3）新建目录：

mkdir -p /项目名/storage
注意关闭防火墙： chkconfig iptables off

4）启动和停止

service fdfs_storaged start  # 启动fdfs_storaged服务，停止用stop
设置storage服务开机启动：

chkconfig fdfs_storaged on
ps -ef | grep fdfs



11.5 安装fastdfs-nginx-module
11.5.1 解压
tar -zxvf fastdfs-nginx-module_v1.16.tar.gz
11.5.2 修改config
1）进入src目录

cd fastdfs-nginx-module/src/
2）编辑config

vim config
使用以下底行命令：

:%s+/usr/local/+/usr/+g
将所有的/usr/local替换为 /usr，这个才是正确的目录:



11.5.3 配置nginx与FastDFS关联配置文件
复制 fastdfs-nginx-module 源码中的配置文件到/etc/fdfs 目录， 并修改

cp /usr/local/项目名/fastdfs-nginx-module/src/mod_fastdfs.conf /etc/fdfs/

vi /etc/fdfs/mod_fastdfs.conf
修改以下配置：

connect_timeout=10                       # 客户端访问文件连接超时时长（单位：秒）

tracker_server=192.168.56.101:22122    # tracker服务IP和端口

url_have_group_name=true                # 访问链接前缀加上组名

store_path0=/leyou/storage            # 文件存储路径
复制 FastDFS 的部分配置文件到/etc/fdfs 目录

cd /usr/local/项目名/FastDFS/conf/
cp http.conf mime.types /etc/fdfs/
11.6 安装Nginx的插件
11.6.1 如果没有安装过nginx
1、安装nginx的依赖库

yum -y install gcc pcre pcre-devel zlib zlib-devel openssl openssl-devel
2、解压安装包

tar -zxvf nginx-1.10.0.tar.gz

3、配置nginx安装包，并指定fastdfs-nginx-model

cd nginx-1.10.0

./configure --prefix=/opt/nginx --sbin-path=/usr/bin/nginx --add-module=/usr/local/leyou/fastdfs-nginx-module/src
注意：在执行./configure配置nginx参数的时候，需要将fastdfs-nginx-moudle源码作为模块编译进去。

4、编译并安装

make && make install
11.6.2 如果已经安装过nginx
1、 进入nginx目录：

cd /usr/local/项目名/nginx-1.10.0/
2、 配置FastDFS 模块

./configure --prefix=/opt/nginx --sbin-path=/usr/bin/nginx --add-module=/usr/local/项目名/fastdfs-nginx-module/src
注意：这次配置时，要添加fastdfs-nginx-moudle模块

3、编译，注意，这次不要安装（install）

make
4、替换nginx二进制文件:

备份：

mv /usr/bin/nginx /usr/bin/nginx-bak
用新编译的nginx启动文件替代原来的：

cp objs/nginx /usr/bin/
11.6.3 启动nginx
配置nginx整合fastdfs-module模块

我们需要修改nginx配置文件，在/opt/nginx/config/nginx.conf文件中：

vim  /opt/nginx/conf/nginx.conf
将文件中，原来的server 80{ ...} 部分代码替换为如下代码：

server {
    listen       80;
    server_name  image.项目名.com;
	# 监听域名中带有group的，交给FastDFS模块处理
    location ~/group([0-9])/ {
        ngx_fastdfs_module;
    }
    location / {
        root   html;
        index  index.html index.htm;
    }
    error_page   500 502 503 504  /50x.html;
    location = /50x.html {
        root   html;
    }
}
启动nginx：

nginx	# 启动nginx

nginx -s stop	# 停止nginx

nginx -s reload	# 重新载入配置文件
# 可通过ps -ef | grep nginx查看nginx是否已启动成功



11.6.4 设置nginx开机启动
创建一个开机启动的脚本：

vim /etc/init.d/nginx
添加以下内容：

#!/bin/sh
#
# nginx - this script starts and stops the nginx daemon
#
# chkconfig:   - 85 15
# description:  NGINX is an HTTP(S) server, HTTP(S) reverse \
#               proxy and IMAP/POP3 proxy server
# processname: nginx
# config:      /etc/nginx/nginx.conf
# config:      /etc/sysconfig/nginx
# pidfile:     /var/run/nginx.pid

# Source function library.
. /etc/rc.d/init.d/functions

# Source networking configuration.
. /etc/sysconfig/network

# Check that networking is up.
[ "$NETWORKING" = "no" ] && exit 0

nginx="/usr/bin/nginx"
prog=$(basename $nginx)

NGINX_CONF_FILE="/opt/nginx/conf/nginx.conf"

[ -f /etc/sysconfig/nginx ] && . /etc/sysconfig/nginx

lockfile=/var/lock/subsys/nginx

make_dirs() {
   # make required directories
   user=`$nginx -V 2>&1 | grep "configure arguments:.*--user=" | sed 's/[^*]*--user=\([^ ]*\).*/\1/g' -`
   if [ -n "$user" ]; then
      if [ -z "`grep $user /etc/passwd`" ]; then
         useradd -M -s /bin/nologin $user
      fi
      options=`$nginx -V 2>&1 | grep 'configure arguments:'`
      for opt in $options; do
          if [ `echo $opt | grep '.*-temp-path'` ]; then
              value=`echo $opt | cut -d "=" -f 2`
              if [ ! -d "$value" ]; then
                  # echo "creating" $value
                  mkdir -p $value && chown -R $user $value
              fi
          fi
       done
    fi
}

start() {
    [ -x $nginx ] || exit 5
    [ -f $NGINX_CONF_FILE ] || exit 6
    make_dirs
    echo -n $"Starting $prog: "
    daemon $nginx -c $NGINX_CONF_FILE
    retval=$?
    echo
    [ $retval -eq 0 ] && touch $lockfile
    return $retval
}

stop() {
    echo -n $"Stopping $prog: "
    killproc $prog -QUIT
    retval=$?
    echo
    [ $retval -eq 0 ] && rm -f $lockfile
    return $retval
}

restart() {
    configtest || return $?
    stop
    sleep 1
    start
}

reload() {
    configtest || return $?
    echo -n $"Reloading $prog: "
    killproc $nginx -HUP
    RETVAL=$?
    echo
}

force_reload() {
    restart
}

configtest() {
  $nginx -t -c $NGINX_CONF_FILE
}

rh_status() {
    status $prog
}

rh_status_q() {
    rh_status >/dev/null 2>&1
}

case "$1" in
    start)
        rh_status_q && exit 0
        $1
        ;;
    stop)
        rh_status_q || exit 0
        $1
        ;;
    restart|configtest)
        $1
        ;;
    reload)
        rh_status_q || exit 7
        $1
        ;;
    force-reload)
        force_reload
        ;;
    status)
        rh_status
        ;;
    condrestart|try-restart)
        rh_status_q || exit 0
            ;;
    *)
        echo $"Usage: $0 {start|stop|status|restart|condrestart|try-restart|reload|force-reload|configtest}"
        exit 2
esac
修改文件权限，并加入服务列表

# 修改权限
chmod 777 /etc/init.d/nginx 
# 添加到服务列表
chkconfig --add /etc/init.d/nginx 
设置开机启动

chkconfig nginx on
11.7 安装Elasticsearch
需要虚拟机JDK1.8及以上

11.7.1 新建一个用户leyou
出于安全考虑，elasticsearch默认不允许以root账号运行。

创建用户：

useradd leyou
设置密码：

passwd leyou
切换用户：

su - leyou
11.7.2 上传安装包,并解压
我们将安装包上传到：/home/leyou目录

解压缩：

tar -zxvf elasticsearch-6.2.4.tar.gz
我们把目录重命名：

mv elasticsearch-6.3.0/ elasticsearch


进入，查看目录结构：



11.7.3 修改配置
我们进入config目录：cd config

需要修改的配置文件有两个：



1、jvm.options

Elasticsearch基于Lucene的，而Lucene底层是java实现，因此我们需要配置jvm参数。

编辑jvm.options：

vim jvm.options
默认配置如下：

-Xms1g
-Xmx1g

内存占用太多了，我们调小一些：

-Xms512m
-Xmx512m

2、elasticsearch.yml

vim elasticsearch.yml
修改数据和日志目录：

path.data: /home/leyou/elasticsearch/data # 数据目录位置
path.logs: /home/leyou/elasticsearch/logs # 日志目录位置
我们把data和logs目录修改指向了elasticsearch的安装目录。但是这两个目录并不存在，因此我们需要创建出来。

进入elasticsearch的根目录，然后创建：

mkdir data
mkdir logs


修改绑定的ip：

network.host: 0.0.0.0 # 绑定到0.0.0.0，允许任何ip来访问
默认只允许本机访问，修改为0.0.0.0后则可以远程访问

11.7.4 运行
进入elasticsearch/bin目录，可以看到下面的执行文件：



然后输入命令：

./elasticsearch
或者后台运行：

./elasticsearch -d
11.7.5 错误1：内核过低


修改elasticsearch.yml文件，在最下面添加如下配置： 然后重启

bootstrap.system_call_filter: false
11.7.6 错误2：文件权限不足


我们用的是leyou用户，而不是root，所以文件权限不足。

首先用root用户登录。直接输入exit命令

然后修改配置文件:

vim /etc/security/limits.conf
添加下面的内容：

* soft nofile 65536

* hard nofile 131072

* soft nproc 4096

* hard nproc 4096
11.7.7 错误3：线程数不够
[1]: max number of threads [1024] for user [leyou] is too low, increase to at least [4096]

继续修改配置：

vim /etc/security/limits.d/90-nproc.conf 
修改下面的内容：

* soft nproc 1024
改为

* soft nproc 4096
11.7.8 错误4：进程虚拟内存
[3]: max virtual memory areas vm.max_map_count [65530] likely too low, increase to at least [262144]

vm.max_map_count：限制一个进程可以拥有的VMA(虚拟内存区域)的数量，继续修改配置文件， ：

vim /etc/sysctl.conf 
添加下面内容：

vm.max_map_count=655360
然后执行命令：

sysctl -p
11.7.9 重启终端窗口
所有错误修改完毕，一定要重启你的 Xshell终端，否则配置无效。

11.8 安装RabbitMQ
cd /usr/local/myapp

mkdir rabbitmq

cd rabbitmq
11.8.1 安装Erlang
1、在线安装

yum install esl-erlang_17.3-1~centos~6_amd64.rpm

yum install esl-erlang-compat-R14B-1.el6.noarch.rpm
2、离线安装



依次执行命令：

1）rpm -ivh esl-erlang-17.3-1.x86_64.rpm --force --nodeps



2）rpm -ivh esl-erlang_17.3-1~centos~6_amd64.rpm --force --nodeps



3）rpm -ivh esl-erlang-compat-R14B-1.el6.noarch.rpm --force --nodeps



11.8.2 安装RabbitMQ


安装：

rpm -ivh rabbitmq-server-3.4.1-1.noarch.rpm


11.8.3 设置配置文件
cp /usr/share/doc/rabbitmq-server-3.4.1/rabbitmq.config.example
/etc/rabbitmq/rabbitmq.config
开启用户远程访问

vi /etc/rabbitmq/rabbitmq.config


注意要去掉后面的逗号。

11.8.4 启动、停止
service rabbitmq-server start

service rabbitmq-server stop

service rabbitmq-server restart
11.8.5 开启web界面管理工具
rabbitmq-plugins enable rabbitmq_management

service rabbitmq-server restart
11.8.6 设置开机启动
chkconfig rabbitmq-server on
11.8.7 防火墙开放15672端口
/sbin/iptables -I INPUT -p tcp --dport 15672 -j ACCEPT

/etc/rc.d/init.d/iptables save
11.9 redis安装和配置
11.9.1 安装
解压

tar -xvf redis-4.0.9.tar.gz
编译安装

 mv redis-4.0.9 redis
 cd redis
 make && make install
11.9.2 配置
修改安装目录下的redis.conf文件

vim redis.conf
修改以下配置：

#bind 127.0.0.1 # 将这行代码注释，监听所有的ip地址，外网可以访问
protected-mode no # 把yes改成no，允许外网访问
daemonize yes # 把no改成yes，后台运行
11.9.3 启动或停止
redis提供了服务端命令和客户端命令：

redis-server 服务端命令，可以包含以下参数： start 启动 stop 停止

redis-cli 客户端控制台，包含参数： -h xxx 指定服务端地址，缺省值是127.0.0.1 -p xxx 指定服务端端口，缺省值是6379

11.9.4 设置开机启动
1) 输入命令，新建文件

vim /etc/init.d/redis
输入下面内容：

#!/bin/sh
# chkconfig:   2345 90 10
# description:  Redis is a persistent key-value database
PATH=/usr/local/bin:/sbin:/usr/bin:/bin

REDISPORT=6379
EXEC=/usr/local/bin/redis-server
REDIS_CLI=/usr/local/bin/redis-cli

PIDFILE=/var/run/redis.pid

CONF="/usr/local/leyou/redis/redis.conf"

case "$1" in  
    start)  
        if [ -f $PIDFILE ]  
        then  
                echo "$PIDFILE exists, process is already running or crashed"  
        else  
                echo "Starting Redis server..."  
                $EXEC $CONF  
        fi  
        if [ "$?"="0" ]   
        then  
              echo "Redis is running..."  
        fi  
        ;;  
    stop)  
        if [ ! -f $PIDFILE ]  
        then  
                echo "$PIDFILE does not exist, process is not running"  
        else  
                PID=$(cat $PIDFILE)  
                echo "Stopping ..."  
                $REDIS_CLI -p $REDISPORT SHUTDOWN  
                while [ -x ${PIDFILE} ]  
               do  
                    echo "Waiting for Redis to shutdown ..."  
                    sleep 1  
                done  
                echo "Redis stopped"  
        fi  
        ;;  
   restart|force-reload)  
        ${0} stop  
        ${0} start  
        ;;  
  *)  
    echo "Usage: /etc/init.d/redis {start|stop|restart|force-reload}" >&2  
        exit 1  
esac
然后保存退出

注意：以下信息需要根据安装目录进行调整：

EXEC=/usr/local/bin/redis-server # 执行脚本的地址

REDIS_CLI=/usr/local/bin/redis-cli # 客户端执行脚本的地址

PIDFILE=/var/run/redis.pid # 进程id文件地址

CONF="/usr/local/src/redis-3.0.2/redis.conf" #配置文件地址

2）设置权限

chmod 755 /etc/init.d/redis
3）启动测试

/etc/init.d/redis start
启动成功会提示如下信息：

Starting Redis server...
Redis is running...

4）设置开机自启动

chkconfig --add /etc/init.d/redis
chkconfig redis on
















[root@node1 ~]# vi /etc/sysconfig/network
NETWORKING=yes
HOSTNAME=node1






linux常用命令行：
一、基本命令：
关机  
    立即关机        shutdown -h now  
    5分钟后关机     shutdown -h 5  
    立刻关机        poweroff  
重启  
    立刻重启        shutdown -r now  
    5分钟后重启     shutdown -r 5  
    立刻重启        reboot  
帮助命令            --help  
                   shutdown --help  
    查看网卡信息    ifconfig --help  
man命令（命令说明书）注意：man shutdown打开命令说明书之后，使用按键q退出  
                    man shutdown  
二、目录操作命令
cd 目录  
    切换到根目录    cd /  
    根目录下的usr   cd /usr  
    切换到上一级    cd ../  或 cd..  
    切换到home      cd ~  
    切换到上次访问  cd -  
ls 目录查看  
    查看当前目录下  ls  
    查看当前目录包括隐藏文件      


