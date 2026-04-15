---
title: Tranform Data
parent: Cleaning Data in Python
layout: default
nav_order: 7
---

### **Transform data**

In many instances, it will be necessary to transform your dataset to a form you can work with.

You might have to **remove duplicate observations**:

```py
data.drop_duplicates()
```

In our case, there are no duplicate rows that need to be dropped.

![](https://data.library.utoronto.ca/sites/default/public/pictures/xpy010.png.pagespeed.ic.0H0LyLzEFu.png)![]({{ '/assets/images/CleanDataPython-25.PNG' | relative_url }})

**...                       ...               ...           ...               ...               ...        ...**

**![]({{ '/assets/images/CleanDataPython-26.PNG' | relative_url }})**

You might want to **r****eplace values**. To replace all instances of the value 1 with the value 7 for the entire dataset you can use the following code:

```py
data = data.replace(1, 7)
```

The replace function returns a **copy** of the altered dataset but keeps the original dataset intact. In order to retain your changes, it is important to assign a variable to the returning dataset. Using **data =** replaces the previous dataset with the renamed dataset (in this case, the original dataset 'data' is replaced with the result of the replace function).

![](https://data.library.utoronto.ca/sites/default/public/pictures/xpy011.png.pagespeed.ic.kiWPYA_SlG.png)![]({{ '/assets/images/CleanDataPython-27.PNG' | relative_url }})

You might want to **r****ename an index**. To rename the index '0' with 'person1' the following command can be used:

```py
data2 = data.rename(index={0: 'person1'})
```

Again, in order to retain your changes, it is important to assign a variable to the returning dataset. Using **data2 =** ensures the changes are saved to another varaible, keeping the original data frame, named 'data' in tact.

![](https://data.library.utoronto.ca/sites/default/public/pictures/xpy_rename_index.PNG.pagespeed.ic.XgHzvmIPAa.png)![]({{ '/assets/images/CleanDataPython-28.PNG' | relative_url }})

Sometimes numerical values make more sense if clustered together.This is called **discretization or binning**. For example, if we’re trying to differentiate respondents based on their drinking habits, the exact number of drinks might not matter to us. We can use a cut command to group records based on discrete numbers.

Here we are dividing the survery's respondents in 4 groups based on the "Variable AUDG06: Number of drinks per day on days when drank in past 12 months".

```py
pandas.cut(data.AUDG06, 4)
```

![CleanDataPython-47](https://mdl.library.utoronto.ca/sites/default/public/CleanDataPython-47.PNG)



...

![]({{ '/assets/images/CleanDataPython-48.PNG' | relative_url }})

At the bottom of the result, it displays the break values of the dataset for the four categories divided.