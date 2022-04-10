---
title: Monthly Reviews
---
Status:
Tags: 
Links: [Periodic Reviews](out/periodic-reviews.md)
___
# Monthly Reviews
## 2022
```dataview
list 
from [Monthly Reviews](out/monthly-reviews.md)
where file.name[0] = "2" AND file.name[3] = "2"
sort file.name desc
```
## 2021
```dataview
list 
from [Monthly Reviews](out/monthly-reviews.md)
where file.name[0] = "2" AND file.name[3] = "1"
sort file.name desc
```
___
# Backlinks
```dataview
list from [Monthly Reviews](out/monthly-reviews.md) AND !outgoing([Monthly Reviews](out/monthly-reviews.md))
```
___
References:

Created:: 2021-05-30 21:24 PM