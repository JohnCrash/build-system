目的
==
这个工程用来帮助你使用VC编译器来编译使用autotool作为编译系统的工程。<br/>

使用方法
====
###msvc
首先你需要下载cygwin，然后将VC的头文件搜索路径设置在INCLUDE环境变量中。<br/>
将库搜索路径设置在LIBS环境变量中。然后将要使用的编译器代理脚本设置到PATH
环境变量中。<br/>
在配置时使用<br/>
./configure --host=cygwin-msvc
就可以使用vc的命令行进行编译了。<br/>
另外可以通过调整DEBUG环境变量来开启DEBUG模式的编译。<br/>
export DEBUG=1<br/>
一些情况导致libtool不能讲过库传递给编译器，可以使用环境变量msvc_LDFLAGS <br/>
这确保在链接时附加给定的库。多个库可以用空格分割。<br/>

###ndk
需要配置NDK环境变量，和NDK_TOOLCHAINS。<br/>
有两种方法来配置NDK的编译环境，可以参加NDK文档docs/STANDALONE-TOOLCHAIN.html。<br/>
一种你需要设置环境变量NDK_PLATFORM，并且NDK_TOOLCHAINS在NDK路径之下。<br/>
也就文档中说的hard mode。还可以使用easy mode创建一个独立的编译环境。然后配置NDK_TOOLCHAINS。<br/>