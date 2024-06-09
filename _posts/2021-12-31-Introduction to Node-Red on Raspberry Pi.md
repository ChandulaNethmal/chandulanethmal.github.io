---
title: "IoT with Node-RED on a Raspberry Pi"
header:
  overlay_color: "#000"
  overlay_filter: "0.4"
  overlay_image: "assets/images/nodered_intro/nodered1.jpg"
  teaser: "assets/images/nodered_intro/nodered1.jpg"
  og_image: "assets/images/nodered_intro/nodered1.jpg"
actions:
  - label: "Blog"
    url: "/year-archive/"
categories:
  - Computer
tags:
  - IoT
  - Embedded
toc: true
--- 
This blog post aims to unfold the details of DPI, exploring its definition, methods, applications, modern technologies, and the challenges it presents in the ever-evolving landscape of cybersecurity.

Beginner's Guide for IoT with Node-RED on Raspberry Pi
# Introduction
The Internet of Things (IoT) has revolutionized the way we interact with devices and the world around us. With IoT, everyday objects are connected to the internet, enabling them to send and receive data. Node-RED, a flow-based development tool, makes it easy to create IoT applications by wiring together devices, APIs, and online services.

# Node-Red
Node-RED is an open-source visual programming tool designed for flow-based development of IoT applications. It provides a browser-based flow editor that allows users to wire together devices, APIs, and online services in a visual manner. Node-RED is built on top of Node.js, which allows it to run on various platforms, including Raspberry Pi, cloud environments, and edge devices

# Node-Red on Raspberry Pi 

## Why Node-Red on an RPi?
> Visual Programming: Node-RED provides a visual programming environment that allows users to create IoT applications by simply dragging and dropping nodes, making it easy for beginners to get started with IoT development.

> Raspberry Pi GPIO Support: Node-RED has built-in support for interacting with the Raspberry Pi's GPIO pins, allowing users to easily interface with sensors, actuators, and other hardware components.

> Dashboarding: Node-RED includes a dashboard feature that allows users to create web-based dashboards for visualizing data from IoT devices, making it easy to monitor and control IoT applications from anywhere.

> Prototyping and Rapid Development: The combination of Raspberry Pi and Node-RED enables rapid prototyping and development of IoT applications, allowing developers to quickly iterate on ideas and concepts.

> Open-Source and Customizable: Node-RED is open-source and highly customizable, allowing users to extend its functionality by creating custom nodes and modules to suit their specific IoT project requirements.

## Setting Up Raspberry Pi

> Get a Raspberry Pi: Purchase a Raspberry Pi board(Here I've used a RPi 3B+ for this preoject) along with essential accessories like a microSD card and a power supply.
> Install Raspberry Pi OS: Download and install Raspberry Pi OS on the microSD card using the Raspberry Pi Imager tool.
Boot Raspberry Pi: Insert the microSD card into the Raspberry Pi, connect it to a monitor, keyboard, and mouse, and power it up.
> Installing Node-RED
Open Terminal: Launch the terminal on Raspberry Pi.

Update Raspberry Pi:
```bash
sudo apt-get update
sudo apt-get upgrade
```

Install Node-RED: Use the following command to install Node-RED:
```bash
bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)
```
![DPI schem]({{ site.url }}{{ site.baseurl }}/assets/images/nodered_intro/nodered4.png)

Configure Node-Red Settings: 
After installing, it is recommended to configure initial options and settings.
Once the intallation process is copmleted, it will automatically take you to the configuration stage and ask to set the parameters one-by-one.
In a case the installation process do not take you to the configuration stage, please run the following command to initiate the configuration:

```bash
node-red admin init
```
![DPI schem]({{ site.url }}{{ site.baseurl }}/assets/images/nodered_intro/nodered5.png)

Once the Node-RED configuration was successful as the above sceenshot. All settings will be saved on settings.js file.

After successfully completed the configuration stage, start node-red on your RPi with the following command;
```bash
node-red-start
```
![DPI schem]({{ site.url }}{{ site.baseurl }}/assets/images/nodered_intro/nodered6.png)
You will see a set of status messages on the terminal as the above screenshot while the node-red is running.


Access Node-RED: Open a web browser and navigate to http://localhost:1880 to access the Node-RED editor.
Creating Your First Flow

Drag and Drop Nodes: In the Node-RED editor, drag nodes from the palette onto the workspace. Nodes represent devices, APIs, and functions.
Connect Nodes: Click and drag from the output of one node to the input of another to create connections (flows).

Configure Nodes: Double-click on a node to configure it. For example, configure an inject node to send a message at regular intervals.
Deploy Flow: Click the "Deploy" button to deploy your flow. Your IoT application is now running!

Connecting IoT Devices
Install Additional Nodes: Node-RED supports a wide range of nodes for connecting to IoT devices. Install additional nodes from the palette manager if needed.

Configure IoT Nodes: Configure the nodes to connect to your IoT devices. For example, configure a MQTT node to connect to a MQTT broker.
Integrate IoT Data: Use Node-RED's built-in functions and flows to process and visualize the data from your IoT devices.

Example IoT Project: Temperature Monitoring

Hardware Setup: Connect a temperature sensor (e.g., DS18B20) to the Raspberry Pi GPIO pins.
Install Required Libraries: Use sudo apt-get install python3-w1thermsensor to install the required Python library for the temperature sensor.

Create Node-RED Flow: Create a flow in Node-RED to read temperature data from the sensor and display it on a dashboard.
Deploy and Test: Deploy the flow and monitor the temperature readings on the Node-RED dashboard.
Conclusion
Node-RED simplifies IoT development on Raspberry Pi, allowing beginners to create powerful IoT applications with ease. By following this guide, you can start building your IoT projects and explore the endless possibilities of IoT with Node-RED.

