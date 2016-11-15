#### Linux 常用命令简记

系统信息显示

```
date                      # 当前日期时间 
cal                       # 日历
uptime                    # 当前更新的时间
w                         # 在线用户信息
whoami                    # 当前登录用户的用户名
finger user               # 关于user用户的信息
uname -a                  # 内核信息 
cat /proc/cpuinfo         # CPU信息
cat /proc/meminfo         # 内存信息
man command               # 查找关于command命令的手册
df                        # 磁盘使用情况
du                        # 当前目录下文件的空间占用情况
free                      # 内存和交换空间的使用情况
whereis app               # app可能出现的位置
which app                 # app运行时默认的运行位置
```

文件解压缩

```
tar cf file.tar files      # 将files文件夹或文件, 打包为file.tar
tar xf file.tar            # 解压file.tar
tar czf file.tar.gz files  # 使用gzip创建压缩文件file.tar.gz
tar xzf file.tar.gz        # 使用gzip解压file.tar.gz
tar cjf file.tar.bz2       # 使用bzip2创建压缩文件file.tar.bz2
tar xjf file.tar.bz2       # 使用bzip2解压file.tar.bz2
gzip file                  # 将file文件压缩并重命名为file.gz
gzip -d file.gz            # 解压缩file.gz
```

进程管理

```
ps                         # 显示当前活动进程
top                        # 显示所有运行中的进程
kill pid                   # 终止ID为pid的进程
killall proc               # 终止所有名为proc*的进程
bg                         # 列出已终止或后台运行的进程
fg                         # 将最近的后台任务调至前台
fg n                       # 将任务n调至前台
```

网络相关

```
ping host                  # ping主机地址并显示结果
whois domain               # 获取domain域名的whois信息
dig domain                 # 获取domain域名的DNS信息
dig -x host                # 反向查询host主机
wget file                  # 下载文件
wget -c file               # 继续已停止的下载
```

安装软件

```
# 从源码安装软件
./configure
make
make install 

dpkg -i pkg.deb            # 安装deb格式的软件包
rpm -Uvh pkg.rpm           # 安装rpm格式的软件包
```

搜索相关

```
grep pattern files         # 查找匹配pattern模式的文件
grep -r pattern dir        # 在目录下递归查找匹配pattern模式
command | grep pattern     # 在command命令的输出中查找匹配pattern的信息
locate file                # 查找file文件的所有实例
```

文件权限

```
chmod octal file           # 为文件设置octal数字所代表的权限
chmod 777 file             # 所有人可以完全控制file文件
chmod 755                  # 文件创建者可以完全控制file文件, 组内成员和其他人只能读取和执行
4:读取(r)
2:写入(w)
1:可执行(x)
```

文件相关

```
ls                        # 列出目录
ls -al                    # 列出所有文件目录的信息
cd dir                    # 切换到dir目录下
cd                        # 切换到home目录下
pwd                       # 显示当前目录
mkdir dir                 # 创建目录
rm file                   # 删除file文件
rm -r dir                 # 删除dir目录下的内容
rm -f file                # 强制删除file文件
rm -rf dir                # 强制删除dir目录下的内容
cp file1 file2            # 复制文件
cp -r dir1 dir2           # 复制文件夹
mv file1 file2            # 重命名文件或移动文件
ln -s file link           # 创建符号连接
touch file                # 创建或更新文件
more file                 # 输出文件内容
head file                 # 输出文件前10行的内容
tail file                 # 输出文件后10行的内容
```

