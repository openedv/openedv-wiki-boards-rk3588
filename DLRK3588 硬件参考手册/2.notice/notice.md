---
title: '2 ATK-DLRK3588B开发板硬件资源详细说明'
sidebar_position: 1
---

# 2 ATK-DLRK3588B开发板硬件资源详细说明

&emsp;&emsp;下面详细介绍ATK-DLRK3588B开发板底板的各部分硬件资源，便于用户详细了解底板硬件资源情况，按逆时针顺序依次介绍：

&emsp;&emsp;**1、5V电源输出**<br />
&emsp;&emsp;开发板板载1组5V电源输出排针（2*3）（JP2），该排针用于给外部提供5V的电源。<br />
&emsp;&emsp;用户在实验时可能会因为没有5V电源而苦恼不已，有了这组5V排针，就可以很方便地拥有一个简单的5V电源。


&emsp;&emsp;**2、3.3V电源输出**<br />
&emsp;&emsp;开发板板载1组3.3V电源输出排针（2*3）（JP1），用于给外部提供3.3V的电源。<br />
&emsp;&emsp;在做实验的时候如果需要3.3V电源（最大电流不能超过1000mA），那么就可以使用此电源，注意不能接功率太大的设备，一般用来接一些传感器之类的小功率器件，仅做应急3.3V电源使用。


&emsp;&emsp;**3、DC12V电源输入**<br />
&emsp;&emsp;开发板板载1个外部电源输入口（DC_IN），采用标准的直流电源插座。开发板板载了DC-DC芯片，用于给开发板提供高效、稳定的电源。如5V、3.3V等。建议使用正点原子开发板配套的12V电源供电。

&emsp;&emsp;**4、电源开关**<br />
&emsp;&emsp;开发板板载1个电源开关（S1）。该开关用于控制整个开发板的供电。这是一个两段式拨动开关，拨到上边打开开发板电源，整个板子开始供电，蓝色的电源指示灯(PWR1)点亮。<br />
&emsp;&emsp;拨到下边关闭开发板电源，整个开发板都将断电，蓝色的电源指示灯（PWR1）会随之熄灭

&emsp;&emsp;**5、千兆网络接口ETH0**<br />
&emsp;&emsp;这是开发板板载的1个1000M以太网接口，可以进行10/100/1000M网络通信。RK3588内部含有2个10/100/1000M以太网MAC外设，通过外接1000M网络PHY芯片，可以实现1000M有线网络。

&emsp;&emsp;**6、千兆网络接口ETH1**<br />
&emsp;&emsp;这是开发板板载的另一路1000M以太网接口。

&emsp;&emsp;**7、用户扩展IO口**<br />
&emsp;&emsp;这是开发板用户扩展IO端口，采用2×11排针，总共引出20个GPIO引脚，这些GPIO引脚用户可自行使用，用作I2C、SPI、串口等。另外还有2个ADC引脚，可以用来采集ADC数值。

&emsp;&emsp;**8、WIFI天线接口**<br />
&emsp;&emsp;这是开发板上的WIFI天线接口，开发板板载的一个WIFI模组(WIFI&蓝牙一体模组)，为USB接口，连接到了RK3588的USB20_HOST0接口上。模组为RTL8733，这个模组WIFI和蓝牙天线分开的，RTL8733支持5G WIFI，所以要使用5G&2.4G WIFI天线。

&emsp;&emsp;**9、BT天线接口**<br />
&emsp;&emsp;这是开发板上的蓝牙天线接口，也就是RTL8733的蓝牙天线接口。

&emsp;&emsp;**10、RTC实时时钟电池座**<br />
&emsp;&emsp;这是外置RTC芯片AT8563T的纽扣电池供电接口，用来在开发板断电的时候给RTC芯片供电，维持RTC的运行。<br />
&emsp;&emsp;开发板板载了一颗AT8563T芯片，这是一片外置的RTC实时时钟芯片，IIC接口。RK3588芯片内部没有RTC外设，需要外置一个RTC芯片。开发板出厂的时候默认都装上了一颗纽扣电池。

&emsp;&emsp;**11、六轴传感器**<br />
&emsp;&emsp;这是开发板板载的一个六轴传感器芯片(U15)，型号为SH3001，此芯片采用IIC接口与RK3588相连接。SH3001内部集成1个三轴加速度传感器和1个三轴陀螺仪，该传感器在姿态测量方面应用非常广泛。所以喜欢玩姿态测量的朋友，也可通过本开发板进行学习。

&emsp;&emsp;**12、按键**<br />
&emsp;&emsp;这是开发板板载的7个机械式输入按键，其中3个功能按键，UPDATE、PWRON和RESET。UPDATE按键用于系统烧写，PWRON按键是核心板上RK806-1这颗PMIC的上电按键，当RK3588不正常工作的时候可以按下PWRON按键重新上电。RESET是复位按键，用于复位整个开发板。<br />
&emsp;&emsp;另外4个按键是用户按键，采用ADC的方式实现，可以做为普通按键输入使用，默认用作菜单和音量加减按键。


&emsp;&emsp;**13、MIPI摄像头接口4**<br />
&emsp;&emsp;这是开发板的MIPI CSI摄像头接口4，支持4 Lanes，用于连接MIPI摄像头，比如正点原子出品的ATK-MCIMX335和ATK-MCIMX415摄像头。

&emsp;&emsp;**14、FAN接口**<br />
&emsp;&emsp;这是开发板上的散热风扇接口，这是一个4P接口，带有PWM调速功能，用来连接散热风扇，。如果在实际使用中发现RK3588工作温度太高的话，就可以安装散热风扇，提高散热能力。

&emsp;&emsp;**15、MIPI摄像头接口3**<br />
&emsp;&emsp;这是开发板的MIPI CSI摄像头接口3，功能和13一样。

&emsp;&emsp;**16、MIPI屏接口1**<br />
&emsp;&emsp;这是开发板的MIPI DSI屏幕接口，支持 4 Lanes，用于连接MIPI屏幕，比如正点原子出品的ATK-MD0550 5.5寸MIPI屏幕。

&emsp;&emsp;**17、MIPI屏接口0**<br />
&emsp;&emsp;这是开发板的MIPI DSI屏幕接口，功能和16一样。

&emsp;&emsp;**18、MIPI摄像头接口1**<br />
&emsp;&emsp;这是开发板的MIPI CSI摄像头接口1，功能和13一样。

&emsp;&emsp;**19、MIPI摄像头接口2**<br />
&emsp;&emsp;这是开发板的MIPI CSI摄像头接口2，功能和13一样。

&emsp;&emsp;**20、调试串口(Type-C)**<br />
&emsp;&emsp;这是开发板板载的一个USB Type-C接头（USB_TTL），用于USB连接CH343G芯片，从而实现USB转串口。同时，此USB Type-C接头也可以给开发板供电。<br />
&emsp;&emsp;在使用串口的时候要注意将开发板JP3的跳线帽接上，JP3跳线帽标号RX和TX是USB转串口的2个数据线（对CH343G来说）。而UART2_RX和UART2_TX则是RK3588串口2的RXD和TXD数据线。他们通过跳线帽连接在一起了，从而实现RK3588开发板与电脑之间串口通信，可以通过这个串口调试开发板。

&emsp;&emsp;**21、USB3.1 Type-C接口0**<br />
&emsp;&emsp;这是开发板板载的一个USB 3.1 Type-C接口，用于实现OTG功能，一般通过此接口来烧写系统以及ADB通信。此接口支持DP显示功能，需要购买Type-C转DP线来连接DP显示器。

&emsp;&emsp;**22、USB3.1 Type-C接口1**<br />
&emsp;&emsp;这是开发板板载的一个USB 3.1 Type-C接口，此接口也支持OTG功能，此USB口不能用来烧写系统和ADB通信。此接口也支持DP显示功能，通过Type-C转DP线来连接DP显示器。

&emsp;&emsp;**23、USB2.0 HOST接口**<br />
&emsp;&emsp;这个是开发板上的两个USB2.0 HOST接口，RK3588有两个原生的USB2.0 HOST接口：USB20_HOST1和USB20_HOST0。其中USB20_HOST0用来接USB WIFI&BT。因此使用USB20_HOST1来接CH334R这个HUB芯片，实现USB2.0接口扩展。这两路USB2.0 HOST接口就是扩展出来的，可以通过这两个USB2.0 HOST接口连一些低速USB设备。

&emsp;&emsp;**24、核心板接口**<br />
&emsp;&emsp;这是开发板底板上面的核心板接口，由4个2×50P、0.4mm间距的贴片板对板连接座母座组成，共400PIN。可以用来对插正点原子ATK-CLRK3588B核心板，从而进行RK3588处理器的开发、验证。

&emsp;&emsp;**25、HDMI接收接口**<br />
&emsp;&emsp;这是HDMI接收接口，RK3588集成了一路HDMI接收接口，可以接收其他设备发过来的HDMI信号。此HDMI RX接口支持HDMI 2.0、HDMI 1.4b，最高支持2160p@60Hz，支持RGB/YCbCr4:4:4或YCbCr4:2:2。

&emsp;&emsp;**26、HDMI输出接口1**<br />
&emsp;&emsp;这是HDMI输出接口1，RK3588集成了2路HDMI显示接口，这是其中一个HDMI TX接口，最高支持7680×4320@60Hz，通过此接口连接HDMI显示器，实现高清显示输出。

&emsp;&emsp;**27、单声道喇叭**<br />
&emsp;&emsp;这是开发板板载的一个1W小喇叭。

&emsp;&emsp;**28、HDMI输出接口0**<br />
&emsp;&emsp;这是另外一个HDMI输出接口0，同样最高支持7680×4320@60Hz。

&emsp;&emsp;**29、CAN接口**<br />
&emsp;&emsp;这是开发板板载的CAN总线接口（CAN），通过2个端口和外部CAN总线连接，即CANH和CANL。这里提醒大家：CAN通信的时候，必须CANH接CANH，CANL接CANL，否则可能通信不正常！

&emsp;&emsp;**30、可调电位器**<br />
&emsp;&emsp;这是开发板上一个10K的可调电位器，连接到了RK3588的ADC引脚上，可以用来学习RK3588的ADC采集。

&emsp;&emsp;**31、TF卡槽**<br />
&emsp;&emsp;这是开发板板载的一个标准TF卡接口（TF_CARD），采用小型的TF卡接口，SDMMC方式驱动，有了这个TF卡接口，就可以满足大容量数据存储的需求。

&emsp;&emsp;**32、扬声器外接接口**<br />
&emsp;&emsp;开发板板载2路扬声器外接接口，其中一路扬声器接口SPKR已在开发板接入一个小扬声器，方便用户进行音频播放测试。

&emsp;&emsp;**33、MIC(咪头)**<br />
&emsp;&emsp;这是开发板的板载录音输入口（MIC），开发板板载了ES8388这个音频编解码芯片，该咪头连接到ES8388的MIC输入引脚上，可以用来实现录音功能。

&emsp;&emsp;**34、耳机接口**<br />
&emsp;&emsp;开发板板载1个耳机接口。耳机座规格为PJ-342单柱带T，该接口可以插4段式3.5mm的耳机，支持录音与放音。放音时，支持耳机热插拔；录音时，支持耳机录音和板载麦克风MIC两种方式进行录音。


&emsp;&emsp;**35、Nano SIM卡接口**<br />
&emsp;&emsp;开发板板载1个Nano SIM卡接口，如果需要使用5G模块进行无线数据传输，就需要在此接口插入Nano SIM卡。

&emsp;&emsp;**36、SATA POWER接口**<br />
&emsp;&emsp;这是开发板的SATA硬盘电源接口，当使用SATA硬盘的时候需要通过此电源接口给SATA硬盘供电，提供+12V和+5V电源。

&emsp;&emsp;**37、SATA硬盘接口**<br />
&emsp;&emsp;这是开发板的SATA机械硬盘接口，可以连接机械硬盘这种大容量存储，使用SATA硬盘的时候需要接上SATA电源。

&emsp;&emsp;**38、RS232接口（母）**<br />
&emsp;&emsp;这是开发板板载的一个RS232接口（COM1），通过一个标准的DB9母头和外部的串口连接。通过这个接口，我们可以连接带有串口的电脑或者其他设备，实现串口通信。在使用的时候需要将JP6的两个跳线帽插到上面，也就是将RK3588的UART3用作RS232。


&emsp;&emsp;**39、RS485接口**<br />
&emsp;&emsp;这是开发板板载的RS485总线接口（RS485），通过2个端口和外部485设备连接。这里提醒大家，RS485通信的时候，必须A接A，B接B。否则可能通信不正常。正点原子ATK-DLRK3588B开发板的RS232和RS485复用RK3588的UART3，所以在使用RS485功能的时候需要将JP6的两个跳线帽插到下面，也就是将RK3588的UART3用作RS485。


&emsp;&emsp;**40、5G接口**<br />
&emsp;&emsp;这是开发板板载的一个B_KEY座子，用来连接5G模组，本质上走的USB3.0协议，通过此接口可以连接5G模块，比如移远的RM500U。接上5G模块以后RK358开发板就可以实现5G上网功能，对于不方便布网线或者没有WIFI的场合来说是个不错的选择。

&emsp;&emsp;**41、PCIE WIFI&BT接口**<br />
&emsp;&emsp;这是开发板板载的一个PICE接口WIFI&BT座，为E_KEY类型座子，可以用来连接第三方的PCIE WIFI&BT模组。虽然正点原子ATK-DLRK3588B开发板已经板载了一个RTL8733 WIFI&BT模组，但是RTL8733性能有限。如果对WIFI性能有要求的话，就可以在此接口接上第三方的PCIE WIFI&BT模组，实现更高性能的WIFI通信。

&emsp;&emsp;**42、SSD接口**<br />
&emsp;&emsp;这是开发板板载的一个M.2 SSD接口，采用M_KEY座子，走PCIE通道，可以用来连接2280规格的SSD固态硬盘。




