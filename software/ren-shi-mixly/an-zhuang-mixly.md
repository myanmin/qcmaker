## 安装Mixly

### 1、得到解压后无损坏的安装包

通常，提供的安装包为后缀是RAR格式，需要解压缩，可以用好压等解压软件进行解压；

zip格式的压缩包不需要专门的解压软件，可以直接解压，解压后的文件夹，可以打开直接安装。

注意：端口驱动一般会包含在解压后的文件夹里，如图1.1-1所示：

![img](/assets/image002.jpg)

图1.1-1

Q&A

Q1：电脑上没有解压缩软件，没法打开压缩包。

A1：安装解压软件如：好压、12345解压等软件。

Q2：安装包解压缩失败？

A2：解压后路径太长，需要解压到较短路径下，如解压到c盘；路径名称中有中文有时候也会解压出错

### 2、安装Mixly

得到解压后的安装包之后，如图1.1-2所示，打开文件，还会有一层路径，再打开，画面如图1.1-3所示；

![img](/assets/image004.jpg)

图1.1-2

![img](/assets/image006.jpg)

图1.1-3

 点击图1.1-4所示图标，打开软件，界面如图1.1-5所示，即完成安装。

![img](/assets/image008.jpg)

图1.1-4

![img](/assets/image010.jpg)

图1.1-5

Q&A

Q:安装包出错，有如下五种表现：

a、打开软件，不出现基本模块区，如图1.1-6；

![33055598100164778](/assets/image012.gif)

图1.1-6

b、打开Mixly的功能区正常，但程序编写完成好无法编译通过，无法上传成功，下方的显示信息区出现如下方的代码，

如图1.1-7所示：

Java.lang.NullpointerException

​     at.org.mixly.Browser_new.upload(Browser_new.java:2004)

​     at.org.mixly.Browser_new.accessS43(Browser_new.java:1938)

​     at.org.mixly.Browser_newS54.run(Browser_new.java:1753)

​     at.java.lang.Thread.run(Thread.java:748)

上传失败！

![img](/assets/image014.jpg)

图1.1-7

c、打不开软件，点击图标快捷方式、解压包的图标均无反应；

d、端口、版型选择均正确，写完程序后，点击“上传”信息显示区却没有编译的代码，如图1.1-8所示：

![307136813443371144](/assets/image016.jpg)

图1.1-8

e、打开软件后，软件无响应，Mixly的软件画面变成灰色，出现一个窗口，标题是“java(TM) Platform SE binary 未响应”严重时导致电脑死机，此时必须重启电脑。错误画面如下图1.1-9；

![810709004138676454](/assets/image018.jpg)

图1.1-9

A:重新安装软件Mixly,把当前有问题的压缩包、快捷方式和解压缩的文件删除，重新安装完新的驱动和软件。