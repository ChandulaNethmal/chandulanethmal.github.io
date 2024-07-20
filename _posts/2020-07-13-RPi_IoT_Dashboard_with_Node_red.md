---
title: "IoT Dashborad with Node-Red on Raspberry Pi"
header:
  overlay_color: "#000"
  overlay_filter: "0.4"
  overlay_image: "assets/images/iot_dash/1.png"
  teaser: "assets/images/iot_dash/1.png"
  og_image: "assets/images/iot_dash/1.png"
actions:
  - label: "Blog"
    url: "/year-archive/"
categories:
  - Computer
tags:
  - Embedded
  - Electronics
toc: true
--- 

# Creating an IoT Dashboard with Node-RED on Raspberry Pi

The Internet of Things (IoT) has revolutionized how we interact with technology, providing new ways to monitor and control devices remotely. One of the most popular tools for creating IoT solutions is Node-RED, a flow-based development tool for visual programming. When combined with a Raspberry Pi, you can create powerful IoT dashboards to monitor and control your devices. In this tutorial, we'll guide you through setting up an IoT dashboard with Node-RED on a Raspberry Pi.

## Prerequisites

Before we begin, ensure you have the following:

- A Raspberry Pi with Raspbian OS installed
- Internet connection
- Basic understanding of Node-RED
- Sensors or devices to monitor (e.g., temperature sensor, humidity sensor)

## Step 1: Install Node-RED on Raspberry Pi

First, ensure your Raspberry Pi is up to date. Open the terminal and run:

```bash
sudo apt update
sudo apt upgrade
```

Next, install Node-RED:

```bash
bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)

```

After the installation is complete, enable Node-RED to start on boot:

```bash
sudo systemctl enable nodered.service
```

Start Node-RED:
```bash
node-red-start
```
You can now access Node-RED by navigating to http://<your_pi_ip_address>:1880 in your web browser.

### Step 2: Setting Up the Dashboard
Node-RED includes a dashboard module that allows you to create a web-based user interface. 
To install the dashboard nodes, run the following command in the Node-RED interface:

```
1. Click on the menu (three horizontal lines) in the top right corner.
2. Select "Manage palette".
3. Go to the "Install" tab.
4. Search for node-red-dashboard.
5. Click the install button.
```

### Step 3: Creating Your First Flow
Let's create a simple flow to display sensor data on the dashboard. We'll use a temperature sensor as an example.

1. Add an Inject Node: 
* This node will simulate sensor data.
* Drag an "Inject" node from the palette to the flow editor.
* Double-click the node to configure it.
* Set the payload type to "Number" and specify a value (e.g., 25).

2. Add a Function Node: This node will process the sensor data.
* Drag a "Function" node to the flow editor.
* Connect the output of the "Inject" node to the input of the "Function" node.
* Double-click the "Function" node and enter the following code:

```javascript
Copy code
msg.payload = {
    temperature: msg.payload
};
return msg;
```

3. Add a Dashboard Node: This node will display the data on the dashboard.

* Drag a "Gauge" node from the "dashboard" section to the flow editor.
* Connect the output of the "Function" node to the input of the "Gauge" node.
* Double-click the "Gauge" node to configure it.
* Set the Group to "Add new ui_group" and name it (e.g., "Home").
* Set the Label to "Temperature" and the value format to {{msg.payload.temperature}}.
* Deploy the Flow: Click the "Deploy" button in the top right corner to deploy your flow.

### Step 4: Accessing the Dashboard
After deploying the flow, you can access your dashboard by navigating to http://<your_pi_ip_address>:1880/ui in your web browser. You should see your temperature gauge displaying the sensor data.

### Step 5: Adding More Widgets
You can add more widgets to your dashboard to display different types of data or control devices. For example, you can add charts, buttons, and text fields to create a comprehensive IoT dashboard.

* Charts: Use the "Chart" node to visualize data over time.
* Buttons: Use the "Button" node to control devices (e.g., turn on/off a light).
* Text Fields: Use the "Text input" node to input data.

## Conclusion
Creating an IoT dashboard with Node-RED on a Raspberry Pi is a powerful way to monitor and control your IoT devices. With Node-RED's intuitive visual interface, you can quickly build and customize your dashboard to suit your needs. Whether you're a hobbyist or a professional, Node-RED provides the tools you need to create sophisticated IoT applications.

Happy hacking!

If you found this tutorial helpful, feel free to share it with others. For more guides and tutorials on IoT and Node-RED, stay tuned to our blog!

By the end of this blog post, readers should have a comprehensive understanding of how to integrate the BME280 temperature sensor with the STM32 Nucleo development board, along with insights into its potential applications in environmental sensing projects.