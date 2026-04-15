---
title: Drop Data
parent: Cleaning Data in Python
layout: default
nav_order: 6
---

### **Drop data**

Pandas also allows us to drop, or remove, extraneous data from our dataset.

**We can drop specific observations**: e.g. drop the rows with index 1 and 3

```py
data.drop([1, 3])
```

![](https://data.library.utoronto.ca/sites/default/public/pictures/xpy008.png.pagespeed.ic.ZEtiNeURVz.png)![]({{ '/assets/images/CleanDataPython-21.PNG' | relative_url }})

**...                       ...               ...           ...               ...               ...        ...**

 

**![]({{ '/assets/images/CleanDataPython-22.PNG' | relative_url }})**

**Or we can drop variables**: e.g. drop columns with header "GEOGCMA1" and "ADM_N09". Note that in the command, **axis=1** indicates a column to be dropped. Axis=0 indicates a row/index to be dropped.

```py
data.drop(['GEOGCMA1', 'ADM_N09'], axis=1)
```

![](https://data.library.utoronto.ca/sites/default/public/pictures/xpy009.png.pagespeed.ic.e1dDAHtkQt.png)![]({{ '/assets/images/CleanDataPython-23.PNG' | relative_url }})

**...                       ...               ...           ...               ...               ...        ...**

**![]({{ '/assets/images/CleanDataPython-24.PNG' | relative_url }})**
