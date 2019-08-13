
# Introduction to Azure Machine Learning service 

To set up a projet on Azure ML service, you start your model development on your local computer with the Python tools and open-source frameworks of your choice. Then use the Azure Machine Learning service via Python modules to speed up model training and evaluation, hyperparameter tuning, and deployment, complete with a callable REST API.

## Azure Machine Learning Service within a data science process
<img src="Files/3-ml-service-framework.png">

### Environment setup
You start by creating a workspace, which is a place in Azure for you to store machine learning work. You can create a workspace in the Azure portal or from within Python code. An experiment object is created within the workspace to store information about runs for the models that you train and test. You can have multiple experiment objects in a workspace.

The Azure Machine Learning service allows you to interact with a workspace by using your preferred integrated development environment (IDE), such as a local Jupyter notebook, PyCharm, or a notebook in Azure Notebooks (a cloud version of Jupyter Notebook).

### Data preparation
Before you can train a model, you must explore and analyze the source data to determine its quality and to select data for model features. You can use whatever Python modules you like for data preparation, including Pandas or the Azure Machine Learning Data Preparation SDK called Azureml.dataprep.

### Experimentation
Experimentation is the iterative process of model training and testing. Open-source packages like Scikit-learn, TensorFlow, and others are supported.

After building a model, you can train it locally or on a remote computer.

A key feature of the Azure Machine Learning service is the ability to run model training and evaluation in Azure containers. It's simple to monitor remote model execution and retrieve output by using the Azureml package. You also must create and configure a compute target object, which is used to provision computing resource.

After you have the model you want to use in production, you register the model in the workspace.

### Deployment
After ensuring that the model runs correctly in the local environment and is performing at the accuracy level that you want, you can deploy the model.

You will create a Docker image and then deploy it to Azure Container Instances. Note: Other target environments are available, including Azure Kubernetes Service (AKS), Azure IoT Edge, and a field programmable gate array (FPGA). For the deployment, you need the following files:

- The score scripts file is needed to decide how to run the model.
- The environment file is needed to specify package dependencies, which are important when using open-source packages.
- The configuration file is needed to request an appropriate amount of resources for the container.

### What is a Workspace?
A workspace is the top-level resource for the Azure Machine Learning service. It serves as a hub for building and deploying models. You can create a workspace in the Azure portal, or you can create and access it by using Python on an IDE of your choice. All models must be registered in the workspace for future use. Together with the scoring scripts, you create an image for deployment.

### What is a Datastore?
A datastore is an abstraction over an Azure Storage account. Each workspace has a registered, default datastore that you can use right away, but you can register other Azure Blob or File storage containers as a datastore.

### What is a Compute target?
A compute target is the compute resource to run a training script or to host service deployment. It's attached to a workspace. Other than the local machine, users of the workspace share compute targets.

## Train a model using the Experimentation Service
Let's create a new workspace and experiment. You can quickly set up a workspace by using the Azure portal or via Python code. 

To do it via the Azure portal, add the Azure ML services workspace ressource on your Azure portal, create a workspace and clone the project "Get Started in Azure Notebooks" to run a sample experiment in the workspace you just created.

In this example, you'll learn how to use Azure Machine Learning for experimentation. The concepts you'll learn about are workspace, experiment and run.

__Run__ is a an execution of Python code that does a machine learning task, such as training a model. Within a run you can log metrics and upload results to Azure cloud, to keep track of your experimentation.

In this example, the run is a simple notebook cell, but in subsequent tutorials you can learn how to submit different kinds of runs - hyperparameter tuning, automated machine learning, distributed training - to scalable cloud compute.

__Experiment__ is a collection of related runs. For example, if you train different models to solve the same problem, you can group the training runs under the same experiment, and later compare their results.

__Workspace__ is an Azure resource that contains your experiments, models, deployments and cloud compute resources.

To illustrate these concepts, we use a simple example of Monte Carlo simulation to estimate pi. Follow the steps of the file _01.run-experiment_ to create this experiment in your workspace.
