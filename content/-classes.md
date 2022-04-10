---
title: ' Classes
---
Status: #🔎
Tags: [Learning](out/learning.md)
Links: [My Inputs](out/my-inputs.md)
___
# ' Classes
## Fall 2021
### MACM 101
```dataview
table Created
from #📥
where file.name[0] = "'" AND class = "MACM101"
sort Created desc
```
![MACM 101 Lectures](out/macm-101-lectures.md#MACM 101 Lectures)
### CMPT 125
```dataview
table Created
from #📥
where file.name[0] = "'" AND class = "CMPT125"
```
![CMPT 125 Lectures](out/cmpt-125-lectures.md#CMPT 125 Lectures)
### COGS 110
```query
line:(": [COGS 110 Lectures](None)")
```
### EDUC 100W
```dataview
table Created
from #📥
where file.name[0] = "'" AND contains(lower(class), "educ100w")
```
### GEOG 150
```dataview
table Created
from #📥
where file.name[0] = "'" AND contains(lower(class), "geog150")
sort Created desc
```
___
# Backlinks
```dataview
list from [' Classes](out/-classes.md)
where file.name[0] != "'"

```
___
Created:: 2021-07-15 17:07
