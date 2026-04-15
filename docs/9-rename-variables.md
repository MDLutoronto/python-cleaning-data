---
title: Rename variables
parent: Cleaning Data in Python
layout: default
nav_order: 9
---

### **Rename variables**

To rename the column "ADM_RNO" to "ADM" and the column "GEO_PRV" to "GEO", the following code can be used:

```py
data.rename(columns={'ADM_RNO':'ADM', 'GEO_PRV':'GEO'})
```

![](https://data.library.utoronto.ca/sites/default/public/pictures/xpy013.png.pagespeed.ic.HJbEG3MWmI.png)![]({{ '/assets/images/CleanDataPython-54.PNG' | relative_url }})