---
chapter: false
date: "2020-10-10T18:28:43-05:00"
pre: <b>2.5 </b>
title: IoT Analytics Pipeline
weight: 25
---

#### Create the IoT Analytics Pipeline

A pipeline consumes messages from a channel and enables you to process and filter the messages before storing them in a data store. To connect a channel to a data store, you create a pipeline. 

1. Navigate to the **AWS IoT Analytics** console.
2. In the left navigation pane, navigate to **Pipelines**
3. **Create** a new Pipeline:
    * **ID:** ``streampipeline``
    * **Pipeline source**: ``streamchannel``
6. Click **Next**
7. IoT Analytics will automatically parse the data coming from your channel and list the attributes from your simulated device. By default, all messages are selected.
    ![Pipeline source](/static/images/pipeline-1.png?width=720px)

8. Click **Next**
9. Under 'Pipeline activites' you can trasform the data in your pipeline, add, or remove attributes
10. Click **Add Activity** and choose **Calculate a message attribute** as the type.
     * **Attribute Name:** ``cost``
     * **Formula:** ``(sub_metering_1 + sub_metering_2 + sub_metering_3) * 1.5``
13. Test your formula by clicking **Update preview** and the *cost* attribute will appear in the message payload below.
14. Add a second activity by clicking **Add activity** and **Remove attributes from a message**
     * **Attribute Name:** _id_ and click 'Next'. The _id_ attribute is a unique identifier coming from the Device Simulator, but adds noise to the data set.
16. Click **Update preview** and the _id_ attribute will disappear from the message payload.
    ![Pipeline Transformed](/static/images/pipeline-2.png?width=720px)

17. Click 'Next'
18. **Pipeline output:** Click 'Edit' and choose 'iotastore'
19. Click **Create Pipeline** 


    :::alert{type="info"}
    <p style='text-align: left;'>
Your IoT Analytics pipeline is now set up.</p>
    :::