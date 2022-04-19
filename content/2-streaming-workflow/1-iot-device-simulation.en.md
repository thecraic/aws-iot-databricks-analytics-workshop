---
chapter: false
date: "2020-10-10T18:28:43-05:00"
pre: <b>2.1 </b>
title: IoT Device Simulation
weight: 21
---

#### IoT Device Simulation

Please login to the IoT Device Simulator Management console (URL link copied from the [earlier step](/1-how-to-start/3-cfn-template) with the provided credentials.

Credentials for the Device Simulator will be mailed to the **email address** provided during CloudFormation stack creation. You will be asked to change the default password, use your **user id** (in the email) and assign a new password.


#### Create the Simulated Device

You are going to create a virtual device fleet to simulate data from wind turbines. 

You can get more information about the data simulated here [TODO INFO ABOUT DATA][link](https://databricks.com).

First we will create some "healthy" devices.

1. On the menu, choose -> **Device Types** -> Click **Add Device Type**
    * **Device Type Name:** ``healthy-turbine`` 
    * **Data Topic:** ``wind-farm/site-1/turbines`` 
    * **Message Payload:** Click **Add Attribute** and add the following attributes:  
        
    |     Attribute Name    |            Data Type           | Float Precision |  Minimum Value |  Maximum Value |
    |:---------------------:|:------------------------------:|:---------------:|:---------------------:|:---------------------:|
    |     ID                |              Integer           |                 |                     1 |                   500 |
    |     AN3               |              Float             |               2 |                     0 |                     9 |
    |     AN4               |              Float             |               2 |                     0 |                    11 |
    |     AN5               |              Float             |               2 |                     0 |                    15 |
    |     AN6               |              Float             |               2 |                     0 |                    16 |
    |     AN7               |              Float             |               2 |                     0 |                    17 |
    |     AN8               |              Float             |               2 |                     0 |                    30 |
    |     AN9               |              Float             |               2 |                     0 |                    32 |
    |     AN10              |              Float             |               2 |                     0 |                    15 |
    |     SPEED             |              Float             |               2 |                     1 |                     5 |
    |     timestamp         | UTC Timestamp (Choose Default) |                 |                       |                       |


Add some additional string values to the payload to help readabliity:

    |     Attribute Name    |            Data Type           |  Static Value         |  
    |:---------------------:|:------------------------------:|:---------------------:|
    |     TORQUE            |              String           |     ''                 |
    |     STATUS            |              String           |     HEALTHY            |




3. Once the sample message payload shows all the attributes above, click **Save**
4. Navigate to **Modules** -> **Widgets** -> **Add Widget** 
    * Select 'smart-home' as the **Device Type**
    * **Number of widgets:** 1 -> **Submit**


We have now created a simulated smart home device which is collecting power usage data and publishing that data to AWS IoT Core on the 'smarthome/house1/energy/appliances' topic.

#### Verify that the data is being published to AWS IoT

**Note**: *You will use the AWS console for the remainder of the workshop. Sign-in to the [AWS console](https://aws.amazon.com/console).*


We will verify that the smart home device is configured and publishing data to the correct topic.


1. From the AWS console, choose the **IoT Core** service

2. Navigate to **Test** (On the left pane) 

3. Under **Subscription** input the following:
    * **Subscription topic:** ``smarthome/house1/energy/appliances``
    * Click **Subscribe to topic**

![Subscribe to Topic](/static/images/mqtt-client.png?width=900)


After a few seconds, you should see your simulated devices' data that is published on the 'smarthome/house1/energy/appliances' MQTT topic. 

![Topic Subscription](/static/images/test.png?width=700)

:::alert{type="info"}
<p style='text-align: left;'>
Your IoT smart home data are being simulated</p>
:::