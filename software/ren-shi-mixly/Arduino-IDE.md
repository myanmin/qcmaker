## 安装Arduino IDE

给Arduino写入程序需要使用Arduino IDE软件，通过类C语言来编写，后来，随着Arduino的流行，这种直接编写代码的方式使零基础的初学者感到了困难，所以有爱好者还有一些教育机构开发了很多图形化的编程软件。Mixly是北京师范大学教育学部创客教育实验室开发的，是给Arduino写入程序的图形化编程软件，它适合刚接触Arduino和编程的入门学习者。

Mixly可以看作是介于普通用户与Arduino IDE之间桥梁，通过这个桥梁，即使用户不懂C语言的语法，也可以利用图形化程序编写Arduino程序。Mixly的基本原理是将图形化程序转化成C语言，再利用Arduino IDE上传到硬件中。

1、安装包解压后如图 1.5-1，选择第一个，
![图 1.5-1](/assets/image058.jpg) 
打开后如图 1.5-2 所示，选择 arduino 应用程序，双击，按照步骤安装完成；
![图 1.5-2](/assets/image060.jpg)
安装完成打开时如图 1.5-3 所示，
![图 1.5-3](/assets/image062.jpg)
打开后的界面如图1.5-4 所示。
![图 1.5-4](/assets/image064.jpg) 

3、如果 Mixly 软件没有自动识别端口， 可首先打开端口观察插上 USB 线连接好之后那个端口新出现的，然后选择它；

4、我们也可以在 ArduinoIDE 中选择主控板类型和 COM 口，步骤如下 ：

1） 打开 ArduinoIDE，其编译环境如图 1.5-5所示

![图 1.1-7](/assets/image066.jpg) 

2） 在 ArduinoIDE 中选取甜橙 2.0 主控板型号为 Arduino/Genuino Uno，如图 1.1-8。

![图 1.1-8](/assets/image068.jpg)

图 1.1-8
3） 通过 MicroUSB 线将主控板连接到电脑的 USB 端口，在 ArduinoIDE 中选取与主控板对应的 COM 端口如图 1.1-9 所示，示例中主控板对应的端口为 COM6。

![图 1.1-9](/assets/image070.jpg)

注意：连接同一块甜橙板时，arduino IDE和Mixly识别的是同一个端口，故我们不能同时使用两个软件上传使用Mixly上传时，必须保证Arduino IDE的软件没有正在使用该端口上传程序，同理，也不能在arduino IDE上传程序时在Mixly上上传程序。