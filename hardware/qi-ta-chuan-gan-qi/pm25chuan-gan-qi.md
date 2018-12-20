## 4.7 PM2.5传感器

![](/assets/硬件1218865.png)




### 4.7.1简介

**PM2.5粉尘传感器**GP2Y10 14 7810空气质量PM2.5检测是一款光学空气质量传感器，即PM2.5传感器，其内部对角安放着红外线发光二极管和光电晶体管，使得其能够探测到空气中尘埃反射光，即使非常细小的如烟草烟雾颗粒也能够被检测到，通常在空气净化系统中应用。可测量0.8微米以上的微笑粒子,感知烟草产生的咽气和花粉,房屋粉尘等.体积小,重量轻,便于安装。

![](/assets/硬件1218866.png)

PM2.5激光粉尘传感器是一款数字式通用颗粒物浓度传感器，可以用于获得单位体积内空气中0.3～10微米悬浮颗粒物个数，即颗粒物浓度，并以数字接口形式输出，同时也可输出每种粒子的质量数据。本传感器可嵌入各种与空气中悬浮颗粒物浓度相关的仪器仪表或环境改善设备，为其提供及时准确的浓度数据。

### 4.7.2 灰尘传感器在 Mixly 中使用示例

硬件连接如下图4.7-1所示：粉尘传感器适配器的模拟输出口与甜橙版A0相连；D2接单色LED灯。

![图4.7-1](/assets/硬件1219275.png)





在Arduino IDE 中输入如下的程序：



`/*`

`Standalone Sketch to use with a Arduino UNO and a`

`Sharp Optical Dust Sensor GP2Y1010AU0F`

`*/`



`int measurePin = A0; //Connect dust sensor to Arduino A0 pin`

`int ledPower = 2; //Connect 3 led driver pins of dust sensor to Arduino D2`



`int samplingTime = 280;`

`int deltaTime = 40;`

`int sleepTime = 9680;`



`float voMeasured = 0;`

`float calcVoltage = 0;`

`float dustDensity = 0;`



`void setup(){`

`Serial.begin(9600);`

`pinMode(ledPower,OUTPUT);`

`}`



`void loop(){`

`digitalWrite(ledPower,LOW); // power on the LED`

`delayMicroseconds(samplingTime);`



`voMeasured = analogRead(measurePin); // read the dust value`



`delayMicroseconds(deltaTime);`

`digitalWrite(ledPower,HIGH); // turn the LED off`

`delayMicroseconds(sleepTime);`



`// 0 - 5V mapped to 0 - 1023 integer values`

`// recover voltage`

`calcVoltage = voMeasured * (5.0 / 1024.0);`



`// linear eqaution taken from`[`http://www.howmuchsnow.com/arduino/airquality/`](http://www.howmuchsnow.com/arduino/airquality/)

`// Chris Nafis (c) 2012`

`dustDensity = 0.17 * calcVoltage - 0.1;`



`Serial.print("Raw Signal Value (0-1023): ");`

`Serial.print(voMeasured);`



`Serial.print(" - Voltage: ");`

`Serial.print(calcVoltage);`



`Serial.print(" - Dust Density: ");`

`Serial.println(dustDensity); // unit: mg/m3`



`delay(1000);`

`}`

通过串口监视器观察，如下图4.7-2所示：

![图4.7-2](/assets/硬件1220562.png)


### 4.7.3 灰尘传感器模块应用场景举例

灰尘传感器被广泛应用于大气测量、火灾、烟气测量及工业锅炉、窑炉、化工厂排烟测量等领域。也可以用于各种布袋除尘器的破损检测及各种类型除尘器除尘效率的测量，为这些领域的自动化控制提供可靠的信号。

例如：[空气净化器](https://baike.sogou.com/lemma/ShowInnerLink.htm?lemmaId=122884&ss_c=ssc.citiao.link)和[空气清新机](https://baike.sogou.com/lemma/ShowInnerLink.htm?lemmaId=122884&ss_c=ssc.citiao.link)、空调、空气质量监控仪、空调等相关产品。

