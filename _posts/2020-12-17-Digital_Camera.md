---
title: "Basics of Digital Camera"
header:
  overlay_color: "#000"
  overlay_filter: "0.45"
  overlay_image:  "assets/images/camera/cam1.jpeg"
  teaser: "assets/images/camera/cam4.jpg"
  og_image: "assets/images/camera/cam5.jpg"
categories:
  - Electronics
  - Tech
tags:
  - Camera
toc: true
---
Read my article on some intersting details of digital cameras including camera types, basic structure and functionality. If you are interested in photography or courious about what is happening inside a digital camera this article is for you :D. 

## Digital Camera

Digital cameras are no longer stranger items since it has become a daytoday appliance of the modern society. It is a device that captures photographs and videos using an electronic image sensor and store the images and videos digitally, rather than on film. Digital cameras are becoming more and more popular because they offer a number of advantages over traditional film cameras. One advantage is that you can see the images you have taken immediately after you have taken them, because the images are displayed on a screen on the back of the camera. This allows you to check the composition and focus of the image, and delete any that are not satisfactory.

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//camera/cam2.gif)

Another advantage is that you can easily transfer the images from the camera to a computer, where you can view, edit, and share them. Digital cameras also offer a variety of shooting modes and settings that allow you to adjust the exposure, white balance, and other aspects of the image to get the desired result.We'll discuss them later!

## Camera Types
If you ever think of buying a camera, but don't have an clear idea to choose the best camera for your purpose, let me enlighten you with some details.
Digital cameras are available in a range of sizes, from compact cameras to larger, more complex models with interchangeable lenses. They can be used for a variety of purposes, including casual photography, professional photography, and videography.

### 1. Point and Shoot Cameras

Point-and-shoot cameras, also known as compact cameras, are designed to be portable and easy to use. They are typically smaller and lighter than more advanced cameras and do not have interchangeable lenses. Point-and-shoot cameras are often preferred by amateur photographers or those who do not want to spend a lot of time adjusting settings or changing lenses. They typically have a built-in flash and a zoom lens that can cover a range of focal lengths, from wide-angle to telephoto.

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//camera/cam8.jpeg)

Some point-and-shoot cameras also have advanced features such as image stabilization, high-resolution sensors, and manual controls. These features can help produce better quality images, but may also make the camera more expensive and complex to use.

Overall, point-and-shoot cameras are a good choice for people who want a simple, portable camera for casual photography and are not interested in the more advanced features and controls of larger cameras.

	

### 2. DSLR Cameras

A DSLR (Digital Single-Lens Reflex) camera is a type of digital camera that uses a mirror system to direct light from the lens to the viewfinder, allowing the photographer to preview the composition of the photograph before taking the picture. 

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//camera/cam2.png)


DSLRs are popular among photographers because they offer a wide range of creative control, high image quality, and fast performance. Some of the key features of DSLR cameras include:

#### Interchangeable lenses:
Has a removable lens mount, allowing you to swap out lenses to achieve different focal lengths, apertures, and other effects. (Usually lenses are very expensive :D )

#### Manual controls:
Offers manual controls for exposure, white balance, focus, and other settings, giving you greater control over the final image.

#### Viewfinder:
A DSLR camera has an optical viewfinder, which allows you to preview the scene directly through the lens. This can be helpful in bright light(eg: display isn't visible due to sunlight).

#### High image quality:
They have larger image sensors. Therefore, produce high-quality images with good detail, dynamic range, and low noise, especially at low ISO settings.

DSLR cameras are available in a range of sizes and price points, from entry-level models to professional-grade cameras.
They are a popular choice among professional photographers and serious hobbyists. 




#### Mirrorless Cameras

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//camera/cam9.jpg)
	
### 3. Bridge Cameras

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//camera/cam9.jpg)

### 4. Camera Phones 

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//camera/cam9.jpg)

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//camera/cam1.gif)

<figure class="half">
	<a href="/assets/images/camera/smps_schem.jpg"><img src="/assets/images/camera/smps_schem.jpg"></a>
<figcaption> Schematic of my SMPS which I'm going to use as the example.</figcaption>
</figure>


1. Input with surge and over current protection (R1, U2):  
  R1 MOV is acting as an input surge protector by passing surge currents through itself, and U2 Fuse for fault protection within the circuit.
2. Rectification part	(D1):  
	Bridge diode converts AC to DC.
3. Common mode EMI rejection filter	(C1, CM, C2):  
	Rejects to common mode noise by CM common mode choke.
4. Driver and switching circuit (U1, C3):  
	Switching components (MOSFETs) and MOSFET driver circuit.
5. Clamping and Under-voltage protection (clamp:D2, D3 UnderV:R2, R3)
6. Input-Output Galvanic isolation(T1): 
	Isolate Input from output
7. Rectifier and Snubber circuit (Rect: D6, Snub: R8, c4)
8. Output filter ( C6, C7, L2)
9. Feedback circuit (U6, U10, R6, R7, R9, R10):
	Feedback from output to the regulator part.

I have used a simple SMPS circuit using the TNY286 switching IC which contains the MOSFET and MOSFET driver and some other safety features inside. 

## Why PCB Designing so important?

Most of the electronic circuits contain microcontrollers or logic devices which are supposed to work under reliable voltage levels. In order to achieve this reliability, not only the schematic design with correct calculations, but also the PCB designing plays a crucial role to achieve desired results.

Since this Switching mode design contains some parts with high frequency switching currents, it becomes more important to have a proper PCB design to eliminate the electromagnetic interference for the output. Let's go through the PCB design considerations described under the following topic.

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//camera/smps_2d1.jpg)

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//camera/smps_2d2.jpg)

<figcaption> Top side and Bottom side of the CAD generated view of my SMPS which I'm going to use as the example.</figcaption>

# PCB Design Consideration for SMPS

## High voltage DC trace Separation

Traces which are carrying high voltage DC in a SMPS are always adding higher amount of noise to the signal lines due to the high frequency switching. Therefore, those lines needed to be separated from signal lines. In this Buck converter design, line which directly goes from the rectifier to the transformer must be separated. It is good to separate these lines using board cutouts Changing the high voltage lines and signal lines in to different layers also another good practice.      

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//camera/2.jpg)

<figcaption> Highlighted traces are the separated power lines using board cutouts.</figcaption>

## separation of Switching Traces

SMPS contains power elements like MOSFETs and drivers which perform the major role of a converter. When they are in the switching action, they contribute a huge amount of noise to the signal lines which maintains the output regulation process. Here in this design, MOSFETs and the MOSFET driver are integrated in to a single TNY268PN IC package. You can separate feedback or other signal lines from these lines using different layers or board cutouts. The line going out from the Drain pin of the IC is the high frequency switching line and that line has been separated using physical board cutouts as you see in below.    

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//smps_pcb/1.jpg)

<figcaption> Switching output of the MOSFET drain pin is separated withn board cutout.</figcaption>

## Shorten the length and Separate Feedback Traces

Feedback lines measure voltages or currents from output part and this lines are very sensitive even for small variations. Therefore, noisy supply lines or switching lines must be separated from feedback lines. Other than that, keeping feedback traces in short lengths and avoiding unnecessary higher widths can improve the quality of output. 

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//smps_pcb/3.jpg)

<figcaption> Length of the feedback line is shorten as possible.</figcaption>

## Assign Widths for Power traces accordingly

Width of copper traces on a PCB is a crucial consideration when it comes to power supply designs or any other designs with high current drawing components. There is a maximum current which can be passed through a trace depending on the following factors.

* copper layer thickness (normally in oz)
* width of the copper trace   
* temperature of then trace

You can calculate the maximum current carrying capacity using following formula.

Area = (Thickness x  Width x 1.378)

Max_current = (k x (Temp_rise^b)) x (Area^c)                                      

Where: k,b,c are constants,

According to IPC-2221A Documents ("Conductive Material Requirements"), their values for inner layers are as follows:
k = 0.048 b = 0.44 c = 0.725

Generally, traces carrying high currents need to have a higher width than the signal carrying traces. After doing a proper calculation you can assign these widths if you know the maximum current flows of each trace. In this SMPS PCB design, I kept the high voltage input lines and high current carrying output DC lines with a higher width than feedback and other signal lines.

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//smps_pcb/4.jpg)

<figcaption> Larger widths for Traces carrying larger currents (ex:power traces) and Smaller widths for small current carrying traces (ex:signal lines).</figcaption>

## Placement of decoupling capacitors near the Inputs/outputs

Adding Filter capacitors is another important part in any power supply to eliminate high frequency noise components from switching and AC sources. Both inputs and outputs can contain filter capacitors according to the design. They must be placed closer to the input or output connectors or signal pins of an IC. In this design I have placed input filter capacitor before the driver, C3 capacitor and C7 output filter capacitor   

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//smps_pcb/filt.jpg)

<figcaption> Plcing Input filter capacitor near the driver IC and output capacitors near output port.</figcaption>


## Separation between Transformer pads and Inductor Pads

When it comes to AC-DC SMPS circuits, the separation of the input form the output is done by a transformer by providing galvanic isolation. It also reduces ripples from the switching output. An adequate distance between primary and secondary pads of this transformer must be there in the PCB to achieve better results. Therefore, it is better to have a physical PCB board cutout or a good separation as in this example PCB. 

The inductor connecting to the switching output also plays a major role from the output side of the circuit. It isn't a good practice to route any traces in between the space of inductor pads since, those traces may be affected by EMI while passing high frequency currents through the inductor.      

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//smps_pcb/trns.jpg)

<figcaption> Placing board cutout between transformer pri/sec pads and not routing signal lines between inductor pads clean.</figcaption>

## Ground planes separation

When it comes to adding copper zones (copper pouring) in to a  power supply PCBs with feedback signals, specially connecting the ground paths through copper pour , you may need to pay a good attention to avoid ground bounce. **Ground bounce** is a deviation of the ground reference value of a circuit with a bouncing kind of voltage graph due to many external factors like neighbour switching components. 

![SMPS schem]({{ site.url }}{{ site.baseurl }}/assets/images//smps_pcb/gnd_b.jpg)

<figcaption> Ground bounce illustration on an oscilloscope.</figcaption>

[Reference : More Information About Ground Bouncing](https://www.tempoautomation.com/blog/understanding-the-causes-of-ground-bounce-in-pcbs/){: .btn .btn--success}

Even if the ground connection of a SMPS is same for entire circuit in the electrical connections, it can be separated in to two paths as **Power ground** which carries higher currents with higher noise components and **Analog ground** which carries lower currents for feedbacks and regulation process. If you wish to add copper pour to ground planes it is a good practice to add separated ground planes to avoid noise from power ground to analog ground.
   
<figure class="half">
	<a href="/assets/images/smps_pcb/gnd1.jpg"><img src="/assets/images/smps_pcb/gnd1.jpg"></a>
<a href="/assets/images/smps_pcb/gnd2.jpg"><img src="/assets/images/smps_pcb/gnd2.jpg"></a>

<figcaption> Here I have placed power ground in the bottom layer and analog ground in the top layer</figcaption>

Those are the facts which I wanted to share with you regarding PCB designing of Switching Mode power supplies. You can practice these things for other applications also according to the nature of the circuit achieve better outcome.   
  
Please share your ideas and do not hesitate to ask anything related to the post on the comment section bellow.
