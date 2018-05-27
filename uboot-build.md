# Uboot Build Reference

发布版本：1.0

作者邮箱：703632667@qq.com

日期：2018-05-20

---

**前言**

适用于uboot编译。

**修订记录**

|日期|版本|作者|修改说明|
|---|-----|---|---|
|2018-05-20|V1.0|Jason Zhu| |

---

[TOC]

## 1. 编译工具选择 

###1.1. ubuntu apt安装

对于armv7的编译，可以选择安装

~~~
sudo apt-get install gcc-arm-linux-gnueabi
~~~

对于armv8或arm64，可以选择安装

~~~
sudo apt-get install gcc-aarch64-linux-gnu
~~~

###1.2. 直接使用现成的工具链

github地址为

~~~
git@github.com:zhuzhizhan/gcc-arm32.git
git@github.com:zhuzhizhan/gcc-arm64.git
~~~
## 2. 编译uboot

###2.1 apt安装编译链编译

32位编译

~~~
make CROSS_COMPILE=arm-linux-gnueabi- <board_name>_defconfig
make
~~~

64位编译

~~~
make CROSS_COMPILE=aarch64-linux-gnu- <board_name>_defconfig
make ARCH=arm CROSS_COMPILE=aarch64-linux-gnu-
~~~

### 2.2现成工具链编译

把CROSS_COMPILE=下载的工具链路径即可。