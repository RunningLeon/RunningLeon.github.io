---
title: windows下同时安装python2和python3以及pip2和pip3
date: 2017-08-08 20:34:30
tags: python pip
---

##一.安装python2 python3
官网下载地址: [download](https://www.python.org/downloads/)

图文安装教程请点击: [转载~](http://www.cnblogs.com/hongten/p/hongten_python_install.html)



*注:python3安装时可以选择自动添加环境变量,如果没有选择,安装后请手动添加环境变量.*

##二.修改python.exe的名字
分别找到python2 和python3的安装目录, 比如`C:\Python27\, C:\Python36\`,将这连个目录下的python.exe文件名重命名为python2,python3.

win+R 输入cmd进入命令行分别输入`python2 -V, python3 -V `进行验证,结果如下图,表面修改成功!

![ops](http://i.imgur.com/OvrHuKu.png)

##三.重新安装pip2, pip3
cmd命令行中分别输入:
    
`python2-m pip install --upgrade pip --force-reinstall`
`python3-m pip install --upgrade pip --force-reinstall`

成功安装图如下:

![ops](http://i.imgur.com/PrNaI0V.png)

分别输入pip2 -V   pip3 -V 进行验证,如下图:

![ops](http://i.imgur.com/7o4TfkP.png)

以后就可以分别用pip2 install ... pip3 install 分别安装各自版本的package.

