---
title: Create new variables
parent: Cleaning Data in Python
layout: default
nav_order: 8
---

### **Create new variables**

We can create a new column “CITIZEN” and designate the value for all observations to be 1:

```py
data.assign(CITIZEN = 1)
```

![](https://data.library.utoronto.ca/sites/default/public/pictures/xpy012.png.pagespeed.ic.DBRUpsyiHT.png)![]({{ '/assets/images/CleanDataPython-52.PNG' | relative_url }})

...

![]({{ '/assets/images/CleanDataPython-53.PNG' | relative_url }})

You can see a new column "CITIZEN" is added in the image at the end of the dataset.