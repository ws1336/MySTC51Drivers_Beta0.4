# MySTC51Drivers
自用的51单片机硬件驱动库

版本说明：
............................................................
版本号Beta0.0
本版本主要包含以下驱动（xxx.c文件和xxx.h文件共同使用,下面不再写后缀）
1“define.h”----包含了类型定义与开发板属性的设置（如晶振频率等）
2“delay”----定义了两个延时函数，支持STC大多数芯片（除15H系列..）
【重要提示】本函数库中函数基本上都依赖于"delay.c""delay.h"和"define.h"文件，这三个文件一定要包含！！！
3“digital_display”----数码管显示驱动（硬件是基于两个373锁存器分别用作段数据和位数据）
4“digital_to_string”----包含了浮点数转换成字符串的函数
5“DS18B20”----温度传感器驱动
6“DS1302”----时钟芯片驱动
7“I2C”----软件模拟I2C总线驱动
8“Keyboard”----矩阵键盘驱动
9“LCD_1602_display”----1602液晶屏驱动（并口）
10“LCD_12864_display”----12864液晶屏驱动（并口带中文字库）（只是显示文字，不包含画图）
11“NEC_IR_coding”----用一个红外LED实现红外编码发射的驱动
12“NEC_IR_decoding”----红外解码驱动
13“NRF24L01”----2.4G无线通讯模块驱动
14“Uart”----串口驱动相关函数	
............................................................
............................................................
版本号Beta0.1
修复了数码管有关残影的bug
取消了矩阵键盘的松手检测，检测不到键按下时返回0代替
............................................................
............................................................
版本号Beta0.2
加入了独立按键的检测，兼容矩阵按键，修复了矩阵键盘关于不同开发板兼容性的bug
增加了串口不同波特率的初始化程序
............................................................
............................................................
版本号Beta0.3
调整了数码管显示驱动的结构代码，方便不同开发板移植
调整了红外解码阈值，提高解码效率
............................................................
............................................................
版本号Beta0.4
1602液晶驱动的代码更改为区域刷新，字符串长度不够显示空格，避免出现显示残留
调整了若干驱动文件名字
修复了数字转字符串函数在显示0时有负号的bug
添加了QMC5883地磁场传感器驱动
............................................................
............................................................
版本号Beta0.5
添加了STC12C5A60S2的AD转换驱动库
添加了BH1705光照强度传感器驱动库
添加了DHT11温湿度传感器驱动库
添加了SD卡的SPI模式驱动库
添加了Petit Fatfs文件系统
添加了步进电机的简单驱动
修复了my_printf函数连续调用时输出乱码问题等
以上都进行了实物测试成功
............................................................
