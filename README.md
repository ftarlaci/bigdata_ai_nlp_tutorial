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


## Part II

We will update this repository and this README file for Part II of the tutorial with further instructions. Please revisit this repo before coming to the Part II next week. 