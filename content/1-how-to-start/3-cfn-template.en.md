---
chapter: true
date: "2020-10-10T18:28:43-05:00"
pre: <b>1.3 </b>
title: Cloud Formation Template
weight: 17
---


### Launch AWS IoT Device Simulator with CloudFormation

The [IoT Device Simulator](https://aws.amazon.com/solutions/implementations/iot-device-simulator/) allows you to simulate real world devices by creating device types and data schemas via a web interface and allowing them to connect to the AWS IoT message broker.
[AWS CloudFormation](https://aws.amazon.com/cloudformation) gives you an easy way to model a collection of related AWS and third-party resources, provision them quickly and consistently, and manage them throughout their lifecycles, by treating infrastructure as code.



![IoT Device Simulator Engine](/static/1-how-to-start/https:/d1.awsstatic.com/Solutions/Solutions%20Category%20Template%20Draft/Solution%20Architecture%20Diagrams/iot-device-simulator-architecture.fb1f3dff5cbb483483bf0caf12e905277125f4c3.png)

By clicking on Launch Stack below, you will be automatically redirected to the CloudFormation section of the AWS Console where your IoT Device Simulator stack will be launched in region *US-EAST-1*:

[![Event Engine](/static/images/LaunchStack.svg)](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/create/review?stackName=IoTDeviceSimulator&templateURL=https://s3.amazonaws.com/solutions-reference/iot-device-simulator/latest/iot-device-simulator.template)

After you have been redirected to the AWS CloudFormation console, take the following steps to launch your stack:

:::alert{type="warning"}
<p style='text-align: left;'>
The email you enter will be used to send credentials to login in IoT Device Simulator, be sure that you can access to this email.
</p>
:::

1. **Parameters** - Input Administrator Name & Email (An ID and **password will be emailed to you for the IoT Device Simulator**)
2. **Capabilities** - Check "I acknowledge that AWS CloudFormation might create IAM resources." at the bottom of the page
3. **Create Stack**
4. Wait until the stack creation is complete

The CloudFormation creation may take between **10-25 mins** to complete. In the **Outputs** section of your CloudFormation stack, you will find the Management console URL for the IoT simulator. Please **copy the URL** to use in the next section.


![CloudFormation Outputs](/static/images/consoleURL.png)