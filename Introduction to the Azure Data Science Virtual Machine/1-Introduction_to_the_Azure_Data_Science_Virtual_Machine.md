
# Introduction to the Azure Data Science Virtual Machine

Data scientists often use many tools to do their job. Microsoft Azure provides some preconfigured virtual machine (VM) images specifically designed for data science work. These machines come preinstalled with the most popular data science tools and frameworks. Although most of the popular data science software comes preinstalled, you can easily install any additional software you need.

Currently there are two different types of Azure DSVM: Windows DSVMs and Linux DSVMs. Azure offers a Windows Server 2016 and Windows Server 2012 version. Linux DSVMs offer Ubuntu 16.04 LTS and CentOS 7.4 versions.

You have machines created specifically for certain tasks, such as for example, deep learning. The Deep Learning DSVM comes preconfigured and preinstalled with many of these tools. Training deep learning models is computationally intense. For better model training performance select a high-speed GPU-based machine, which will significantly speed up machine model training.

In addition, the DSVM has analytic capabilities optimized for geospatial and location data. It has the ArcGIS Pro geographic information system integrated into the VM to support advanced geographic-based AI questions.

#### Experiment and evaluate on a DSVM
You can use the DSVM to learn about tools and topics such as:

- Microsoft Machine Learning Server
- SQL Server
- Microsoft Visual Studio tools
- Jupyter Notebooks
- Deep learning tools
- Popular Machine Learning toolkits
- Other new tools popular in the community

Because the DSVM can be set up quickly, you can apply it in short-term usage scenarios such as replicating published experiments, executing demonstrations, following walkthroughs in online sessions, and doing tutorials. Many sample scripts and data are provided to demonstrate how to use various Microsoft products that support data science and machine learning such as SQL Server, Machine Learning Server, Azure Machine Learning service, and Microsoft Cognitive Services.

Here an overview of what can be done in a DSVM.
<img src = "Files/diagram-1.jpg">

#### Connect to a DSVM
You can always access your VM from the Azure portal. Since we created a Windows VM, we will use the Remote Desktop Protocol (RDP) approach. If we had created a Linux DSVM, we would utilize a Secure Shell (SSH) tool.
