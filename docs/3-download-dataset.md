---
title: Download Dataset
parent: Cleaning Data in Python
layout: default
nav_order: 3
---

### **Download Dataset**

The dataset used in this tutorial is the **Canadian Community Health Survey, 2012: Mental Health Component**. You can directly access the dataset from here: [https://search1.odesi.ca/#/details?uri=%2Fodesi%2Fcchs-82M0013-E-2012-m…](https://search1.odesi.ca/#/details?uri=%2Fodesi%2Fcchs-82M0013-E-2012-mental-health.xml), or you can go to [odesi.ca](https://search2.odesi.ca/#/) and search for the term "CCHS 2012". Choose the entry, "Canadian Community Health Survey, 2012: Mental Health Component".

After loading the page, click "Explore & Download".

![]({{ '/assets/images/CleanDataPython-35.PNG' | relative_url }})

In this new page, find the "**Download**" button on the top right corner.

![]({{ '/assets/images/CleanDataPython-36.PNG' | relative_url }})

 

In the download page, from the "select the data format" drop-down menu, pick "**Comma Separated Value file**" for a csv file that python can work with. Check the "Include documentation" box, and then click "DOWNLOAD" to download the dataset and the related documentation in a compressed zip file.

![]({{ '/assets/images/CleanDataPython-37.PNG' | relative_url }})

This downloaded file must be unzipped before it can be used. If this is unfamiliar to you, this [tutorial](https://www.techolac.com/how-to/how-to-zip-and-unzip-files-on-windows-and-mac/) covers unzipping files in both windows and mac operating systems.

You will find a csv file and a PDF file in the unzipped folder. The csv file contains the data we will be cleaning, and the PDF file contains the metadata in the form of a codebook for all variables in this dataset. We will refer to the codebook if we would like more information on a certain variable.