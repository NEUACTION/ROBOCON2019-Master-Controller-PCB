# 2019ROBOCON大赛主控PCB开源

标签：STM32F407VET6 ACTION 主控PCB Altium-Designer

---
>该文件仅用于萝卜坑坑友的相互交流，请勿用于商业用途。
我们深知还有很多不足之处，十分欢迎广大坑友前来交流，或者在GitHub的`Issues`中留言指出。

开源网址：https://github.com/NEUACTION/Master-Controller-PCB

文件中包含主控的`工程文件`，`PCB文件`，`原理图文件`和`部分模块更新版原理图`。我们后来对STM32F407，AMS117，LM4120的原理图有所更改，改版后的原理图就在`部分模块更新版原理图`这个文件夹中。大家重新画板子的时候这些模块建议参考这个原理图。

## 接口介绍
![AD-3D图](https://github.com/NEUACTION/Master-Controller-PCB/blob/master/AD-3D%E5%9B%BE.png?raw=true)

（以下数字对应图上的标号）

1：下载口（我们烧录程序使用的是3线Jlink，制作方法可以参考以下两个链接）
   http://forum.eepw.com.cn/thread/222232/1
   http://forum.eepw.com.cn/thread/211068/1
   
2：普通按键

3，4：232通信接口（**由于MAX3232芯片限制，通信波特率建议最大115200**）

5，10：CAN通信接口

6：**5V**供电接口（**一定不要接错电压！！！**）

7：单片机复位按键

8，9：TTL通信接口

11，12：CAN通信的电阻选择开关（开关打开时，该节点接入120Ω的电阻）

**其余没有用到的单片机引脚均使用排针引出，大家可以根据自己的需求设计下层板扩展功能。**

## 元器件型号
具体芯片型号原理图上有标识，基本元器件（如电容电阻）的参数以comment为准

## 丝印介绍
图上丝印如接口8处的`R2A3`表示USART2的RX，使用的是PA3引脚，以此类推......

**最后就是我们的实物图了~**

![焊接完成](https://github.com/NEUACTION/Master-Controller-PCB/blob/master/%E5%AE%9E%E7%89%A9%E5%9B%BE.jpg?raw=true)

 

