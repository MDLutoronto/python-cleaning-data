---
title: Merge two datasets
parent: Cleaning Data in Python
layout: default
nav_order: 10
---

### **Merge two datasets**

Sometimes, it is necessary to merge disparate datasets.

In order to demonstrate the merge command, we will first select and 'save' 2 subsets from our dataset that we can then merge. It is important to remember that we are merging these datasets based on a unique shared key, the first column (Index), and as a result both subsets will share this column. Subset_7 will include the first 10 observations with columns 0 - 99; subset_8 will include the first 10 observations with columns 1, 100, 101 and 102.