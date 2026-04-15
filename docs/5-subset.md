---
title: Subset
parent: Cleaning Data in Python
layout: default
nav_order: 5
---

### **Subset**

Pandas offers a variety of options for selecting subests of a dataset. Subset selection is simply selecting particular rows and columns of data from your data frame.

**You can create a subset by selecting observations**: e.g. get the first 100 observations (rows)

```py
data.iloc[:100,:] #get the first 100 observations in a dataset
```

![]({{ '/assets/images/CleanDataPython-13.PNG' | relative_url }})![](https://data.library.utoronto.ca/sites/default/public/pictures/xpy004.png.pagespeed.ic.z8mZ_bDESL.png)

**...                 ...            ...              ...                ...        ...**

![]({{ '/assets/images/CleanDataPython-14.PNG' | relative_url }})

**By selecting variables**: e.g. get the first 100 variables (columns)

```py
data.iloc[:,:100] #get the first 100 variables in a dataset
```

![](https://data.library.utoronto.ca/sites/default/public/pictures/xpy005.png.pagespeed.ic.Ebl59BxZcn.png)![]({{ '/assets/images/CleanDataPython-15.PNG' | relative_url }})

**...                       ...               ...              ...            ...           ...           ...**

**![]({{ '/assets/images/CleanDataPython-16.PNG' | relative_url }})**

**Or by selecting both**: e.g. get the first 100 rows and 100 columns of the original dataset

```py
data.iloc[:100,:100] #get the first 100 rows * 100 columns
```

![](https://data.library.utoronto.ca/sites/default/public/pictures/xpy006.png.pagespeed.ic.61cJarnPzV.png)![]({{ '/assets/images/CleanDataPython-17.PNG' | relative_url }})

**...                  ...             ...             ...           ...           ...**

**![]({{ '/assets/images/CleanDataPython-18.PNG' | relative_url }})**

**Furthermore, you can create a subset by selecting variable names**: e.g. get column “VERDATE”, “ADM_RNO”,  and “GEO_PRV”

```py
data.loc[:,['VERDATE', 'ADM_RNO', 'GEO_PRV']]
```

![](https://data.library.utoronto.ca/sites/default/public/pictures/xpy007.png.pagespeed.ic.6qrisksez7.png)![]({{ '/assets/images/CleanDataPython-19.PNG' | relative_url }})

**...            ...                     ...                     ...**

**![]({{ '/assets/images/CleanDataPython-20.PNG' | relative_url }})**