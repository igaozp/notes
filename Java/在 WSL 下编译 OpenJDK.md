### 获取 JDK 源码
以 OpenJDK 9 为例
```
wget http://hg.openjdk.java.net/jdk9/jdk9/archive/tip.zip
```
解压源码
```
unzip tip.zip
```

### 安装编译环境依赖
```
 sudo apt install build-essential gawk m4 openjdk-8-jdk libasound2-dev libcups2-dev libxrender-dev xorg-dev xutils-dev x11proto-print-dev binutils libmotif-common libmotif-dev ant
```

### 编译环境设置
需要对系统进行相关的环境设置

环境设置脚本：
```shell
# 设置语言选项，否则编译好后会有 HashTable 的 NPE 异常
export LANG=C

# Bootstrap JDK 安装路径，使用 JDK 1.8 实现自举
export ALT_BOOTDIR = /usr/lib/jvm/java-1.8.0-openjdk-amd64/

# 允许自动下载依赖
export ALLOW_DOWNLOADS = true

# 并行编译的线程数量
export HOTSPOT_BUILD_JOBS = 4
export ALT_PARALLEL_COMPILE_JOBS = 4

# 略过比较编译出的镜像与先前版本的差异
export SKIP_COMPARE_IMAGES = true

# 使用预编译头文件, 加快编译速度
export USE_PRECOMPILED_HEADER = true

# 选择要编译的内容
export BUILD_LANGTOOLS = true
# export BUILD_JAXP = false
# export BUILD_JAXWS = false
# export BUILD_CORBA = false
export BUILD_HOTSPOT = true
export BUILD_JDK = true

# 要编译的版本
# export SKIP_DEBUG_BUILD = false
# export SKIP_FASTDEBUG_BUILD =  true
# export DEBUG_NAME = debug

# 避开无关内容的编译
BUILD_DEPLOY = false

# 不编译出安装包
BUILD_INSTALL = false

# 设置存放路径
export ALT_OUTPUTDIR = ~/jdk_build/openjdk9/build/

# 删除环境变量, 否则会有警告
unset JAVA_HOME
unset CLASSPATH

make 2 > &1 | tee $ALT_OUTPUTDIR/build.log
```
