---
title: "Rocker Bogie Suspension System"
date: "2019-05-11"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image:  "https://4.bp.blogspot.com/-GBh99YjvTqM/XNcFLKFhn6I/AAAAAAAADUY/yXkiTuqrsVwABuC6DvuUlBs6DmUKqreAwCLcBGAs/s400/maxresdefault.jpg" 
  teaser: "https://4.bp.blogspot.com/-GBh99YjvTqM/XNcFLKFhn6I/AAAAAAAADUY/yXkiTuqrsVwABuC6DvuUlBs6DmUKqreAwCLcBGAs/s400/maxresdefault.jpg" 
categories:
  - Robotics
  - Electronics
  - Automation
tags:
  - Robotics
  - Rocker Bogie
  - Rover
  - Configuration
toc: true

---
## What is Rocker Bogie Suspension?
When we are designing a robot, understanding the operating environment is a must. For a land mobile robot, we need to consider about the terrain and obstacles it needs to overcome.

Mechanical design of the robot is highly dependent on this details. A suspension is the system which allows the relative motion between wheels and the body and connect them together.  Rocker Bogie is a special suspension mechanism designed for land mobile platforms. Expectation of this design is providing a maximum stability to the platform in all kinds of difficult terrains. A surface with rough terrain including rocks, pits, sand or even stairs can be overcome by a mobile platform with the use of this mechanism. 

## Origin of Rocker Bogie
Rocker Bogie is a suspension system developed by NASA for its Mars Rover missions in 1988. First it was introduced for the Sojourner Mars Rover which landed on Mars on 1997 and after that for Spirit and Opportunity Rovers belonged to MER (Mars Exploration Rover) project in 2003 and also for Curiosity Rover on MSL (Mars Science Laboratory)  project in 2012.   Not only that, this system is already added to the Mars 2020 rover of NASA which is planed to launch in 2021.

<iframe width="560" height="315" src="https://4.bp.blogspot.com/-GBh99YjvTqM/XNcFLKFhn6I/AAAAAAAADUY/yXkiTuqrsVwABuC6DvuUlBs6DmUKqreAwCLcBGAs/s400/maxresdefault.jpg" frameborder="0" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://1.bp.blogspot.com/-faImswuAhgI/XNALeBf022I/AAAAAAAADPQ/4kzA2EIF3OUZWarm53gycPV2b7jLsGNBACLcBGAs/s400/3792_PIA15278_3rovers-lo_D2011_1215_D515-full2.jpg" frameborder="0" allowfullscreen></iframe>
## Rocker Bogie Mechanism
When we hear the name 'Suspension Mechanism' ,  at least one spring or shock-absorber will come to our mind. But unlike many other suspension systems we are familiar with, this one has no above hardware parts. Rocker bogie system has two main parts as shown in the following figure.

<iframe width="560" height="315" src="https://1.bp.blogspot.com/-SmZSxzF8s_s/XNQ3xHhoFsI/AAAAAAAADSI/QkElZX-lINcD5dRJqBFuTbgt9BZpALi7wCLcBGAs/s400/Links.png" frameborder="0" allowfullscreen></iframe>
This consists of two solid links and 3 wheels for both sides of the center platform of the robot. The larger link 1 with only one wheel and two joints is called as the 'Rocker' and it is the forward part of one leg.  The rocker dedicated for  the rocking aspect of the platform.

The second link consists with two drive wheels at both ends called the 'Bogie' which is the rear part of the suspension design. Bogie part helps to maintain a proper load distribution over the terrain in order to protect the stability. This type of bogie parts can be seen in some heavy land vehicles such as trains, trucks and army tanks.

One leg for our platform is made connecting Rocker and bogie links together by a pivot at one end of the rocker and middle of the bogie. A mobile platform consists of two such legs as following figure.

<iframe width="560" height="315" src="https://2.bp.blogspot.com/-EVqf0Ux4FD4/XNVz6YJ1nYI/AAAAAAAADSo/YjscggYRCokAVMc2ehQlqKQ8gM7L_XrGwCLcBGAs/s400/Link2.png" frameborder="0" allowfullscreen></iframe>

## Differential to achieve Stability
One main feature of this mechanism is, allowing individual link to move relatively, giving maximum stability to the body of the robot. Therefore each leg is connected to the chassis from rocker parts. Each rocker has an axle connected to a differential at the middle of the platform. This differential is a small arrangement of bevel gears with orthogonal rotation conversion, in order to maintain an average pitch angle of each rocker to the body part.
<iframe width="560" height="315" src="https://4.bp.blogspot.com/-KtRQr6TzBTs/XNWQZfgc6oI/AAAAAAAADS4/JQgMor3a-vgNJpEDD6a8qB1gSHg2tgPuwCLcBGAs/s400/diff1.png" frameborder="0" allowfullscreen></iframe>

As you can see in the above figure, the center gear is connected to the body of the robot while other two side axles are connected to rockers. When the left rocker goes up on an obstacle, right rocker goes down because of the differential while giving an average pitch angle to the body. This will help to achieve a desirable stable position even the platform goes on a rocky terrain. 

Tilting ability of the rockers is the main feature of the system. However, the stability against tilting is limited by the height of the Center of Gravity of the platform. Normally, a platform with this suspension system is capable of climbing over obstacles with approximately two times high as the diameter of a wheel.  


## Steering of the Robot
Steering capability is a key point for any type of robot. There are two methods to achieve that for this rocker bogie structure.

## Skid Steering 
This is one of the most commonly seen steering mechanism in robots. There is no need of additional  motors for steering other than six wheels driving motors. If we rotate all six wheels in  anti-clockwise robot will turn in the left direction. In another words, if we rotate left wheels to backwards and right wheels to forward direction we can achieve the left turning. 
Similarly, the right turn can be achieved by rotating all six wheels in clockwise direction.
<iframe width="560" height="315" src="https://4.bp.blogspot.com/-UghzmvwT2Po/XNb1nlnyUvI/AAAAAAAADTk/D5H6qRbJMuwqLwSNh-y3yfo-27Luc3QdQCLcBGAs/s640/steer3.png" frameborder="0" allowfullscreen></iframe>
## Using Steering Motors
In this method we are using additional servo/stepper motors to turn wheels. Two steering motors for front wheels and two Steering motors for rear wheels. Middle two wheels only have their driving motors. If we need to turn in to left side, turn front and rear wheels using steering servos as following figure . 
<iframe width="560" height="315" src="https://4.bp.blogspot.com/-o8sxH5o-EfY/XNb1xdXhknI/AAAAAAAADTo/cpBhXqM4Mag1SA5l4q1SnfINRffOqMXhgCLcBGAs/s640/steer2.png" frameborder="0" allowfullscreen></iframe>

Then rotate all six wheels or two front and two rear wheels in clockwise direction in order to turn the whole platform in the left direction. In the similar way, we can achieve right steering also as following figure..
<iframe width="560" height="315" src="https://3.bp.blogspot.com/-dUT3uS4YaDw/XNcCNFzLSUI/AAAAAAAADUI/a6eOB4hHYJQmcVSshoTBHgew-pPILs9tQCLcBGAs/s640/steer4.png" frameborder="0" allowfullscreen></iframe>