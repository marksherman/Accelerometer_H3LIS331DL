## H3LIS100DL for Arduino Library
[The original project: Seeed Studio's H3LIS331DL](https://github.com/Seeed-Studio/Accelerometer_H3LIS331DL)

This fork exists because the H3LIS100DL differs slightly from the 331DL, as used by Seeed. This fork contains the adjustments to work on the sibling chip. 

Using this library you can connect to a 100DL acceleromter in *nearly* exactly the same way as the original library.

## Differences
* 100DL is 8-bit readout, where 331DL is 16-bit, but that doesn't matter because the high byte reads as zero anyway. 
* 100DL is full-scale 100G, where 331DL is adjustable 100/200/400, but the control register bits where scale is selected are disabled on the 100DL so writing to them is harmless, and the chip will always return full-scale 100G.
* 100DL is capable of measuring accelerations with output data rates from 0.5 Hz to 400 Hz, where 331DL is capable of 0.5 Hz to 1kHz, but both use the same mode values, so the 100DL simply doesn't support mode 3, but modes 0,1,2 work the same.

## Similarities
* I2C address is the same (yay!)
* 

The H3LIS100DL is a low power high performance 3-axis linear accelerometer belonging to the “nano” family, with digital I2C serial interface standard output. The device features ultra low power operational modes that allow advanced power saving and smart sleep to wake-up functions. The H3LIS331DL is full scales ±100g and it is capable of measuring accelerations with output data rates from 0.5 Hz to 400 Hz.  For more information, you can visit our wiki [grove_3_Axis_Digital_Accelerometer_H3LIS331DL][1] and [xadow_3_Axis_Digital_Accelerometer_H3LIS331DL][2] 

### Features
+ Ultra low power mode consumption down to 10 µA
+ ±100g/±200g/±400gdynamically selectable full scale
+ 16-bit data output
+ 10000g high shock survivability


### Applications
+ Shock detection
+ Impact recognition and logging
+ Concussion detection 

### Getting Started
please follow the example sketch(**H3LIS331DL_AdjVal** and **H3LIS331DL_Demo**). Have fun!


----

This software is written by lawliet zou (![](http://www.seeedstudio.com/wiki/images/f/f8/Email-lawliet.zou.jpg)) for [Seeed Technology Inc.](http://www.seeed.cc) and is licensed under [The MIT License](http://opensource.org/licenses/mit-license.php). Check License.txt/LICENSE for the details of MIT license.<br>

Contributing to this software is warmly welcomed. You can do this basically by<br>
[forking](https://help.github.com/articles/fork-a-repo), committing modifications and then [pulling requests](https://help.github.com/articles/using-pull-requests) (follow the links above<br>
for operating guide). Adding change log and your contact into file header is encouraged.<br>
Thanks for your contribution.

Seeed is a hardware innovation platform for makers to grow inspirations into differentiating products. By working closely with technology providers of all scale, Seeed provides accessible technologies with quality, speed and supply chain knowledge. When prototypes are ready to iterate, Seeed helps productize 1 to 1,000 pcs using in-house engineering, supply chain management and agile manufacture forces. Seeed also team up with incubators, Chinese tech ecosystem, investors and distribution channels to portal Maker startups beyond.

[1]: http://www.seeedstudio.com/wiki/Grove_-_3-Axis_Digital_Accelerometer(%C2%B1400g)
[2]: http://www.seeedstudio.com/wiki/Xadow-_3-Axis_Digital_Accelerometer(%C2%B1400g)

[![Analytics](https://ga-beacon.appspot.com/UA-46589105-3/Accelerometer_H3LIS331DL)](https://github.com/igrigorik/ga-beacon)
