
# Choose the Data Science service in Azure you need 

## Machine Learning options on Azure

Here are some of the services available on Azure:
- __Azure Machine Learning service__: A managed cloud service for Machine Learning.	Used to train, deploy, and manage models in Azure using Python, Azure CLI, and Azure portal.
- __Azure Machine Learning Studio__: A drag-and-drop visual interface for Machine Learning.	Used to build, experiment, and deploy models using preconfigured algorithms. Ideal for learning about Machine Learning.
- __Azure Databricks__:	Apache Spark–based analytics platform with an integrated notebook interface that seamlessly integrates with Azure Active Directory (Azure AD) and data services. Used to build and deploy models and data workflows with big data.
- __Azure Data Science Virtual Machine__: A virtual machine with preinstalled data science tools. Used to develop machine learning solutions in a preconfigured data science environment.
- __SQL Server Machine Learning Services__: Integrated with Microsoft SQL Server, this scalable analytics server supports the Python and R language. Used to build and develop models in an on-premises SQL server that scales to match the SQL Server engine. Microsoft Machine Learning Server is also available as a cluster type in Azure HDInsight.

### Machine Learning Service
The Azure Machine Learning service supports data science pipeline integration with Azure. It allows you to scale up and automate:

- Model management
- Model training
- Model selection
- Hyper-parameter tuning
- Feature selection
- Model evaluation

The Azure Machine Learning service also enables you to more easily deploy your trained models to Azure containers where you can use them. The key advantage of this service is that it makes it easier for your data science project to utilize containerization and automation, resulting in better results in less time.

The Azure Machine Learning service supports open-source technologies, which include a plethora of packages for practicing machine learning via Python. Azure Machine Learning service includes common data science tools as extensions. If you're wondering why this would be beneficial for a data scientist, this technology permits the use of at-scale data because it can run on a local machine, then be scaled up to the cloud when needed.

<img src="Files/8-aml-framework.png">

Once a model has been built and trained, you can create an image of the model and all components needed to use the model. An image contains:

- The model.
- A scoring script or application which passes input to the model and returns the output of the model.
- The required dependencies (for example, the Python scripts or packages needed by the model or scoring script).

Images can be packaged either as Docker images, or field programmable gate array (FPGA) images.

Azure Machine Learning service can deploy images to either a web service (running in Azure Container Instance, FPGA, or Azure Kubernetes Services), or an IoT module (using IoT Edge). Once deployed, developers can invoke models from their applications to process data and return results.

More here: https://docs.microsoft.com/en-us/azure/machine-learning/service/overview-what-is-azure-ml

### Azure Machine Learning Studio
Azure Machine Learning Studio gives you an interactive, visual workspace that you can use to easily and quickly build, test, and deploy models using pre-built machine learning algorithms. Machine Learning Studio publishes models as web services that can easily be consumed by custom apps or BI tools such as Excel. No programming is required - you construct your machine learning model by connecting datasets and analysis modules on an interactive canvas, and then deploy it with a couple clicks.

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio/

### Azure Databricks
Azure Databricks is a secure, all-in-one data science team collaboration platform. It includes a powerful notebook interface, job scheduling, Azure Active Directory integration, granular security control, and seamless Azure integration. Azure Databricks has a GUI-based cloud portal that makes it even easier to use the Spark big data platform.
Azure Databricks features include, but are not limited to:

- Azure Databricks notebooks, which support SQL, Python, R, Scala, and Java
- Job scheduler
- Local built-in Blob Storage
- Seamless, secure access to Azure data services such as Azure Blob Storage, Azure SQL database, Azure SQL Datawarehouse, and Azure CosmosDB
- Graphical UI to quickly spin up and scale Spark clusters
- Proprietary Spark optimizations

An advanced job scheduler allows you to schedule notebooks to run whenever you want. If the cluster isn't running, the job scheduler will create it automatically and delete it at the end of the job.

Assets such as notebooks can be shared and worked on collaboratively. Best of all, you don't need to worry about the complexities of configuring Spark clusters. The Azure Databricks GUI provides an easy-to-use interface to create and edit your cluster, and even set automatic turn-off for clusters after a period of disuse. You can delete clusters without losing any data or notebooks, so there's no need to keep clusters running if you don't need them.

More here: https://docs.microsoft.com/en-us/azure/azure-databricks/what-is-azure-databricks

### Azure Data Science Virtual Machine
Built specifically for data science, Azure Data Science Virtual Machines (DSVMs) are preconfigured virtual machines you create in Azure that have many popular machine learning tools preinstalled. It provides data scientists a simple way to begin and iterate through the modeling process.

More here: https://docs.microsoft.com/en-gb/azure/machine-learning/data-science-virtual-machine/overview

### SQL Server Machine Learning Services
SQL Server Machine Learning Services runs on the SQL Server on-premises platform, and supports scale up and high performance of Python and R code. With it, you can work with SQL Server data in place. You also get all the SQL Server features including tighter security, excellent performance, the ability to schedule model training with the SQL Agent service, and persistence of models to database tables. In addition, you can encapsulate Python and R code in stored procedures, and they can interoperate with T-SQL so you can have the high performance of T-SQL with the advanced Machine Learning features or R and Python.

Along with core Python and R tools, SQL Server Machine Learning Service includes a set of components for data scientists.

- Python components and packages for data manipulation, transformation, visualization, and analysis.
- R packages such as RevoScaleR, MicrosoftML (R), opalR, and sqlRUtils to perform data science tasks in the R language.

### Spark on HDInsight
Azure HDInsight is an Azure platform as a service (PaaS) Apache Hadoop offering. It is based on the Hortonworks distribution of Hadoop. When you provision an HDInsight cluster, you specify which type of a Hadoop platform you want.

HDInsight provides several benefits.

- You can quickly spin up big data clusters on demand, scale them up or down based on your usage needs, and pay only for what you use.
- Extract, transform, and load your big data clusters on demand with Hadoop MapReduce and Apache Spark.
- Meet industry and government compliance standards and protect your enterprise data assets using an Azure Virtual Network, encryption, and integration with Azure Active Directory.
- Integrate seamlessly with other Azure services, including Data Factory and Data Lake Storage, for building comprehensive analytics pipelines.
- Use your preferred productivity tools, including Visual Studio, Eclipse, IntelliJ, Jupyter, and Zeppelin.
- Write code in familiar languages such as Scala, Python, R, JavaScript, and .NET.

#### What is Spark?
Apache Spark is an open-source big-data platform that uses a scale-out approach. This is where multiple machines working together to process data. Unlike Hadoop, Spark works in-memory as much as possible. This results in much faster processing than Hadoop.

HDInsight Spark is an implementation of Apache Spark on Azure HDInsight. It supports massive scale for data querying, wrangling, and machine learning model training. A cluster has a master server that controls the other servers in the cluster. By splitting the work among multiple machines, performance is greatly enhanced. It shares the data source across all the servers by storing the data into Azure Blob Storage.

Data scientists who are comfortable working with the native Spark interface and want complete custom control of the data science process should consider using HDInsight Spark. For the data science team looking for an all-inclusive, user friendly, secure, collaborative, Spark-based environment, Azure Databricks may be a better solution.

HDInsight Spark has a version that uses R Server as a processing front end. The R Server proprietary model training libraries scale out machine learning over the Spark cluster for big data model training.

Finally, HDInsight Spark clusters include Apache Zeppelin notebooks that you can use to run Apache Spark jobs.

## Azure Cognitive Services
Azure Cognitive Services is a set of APIs that enable you to build apps that use natural methods of communication. These APIs allow your apps to see, hear, speak, understand, and interpret user needs with just a few lines of code. Easily add intelligent features to your apps, such as:

- Emotion and sentiment detection
- Vision and speech recognition
- Language understanding (LUIS)
- Knowledge and search

Use Cognitive Services to develop apps across devices and platforms. The APIs keep improving, and are easy to set up.

More here: https://docs.microsoft.com/en-us/azure/cognitive-services/welcome


```python

```
