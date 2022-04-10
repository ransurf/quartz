Status: #🔎
Tags: [[Learning]]
Links: [[My Inputs]]
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
![[MACM 101 Lectures#MACM 101 Lectures]]
### CMPT 125
```dataview
table Created
from #📥
where file.name[0] = "'" AND class = "CMPT125"
```
![[CMPT 125 Lectures#CMPT 125 Lectures]]
### COGS 110
```query
line:(": [[COGS 110 Lectures]]")
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
list from [[' Classes]]
where file.name[0] != "'"

```
___
Created:: 2021-07-15 17:07
