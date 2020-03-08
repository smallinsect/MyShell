# MyShell

shell命令笔记本

修改root密码 sudo passwd root

切换到用户密码 su root

打开终端快捷键 ctrl+alt+t

查看所有进程 查询ssh的进程 ps -e | grep ssh

安装软件
sudo apt-get install openssh-server
sudo apt-get install vim
更新软件 sudo apt-get update
更新软件包 sudo apt-get upgraded
大版本变化 sudo apt-get dist-upgraded

查看登录的用户 有哪些用户等连接机器 who
用户退出 exit

清屏 clear

当前目录 pwd
查看命令使用方法 man pwd
查看目录下的文件 ls
ls -l和ll一样
drwxr-xr-x d是目录 普通文件是- r可读文件 w可写文件 x可执行文件
cd /开始 绝对路径
cd 账户的主目录 ~表示自己的主目录下面
cd home/..... 相对路径
cd .当前目录
cd ..上一级目录

显示所有的txt文件 ls *.txt *表示任意多个字符 ?一个字符
创建文件 touch abc.txt

拷贝文件 cp aaa.txt bbb.txt
查看文件属性 ls -l aaa.txt bbb.txt

ls -sail *.txt
拷贝文件询问 cp -i aaa.txt bbb.txt
拷贝文件链接 cp -l aaa.txt ccc.txt ccc.txt就是aaa.txt文件别名 硬链接
软连接 cp -s aaa.txt bbb.txt 可以跨文件系统
ln 相当于 cp -s命令

删除文件 rm 删除文件是真的把文件删除了
文件硬盘地址        文件链接数
919949 4 -rw-rw-r-- 2 usmall usmall 20 8月   2 15:53 aaa.txt
919858 0 -rw-rw-r-- 1 usmall usmall  0 8月   2 15:41 abc.txt
919950 4 -rw-rw-r-- 1 usmall usmall 20 8月   2 15:54 bbb.txt
919911 4 -rw-rw-r-- 1 usmall usmall 20 8月   2 15:54 ccc.txt
919949 4 -rw-rw-r-- 2 usmall usmall 20 8月   2 15:53 ddd.txt

建立目录 mkdir 文件目录名
创建连续目录 mkdir -p a/b/c/d
删除目录 rmdir 目录名
递归删除 rm -r 目录名

详细文件信息 stat aaa.txt
查看文件编码 file aaa.txt

sudo !!执行上次命令

cat 文件名
more aaa.txt 分页查看文件
less aaa.txt
tail aaa.txt 查看文件后10行 用来查看程序的打印log文件
tail -n 3 aaa.txt 查看后3行
tail -f -n 3 aaa.txt 末尾有数据更新时 会及时刷出来的
head aaa.txt 查看文件的前10行

查看当前系统运行了什么程序
ps命令
ps -ef e显示所有的进程 f输出所有属性
pid 是进程id
ppid 是父进程id
stime 系统启动时间
TTY 终端打开
TIME 
CMD 启动命令

ps al a显示所有的 l列表显示
ps axgl 
ps --forest
实施查看进程信息 top
实施查看进程信息界面好看的用 htop

killall 关闭程序名字
kill 关闭程序id
kill -9 强制杀掉程序
kill -s INT 程序

df查看磁盘空间
df -h增加可读性
du
du -h

grep查看文件
grep apple test.txt 查看test.txt文件里面apple单词
grep -c apple test.txt 包含apple行数
grep -v apple test.txt 不包含apple的行
grep -n apple test.txt 显示行数

zip 打包 unzip解包
tar 压缩解压

echo $PATH 打印环境变量
printenv查看全局变量
vim ~/.hashrc 配置shell相当于windows的bat文件

wim fff.sh创建shell文件
chmod +x fff.sh添加可执行文件
chmod +xwr 添加可执行 可写 可读属性
chmod -xwr 删除可执行 可写 可读属性


nc 192.168.3.58 8080



linux文件目录路径
bin 执行文件
boot 启动文件
dev 设备文件
etc 配置文件
home 用户主目录文件
lib 库目录
lib64 64位库目录
lost+found
media 挂载目录
opt 可选目录
root 根的主目录
sbin 
sys 系统主目录
tmp 临时文件目录
usr 用户装的软件
var 
