目的
==
这个工程用来帮助你使用VC编译器来编译使用autotool作为编译系统的工程。

使用方法
====
首先你需要下载cygwin，然后将VC的头文件搜索路径设置在INCLUDE环境变量中。
将库搜索路径设置在LIBS环境变量中。然后将要使用的编译器代理脚本设置到PATH
环境变量中。
在配置时使用
./configure --host=cygwin-msvc
就可以使用vc的命令行进行编译了。
另外可以通过调整DEBUG环境变量来开启DEBUG模式的编译。
export DEBUG=1