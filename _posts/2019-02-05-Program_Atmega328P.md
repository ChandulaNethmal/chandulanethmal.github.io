---
title: "Program Atmega328P microcontroller via Arduino board as an ISP Programmer"
header:
  teaser: "/assets/images/atmega328isp/1.jpg"
  og_image: "/assets/images/atmega328isp/1.jpg"
categories:
  - Electronic
  - Embedded
  - Programming
tags:
  - Arduino
  - Microcontroller
  - AVR
toc: true
---
Most of electronics projects are related with microcontrollers and programming. Among these projects many of them are programmed using Arduino due to the user friendliness of Arduino coding. Even a beginner can quickly learn to code Arduino for a deeper level. But some of the projects like university or college projects cannot have an Arduino board within the project due to limitations from the academic staffs. For that kind of cases we can still use Arduino programming to program Atmega 328PU IC microcontroller which is the same controller IC within the Arduino UNO board.

![Unsplash image 9]({{ site.url }}{{ site.baseurl }}/assets/images/atmega328isp/1.jpg)

Here we are using an Arduino UNO board to program the Atmega 328PU chip. UNO board is acting as an ISP (In System Programming) programmer to program the chip on a bread board or on a PCB. This method allows to program a microcontroller while it is installed in a system.


## Uploading ISP sketch to Arduino
Open Arduino IDE and go to Examples => ArduinoISP and there you can see the  ArduinoISP example sketch.
 Open this sketch in a new tab and upload it to the Arduino board which you are going to use as the ISP programmer.

![Unsplash image 9]({{ site.url }}{{ site.baseurl }}/assets/images/atmega328isp/2.png)

## Setting up connections
   After a successful uploading, connect your ATMega328p chip to several other components as following image. Here I have used an Arduino Uno board as the programmer. But you can use any other Arduino board for this. In that case pin connecting diagram will be differ according to the chip of the Arduino board.

There are two methods for the next step.
* The ATMega chip on the programmer Arduino board should be removed from the board.
![Unsplash image 9]({{ site.url }}{{ site.baseurl }}/assets/images/atmega328isp/3.png)

* But if you have an Arduino clone board with a non-removable surface mounted Atmega chip, you need to connect the reset pin of the programmer Arduino board to the ground through a capacitor (here I used a 10uF one) as the image shown bellow.

![Unsplash image 9]({{ site.url }}{{ site.baseurl }}/assets/images/atmega328isp/4.png)

## Uploading Arduino Bootloader 

If your target ATMEGA 328P does not contain the Arduino bootloader, you need to upload it as follows. (If your 328P chip already contain the bootloader, you can skip this step).
     Go to Tools=> programmer and then select "Arduino as ISP"

![Unsplash image 9]({{ site.url }}{{ site.baseurl }}/assets/images/atmega328isp/5.png)

Now you already have an Atmega 328 chip with the boot loader. Next step is to program this chip using  an Arduino board as an ISP programmer.

Open the Arduino sketch which you want to upload. Connect the chip in the same configuration in above figures which you used to upload the bootloader. You need to upload ArduinoISP to the Arduino board and select programmer as "Arduino as ISP" from tools tab.
Then go to the sketch tab and click on "Upload Using Programmer". It will upload the sketch to the chip on the breadboard.

![Unsplash image 9]({{ site.url }}{{ site.baseurl }}/assets/images/atmega328isp/7.png)
