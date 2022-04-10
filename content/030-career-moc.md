---
title: 030 Career MOC
---
Status: #🗺️ 
Tags: 
Links: [000 Index](out/000-index.md)
___
# 030 Career MOC
> [Youtube MOC](out/scripts/youtube-moc.md)
> [Coding MOC](out/coding-moc.md)
> [Job](out/job.md)
## Principles

Roles should update every 3-4 years
- Either promotion or work somewhere else
## Inputs
### Articles
```dataview
table Created
from [020 Career MOC](None)
from #📥 
where file.name[0] = "("
sort Created desc
```
### Videos
```dataview
table Created
from [020 Career MOC](None)
from #📥
where file.name[0] = "+"
sort Created desc
```
### Books
```dataview
table Created
from [020 Career MOC](None)
from #📥
where file.name[0] = "{"
sort Created desc
```
## References
### Thoughts
```dataview
table Created
from #💭/ AND [020 Career MOC](None)
sort Created desc
```
### Other Notes
```dataview
list from [020 Career MOC](None) AND !outgoing([020 Career MOC](None))
```
___
References:

Created:: 2022-01-07 03:31
