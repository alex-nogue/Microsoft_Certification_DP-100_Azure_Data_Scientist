IMPORTANT NOTE: This repository is about the old version of the DP-100 certification. Today's certification focus is much more on Azure Machine Learning Service instead of Studio, which is disappearing with time.

# Azure Data Scientist
This repository contains my notes for preparing the exam Microsoft [DP-100: Designing and Implementing a Data Science Solution on Azure](https://www.microsoft.com/en-us/learning/exam-dp-100.aspx).

The exam consists on 35 questions, 5 of which represent a use case. The length of the exam is 3 hours, which is largely enough.

Most of the questions of the exam are about Machine Learning Studio and its modules. The other questions are related to Azure services (such as Databricks, Data Factory, Virtual Machines, Cognitive Services etc) and some Machine Learning and Python-related questions.

Here is an overview of the study material I used and recommend.

## Machine Learning Studio
Almost every question regarding ML Studio is about its modules. I suggest going through the [list](https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/a-z-module-list) of modules, but not yet because there is a plethora of them and one can easily get lost. I recommend using this list as a reference when you have some doubts about a specific module.

First thing to do is to explore ML Studio and some of its modules. I thereby recommend following the Microsoft Learn _Learning Path_ [Publish a Machine Learning Experiment with Azure Machine Learning Studio](https://docs.microsoft.com/en-us/learn/paths/publish-experiment-with-ml-studio/), which provides an overview of how to access to ML Studio and clearly explains how to do your first Machine Learning experiment.

Once you understand how ML Studio works, one can start exploring other experiments on ML Studio and/or start doing its own experiment. It is recommended to start getting familiarized with the main modules. Here are some experiments you could follow:
- http://yacineyakoubi-blog.com/2018/12/02/azure-ml-studio/
- https://docs.microsoft.com/en-us/azure/machine-learning/studio/text-analytics-module-tutorial

Now it is time to discover other modules and try to implement them. Note that some modules are more important for this exam than others. In the file [Machine Learning Studio/Relevant_modules.md](https://github.com/alex-nogue/Microsoft_Certification_DP-100_Azure_Data_Scientist/blob/master/Machine%20Learning%20Studio/Relevant_modules.md), you will find a list of modules you __must__ be familiar with, as there is a high probability they will be asked in the exam.

For the DP-100 exam, you will sometimes need to just know the module but in some cases, you might need to know _how_ to use it and how to specify its parameters.

Optimally, one should go through the [list](https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/a-z-module-list) of modules and understand every module's purpose, but you do not need all of them for the exam. A good advice is to do dump exams and understand / experiment with the modules you will find.

## Azure Services
That was the trickiest part for me. Questions regarding Azure Services are generally _basic_ but you need a good understanding on a lot of different Azure sevices. Got questions on Azure Databricks (and Data Factory orchestration), DSVM and DLVM, Azure Notebooks, Azure HDInsight etc. The tricky thing is that questions range from "what should you use if you want to run a python notebook without any installation nor Azure subscription" (Azure Notebooks) to "which virtual machine do you need if you want to connect to a PostGRE SQL database" (DSVM with Linux) and other very specific questions. Again, a good advice is to look at the dumps and understand / experiment with the different services. 

Here are a non-exhaustie list of training recommendations:
- __Azure Fundamentals__: <br> Some of the knowledge required here can be found in the [AZ-900](https://docs.microsoft.com/en-us/learn/paths/azure-fundamentals/index) Certification. It is advised but not at all mandatory to pass that certification first (passed my DP-100 before the AZ-900).
- __Intro to Data Science in Azure__: <br> Follow the learning path [Explore AI solution development with data science services in Azure](https://docs.microsoft.com/en-us/learn/paths/explore-data-science-tools-in-azure/). Summary of the mentionned modules available in the folder with the same name in this repository.
- __Virtual Machines__: <br> Follow the first two modules of the learning path [Get started with Machine Learning with an Azure Data Science Virtual Machine](https://docs.microsoft.com/en-us/learn/paths/get-started-with-azure-dsvm/). Summary available in the folder with the same name.
- __Azure Machine Learning Services__: <br> Follow the first module of the learning path [Build AI solutions with Azure Machine Learning service](https://docs.microsoft.com/en-us/learn/paths/build-ai-solutions-with-azure-ml-service/). Summary available in the folder with the same name.
- __Azure Notebooks__: <br> Do at least one module in the learning path [Introduction to machine learning with Python and Azure Notebooks](https://docs.microsoft.com/en-us/learn/paths/intro-to-ml-with-python/). They are fun to do and you might learn about Machine Learning, which might help you with questions regarding Machine Learning (cleaning, feature engineering, evaluation etc).
- __Azure Databricks__: <br> Do at least the first module of the learning path [Extract knowledge and insights from your data with Azure Databricks](https://docs.microsoft.com/en-us/learn/paths/data-science/). The other modules are recommended but not mandatory.

## Machine Learning and Python
There are as well some questions about Machine Learning (PCA, Cross-validation, performance metrics, class imbalance, model selection etc) but they are in general not very hard. If you followed the steps described in the previous two sections, you would have learned almost everything you need for this exam.

In addition, some questions about Python and scikit-learn might also arise (around 2 or 3 questions out of 35). They are not very hard but again, I refer the reader to the dumps for Python-related questions. For example, I remember a question about which values are expected as arguments of the scikit-learn PCA function.

Finally, there are some questions about PyTorch, TensorFlow and other frameworks. Some potential questions are already covered in the previous two sections and the rest, I refer again the reader to dump exams.

## Conclusion

If you follow the steps described previously, you should be able to answer at least 75% of the questions correctly. I strongly encourage to do some dump exams before taking the exam, as they are very representative of the exam.

Finally, here are two nice articles articles about the DP-100 exam:
- [Study Guide for Microsoft Azure Data Scientist Associate Certification](https://medium.com/deep-ai/study-guide-for-microsoft-azure-data-scientist-associate-certification-dp-100-c2e4611cb071)
- [What is on the Microsoft Data Science Certification Exam](https://101.datascience.community/2019/05/20/what-is-on-the-microsoft-data-science-certification-exam/)

Thanks for reading and gluck !
