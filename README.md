# Austin Big Data AI, NLP Tutorial Part I


**Date: Thursday, July 9, 2020, 7:00 PM to 8:00 PM CDT**


This tutorial is a gentle introduction to Natural Language Processing (NLP) for those who have not used NLP methods and techniques before or have some minimal experience with them. 


## Part I
We will start with a brief introduction to NLP concepts and terminology and then, we will walk you through some of the text preprocessing steps to prepare the provided dataset for further NLP modeling. If time permits, we will also show you a complete implementation of a sentiment analysis model. 


## Setup Instructions: Please Read Before the Tutorial!

**Please do the download and install of Jupyter Notebook, as well as the packages listed in the environment.yml file as described below before coming to the tutorial!**
**We will NOT have time to setup or handle technical problems that might come up due to downloads during 
the tutorial due to the very limited amount of time we will have.**


We'll be using [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html) and [NLTK](https://www.nltk.org/data.html), as well as some other open source libraries. 


### Installation Steps


*Please note: if you are familiar with creating development environments on your machine, it is generally recommended to install packages in a virtual environment to avoid modifying system state.*

There is an environment.yml file included in the github repo that will create a conda environment with all dependecies for the tutorial.  This is the easiest way to get all you need to run the jupyter notebooks included with the tutorial. 

* You will need to clone the repository for this tutorial from github using your command line:
    ```
    git clone 
    git@github.com:ftarlaci/bigdata_ai_nlp_tutorial.git
    ```

* If you do not have anaconda installed, you can download it here: [download Anaconda](https://www.anaconda.com/products/individual)

* Once you have installed Anaconda, in a shell, navigate to the cloned directory for the tutorial, and run the following line to create an environment with all requirements needed:

    ```
    conda env create -f environment.yml
    ```
 
 
* Activate the environment and open the notebook (a browser window should open):
    
    ```
    conda activate nlp_tutorial
    jupyter notebook
    ```
    
    
 This command will launch the Jupyter Notebook in your browser. 

### Testing correct installation
If you have installed all the required packages, please open and run the `test_installations.ipynb`. If you don't get any errors, that means you have installed the required libraries correctly and will be able to run the notebooks during the tutorial. 


# Part II

Date: Thursday, July 17, 2020, 7:00 PM to 8:00 PM CDT

In this second part of our tutorial, we will introduce a new NLP library, named **Spark NLP**, and explain some of the concepts that shape the most recent and advanced NLP methods that are widely used today. More specifically, we will breifly talk about what **pretrained models** and **transfer learning** mean, as well as how these concepts are integrated into Spark NLP. 

We will also walk you through how we can do sentiment analysis with this library. By the end of this session, you will have a better understanding of the more recent techniques and libraries used in NLP. 


Spark NLP is a self-contained library. It does not require you to download any other NLP library. Spark NLP is built on top of [Apache Spark](https://spark.apache.org/docs/latest/), which is a general-purpose in-memory distributed data processing engine, which makes Spark NLP a highly efficient NLP tool. If you would like to learn more about Spark NLP, please read [this](https://towardsdatascience.com/introduction-to-spark-nlp-foundations-and-basic-components-part-i-c83b7629ed59) and [this](https://medium.com/spark-nlp/introduction-to-spark-nlp-installation-and-getting-started-part-ii-d009f7a177f3) blog posts from one of the core dev team members of Spark NLP.



In preparation for Part II, please follow the installation/setup steps below before coming to the tutorial:


+ If you have attended Part I of the tutorial, Do a `git pull` to make sure you have the latest updates in this repository. If you have not attended Part I, clone this repo into your machine by running `git clone https://github.com/ftarlaci/bigdata_ai_nlp_tutorial.git` in your command line. The files that we will be working with during Part II can be found inside `nlp-tutorial-part-ii` folder in this repository. 

### Option 1: Setup by Using Google Colab 

We will be using Google Colab during the session. If you have not used colab before, please follow the steps to set it up for the tutorial. 

1. If you don't have a gmail account, you will need to create one to be able to use Google Colab.
2. Login to your google drive by going to drive.google.come, then click on `My Drive`. Inside My Drive, you will find a folder, named "Colab Notebooks". Click on this folder.  
    + If you don't see `Colab Notebooks` in your drive, on the left side of the screen, click on `New`, scroll down to `More`, and select `Google Colaboratory`. 
    + Note: you may need click on `Connect more apps` if you do not see `Google Colab` listed.  You will then search for `colab` and install it into your google drive.  
3. Upload the "nlp-tutorial-part-ii" folder from inside this repository to Google Drive. This will upload the files you need for Part II on colab. 
4. Navigate to the "nlp-tutorial-part-ii" folder that you have uploaded on Google Drive. To open up any notebook in Google Colab, right click on the notebook file and select "open with", then select Google Colab.



### Option 2: Setup by Using Jupyter Notebook

You can choose to use Jupyter Notebook as we did in Part I, if you prefer to do so. If you do, install Spark NLP by following the installation steps below: 

You can install Spark NLP either with `pip` or `conda`

### Install Spark NLP from PyPI

`pip install spark-nlp==2.5.3`


### Install Spark NLP from Anaconda/Conda

`conda install -c johnsnowlabs spark-nlp`

+ If you would like to install spark-nlp into a conda environment (recommended), follow the steps below. In your terminal, type:

`java -version  #should be Java 8 (Oracle or OpenJDK)`  (If Java in your machine needs to be updated, see [this page](https://www.java.com/en/download/help/update_runtime_settings.xml))

`conda create -n sparknlp python=3.6 -y`

`conda activate sparknlp`

`pip install spark-nlp==2.5.3 pyspark==2.4.4`


After the installation, please make sure the following lines of code runs in your Jupyter Notebook without any errors:

```yaml
import sparknlp
spark = sparknlp.start()
print("Spark NLP version")
sparknlp.version()
print("Apache Spark version")
spark.version
```