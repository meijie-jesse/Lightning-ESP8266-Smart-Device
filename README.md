# Lightning-ESP8266-Smart-Device
RGBWW LED driver 五路LED调光驱动板

![image](https://github.com/meijie-jesse/Lightning-ESP8266-Smart-Device/blob/master/images/Lightning4.jpg)

![image](https://github.com/meijie-jesse/Lightning-ESP8266-Smart-Device/blob/master/images/Lightning2.jpg)


尺寸是70x63，五路输出：

Red is on GPIO15
Green is on GPIO13
Blue is on GPIO12
White 1 (W1) is on GPIO14
White 2 (W2) is on GPIO4

电路中去掉了8266的复位键，只有一个boot键用来下载程序。当然，第一次用串口烧录进去程序了之后就可以用OTA升级了，boot键其实也可以省的，为了第一次下载方便还是保留了。
降压电路采用的是MP2451，最大支持到36V的输入。但是电源电压请以灯条的为准，一般都是12V或者24V。
MOS管设计采用的是DTU35N06，最大连续电流35A，足够灯条去造了，也可采用其他的MOS管，看下参数替换即可，实际我采用的是AOD484，我画的这个焊盘超级大，所以N沟道的MOS直接无脑替换即可。
GPIO到MOS管中间用了一片74HC245来保护，但是为了稳定还是加上了，也可以不用，直接短接A到B的引脚即可。
板子背部为了承受大电流，主供电底层阻焊挖掉，可以在上面堆锡。

## 功耗测试：
单路输出：
![image](https://github.com/meijie-jesse/Lightning-ESP8266-Smart-Device/blob/master/images/Lightning3.jpg)

五路输出：
![image](https://github.com/meijie-jesse/Lightning-ESP8266-Smart-Device/blob/master/images/Lightning5.jpg)

调光视频：
![image](https://github.com/meijie-jesse/Lightning-ESP8266-Smart-Device/blob/master/images/Lightning_showtime.gif)
