---
chapter: false
date: "2020-10-10T18:28:43-05:00"
pre: <b>5.1 </b>
title: Jupyter Notebook
weight: 51
---

#### Create Jupyter Notebooks using Amazon Sagemaker 

An Amazon SageMaker notebook instance is a machine learning (ML) compute instance running the Jupyter Notebook App. SageMaker manages creating the instance and related resources. Use Jupyter notebooks in your notebook instance to prepare and process data, write code to train models, deploy models to SageMaker hosting, and test or validate your models.

With respect to code, it can be thought of as a web-based IDE that executes code on the server it is running on instead of locally.
There are two main types of “cells” in a notebook: code cells, and “markdown” cells with explanatory text. You will be running the code cells. These are distinguished by having “In” next to them in the left margin next to the cell, and a greyish background. Markdown cells lack “In” and have a white background. For further information about SageMaker Notebooks, please visit: [Use Amazon SageMaker Notebook Instances](https://docs.aws.amazon.com/sagemaker/latest/dg/nbi.html)  

1. Navigate to the **AWS IoT Analytics** console.
2. Select **Notebooks** from the left-hand navigation pane.
3. Click **Create** to begin configuring a new Notebook.
4. Click **Blank Notebook** and input the following: 
    * **Name**: ``smarthome_notebook``
    * **Select data set sources**: 'streamdataset'
5. Create a Notebook instance: 
    * **Name**: ``IoTAWorkshopSagemaker``.
    * **Instance type**: 'ml.t2.medium'.
    * Create a new **Role** ``iot-sagemaker-role``.
    * Click on 'Create Notebook instance'.
    * Wait until the instance is ready.
6. **Create Notebook**
7. Click on **IoTAWorkshopSagemaker**
    * Choose **IoT Analytics** in the drop down menu
    * Next to smarthome_notebook.ipynb, choose **Open in Jupyter**
8. If you get a message that says "Kernel not found". Click **Continue Without Kernel**
9. Download the following Jupyter Notebook: <a target="_blank_" href="/notebook/SmartHomeNotebook.ipynb" download>SmartHomeNotebook</a>.
10. In the Jupyter Notebook console, click **File** -> **Open**
11. Choose **Upload** and select the SmartHomeNotebook.ipynb notebook downloaded in step 9.
12. Click on the SmartHomeNotebook.ipynb to be taken back to the Jupyter Notebook.
13. In the menu **Kernel**, choose **Change kernel** and select **conda_mxnet_p36**.
14. You need to give permissions to the 'iot-sagemaker-role' to access the ‘Household Power Consumption‘ data set available in Amazon S3, which is similar to the data set simulated in previous sections. 
    * Navigate to the **IAM console**.
    * Navigate to **Roles** (On the left pane)
    * **Search and select** the Sagemaker role created in step 5: ``iot-sagemaker-role``.
    * On the Permissions tab, click on **Attach policies**.
    * Search and **Attach policy** ``AmazonS3FullAccess``.
15. Returning to the Jupyter notebook in SageMaker, you should see some pre-filled Python code steps in the Jupyter notebook.
16. Click **Run** for each cell. Follow the documentation presented in the Notebook. The Notebook includes information about how the machine learning process works for each step.
17. Run through all the steps in the SmartHomeNotebook to understand how the machine learning training process works with Jupyter Notebooks. _**Note**: Wait until the asterisk * disappears after running each cell. If you click 'Run' before the previous step is completed, this could cause some code to fail to complete and the algorithm will fail._