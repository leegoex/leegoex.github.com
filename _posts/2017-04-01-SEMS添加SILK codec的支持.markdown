---

layout: post
title: SEMS添加SILK codec支持
permalink: SEMS添加SILK codec支持.html
date: 01 April 2017

---     
SEMS默认是不会编译silk.so插件的，因此如果想要让SEMS支持SILK到其他编码的转换，必须手动给SEMS添加SILK的支持，即需要自己编译SEMS中的silk.so插件。编译的步骤是：

1.下载SILK\_SDK\_SRC_v1.0.8.zip

2.将SILK\_SDK\_SRC_v1.0.8.zip拷贝到SEMS源码目录的$(SEMS\_SRC\_ROOT)/core/plug-in/silk

3.进入到$(SEMS\_SRC_ROOT)/core/plug-in/silk，然后执行如下命令

    unzip SILK_SDK_SRC_v1.0.8.zip
    cd SILK_SDK_SRC_v1.0.8/SILK_SDK_SRC_FIX_v1.0.8
    make clean lib

执行如上的命令如果没有出现什么错误，则说明silk依赖的sdk已经编译好了。

4.进入到$(SEMS\_SRC_ROOT)/core/plug-in/silk，然后执行如下命令

    make
    make install


