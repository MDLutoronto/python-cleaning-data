---
title: Load dataset into Spyder
parent: Cleaning Data in Python
layout: default
nav_order: 4
---

### **Load dataset into Spyder**

After you open Spyder, you can direct it to the dataset that you want to clean. This is the location (path) of where your unzipped folder is saved on your computer and is achieved by running a few lines of code that set up your working directory. If you are new to paths and working directories, a succinct introduction can be found [here](https://www.earthdatascience.org/courses/intro-to-earth-data-science/python-code-fundamentals/work-with-files-directories-paths-in-python/). Furthermore, these tutorials provide instructions on determining the path of your unzipped folder in [windows](https://www.isumsoft.com/computer/2-ways-to-copy-full-path-of-files-and-folders.html) and [mac](https://www.switchingtomac.com/tutorials/osx/5-ways-to-reveal-the-path-of-a-file-on-macos/) operating systems.

The following code for sets up a working directory. Please note, in python, anything after the "#" symbol is considered to be comments related to the code.

```py
import os #import the os library (enables operating system dependent functionality)  
os.chdir('C:YourFolderPathGoesHere') #change directory  
os.getcwd() #get the current working directory to confirm the directory change
```

![]({{ '/assets/images/CleanDataPython-38_0.PNG' | relative_url }})

The first line of code imports the module that contains the operating system interface (which includes the subsequent functions that allow for changes to the working directory). The second line changes the working directory to where the unzipped folder is saved. The last line confirms the working directory has been changed. If after running the last file the correct folder path of you unzipped folder isn't returned, check to make sure your code and/or your folder path is correct.

Above the console in the "***Help***" pane, you can take a look of the files loaded in this directory under the "***File Explorer***" tab.

![]({{ '/assets/images/CleanDataPython-42.PNG' | relative_url }})

You can then input the below scripts in the console to load your dataset into the program. Note that the csv file has to be in the current working directory, otherwise an error will be raised.

```py
import pandas #import the pandas data analysis library 
data = pandas.read_csv('cchs-82M0013-E-2012-mental-health_F1.csv')
```

![]({{ '/assets/images/CleanDataPython-39.PNG' | relative_url }})

The first line imports the ***pandas*** library, which will be used throughout this tutorial. The next line uses the ***read_csv*** command in pandas to load the CCHS2012 dataset to the system and assigmins it the variable "data". From now on, when you want to refer to your CCHS2012 dataset, you can just use the variable "data".

It is always helpful to get an idea of our dataset before cleaning it. Above the console in the ***Help*** pane, by clicking on the tab "***Variable explorer***" you will be able to see the details of each variable defined in the current console session, including data type and size.

![]({{ '/assets/images/CleanDataPython-40.PNG' | relative_url }})

Double-clicking a variable in the "Variable explorer" pane will open a new window displaying the whole dataset.

![]({{ '/assets/images/CleanDataPython-41_0.PNG' | relative_url }})

We can also see the dimension of the dataset using the ***shape*** command. In our case, the dataset has 25113 rows and 586 columns.

```py
print(data.shape)
```

![]({{ '/assets/images/CleanDataPython-43.PNG' | relative_url }})

Furthermore, we can view the descriptive statistics of the varaibles in our dataset with numeric values using the ***describe*** command.

```py
data.describe()
```

![]({{ '/assets/images/CleanDataPython-44.PNG' | relative_url }})

It is important for our analysis to identify the missing values in our dataset. This can be achieved by setting determined missing values to **NaN** (missing data) when we are loading the dataset into the program (using the "read_csv" function introduced above).

Suppose a column that's expected to have numerical values has recorded the letter 'g' by mistake in some records. We can use the below code to set these extraneous values to NaN.

```py
data = pandas.read_csv('cchs-82M0013-E-2012-mental-health_F1.csv', header=0, na_values=['g'])

#we can assign the variable 'data_no_gs' for example to retain the original 'data' variable
```

![]({{ '/assets/images/CleanDataPython-44_0.PNG' | relative_url }})

If a dataset contains missing data indicated by 'NA', you can read the data in as follows:

```py
data = pandas.read_csv('cchs-82M0013-E-2012-mental-health_F1.csv', header=0, na_values=['NA'])
```

![]({{ '/assets/images/CleanDataPython-46.PNG' | relative_url }})

Furthremore, if we want to understand how a particular dataset records missing values to then identify them in the program, we can refer to the dataset's metadata for these details.

In our case, we will refer to the accompanying downloaded codebook, where it states that the value '96' denotes the term 'Not Applicable'. To then set this value to 'NaN' the the following code can be used.

```py
data = pandas.read_csv('cchs-82M0013-E-2012-mental-health_F1.csv', header=0, na_values=[96])
```

![]({{ '/assets/images/CleanDataPython-45.PNG' | relative_url }})

You can find all the rows where a specific column holds NaN values as follows:

```py
data[pandas.isnull(data['GEO_PRV'])]
```

Though in this case, the column 'GEO_PRV' does not contain any NaN values, resulting in an empty data frame.

![]({{ '/assets/images/CleanDataPython-10.PNG' | relative_url }})