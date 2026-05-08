---
title: Merge two datasets
parent: Cleaning Data in Python
layout: default
created_date: 2016-11-01
maintainer:
    - name: Neil Aitken
      link: https://library.utoronto.ca/staff/neil-aitken
nav_order: 10
---

### **Merge two datasets**

Sometimes, it is necessary to merge disparate datasets.

In order to demonstrate the merge command, we will first select and 'save' 2 subsets from our dataset that we can then merge. It is important to remember that we are merging these datasets based on a unique shared key, the first column (Index), and as a result both subsets will share this column. Subset_7 will include the first 10 observations with columns 0 - 99; subset_8 will include the first 10 observations with columns 1, 100, 101 and 102.

**Technique:** [Cleaning data](https://mdlutoronto.github.io/tutorials-search/?technique=Cleaning+data) \| **Tools:** [Python](https://mdlutoronto.github.io/tutorials-search/?tool=Python)