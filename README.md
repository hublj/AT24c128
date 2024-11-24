AT24C128测试


注意细节，AO,A1,A2,都接GND.


SCL和SDA分别接上拉电阻10K。


写入和读取，每个字节最少要5ms，才能正确写入和读写（数据手册）。


I2C通讯协议，通讯频率最大100KHZ,(可设置10~100KHZ范围）


供电电压3.3v,或5v.


24C128的I2C地址，0x50


自定义SDA和SCL引脚，只能D+数字，不能只填写引脚数字（如:"D10,D9......")


等待足够的时间以确保写入完成
delay(100)





芯片对比介绍
型号	        容量bit	容量byte	页数	字节/页	器件寻址位	可寻址器件数	WordAddress位数/字节数	备注


AT24C32        32k	    4k	     128	    32	   A2A1A0	       8	        12/2	


AT24C64        64k	    8k     	256	    32	   A2A1A0	       8        	13/2	


AT24C128	    128k	   16k   	  256	    64	   A1A0	         4        	14/2	


AT24C256	    256k	   32k	    512    	64	   A1A0	         4	        15/2	


AT24C512	    512k	   64k	    512	    128	   A2A1A0	       8	        16/2	


这5款芯片与x24C01~x24C16主要的不同是，WordAddress是两个字节，器件寻址位A2/A1/A0三位或者两位，不再有页选择位。例如，下图是AT24C128、AT24C256的引脚图，只有两个硬件地址引脚A0/A1，第3脚不连接。
————————————————
https://i-blog.csdnimg.cn/blog_migrate/20c82deb985d3cf5951913aaa899dac5.jpeg#pic_center


                            版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。
                        
原文链接：https://blog.csdn.net/wanglong3713/article/details/124909042
