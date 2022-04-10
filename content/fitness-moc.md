---
title: Fitness MOC
---
 Status: #🗺️ 
Tags: 
Links: [Wellness MOC](out/wellness-moc.md)
___
# Fitness MOC
> [My Fitness Plan](out/my-fitness-plan.md)
## Inputs
### Articles
```dataview
table Created
from [Fitness MOC](out/fitness-moc.md)
from #📥 
where file.name[0] = "("
sort Created desc
```
### Videos
```dataview
table Created
from [Fitness MOC](out/fitness-moc.md)
from #📥
where file.name[0] = "+"
sort Created desc
```
### Books
```dataview
table Created
from [Fitness MOC](out/fitness-moc.md)
from #📥
where file.name[0] = "{"
sort Created desc
```
## References
### Thoughts
##### Ideas
```dataview
table Created
from [Fitness MOC](out/fitness-moc.md) AND #💭/ideas

sort Created desc
```
##### Feelings
```dataview
table Created
from #💭/feelings AND [Fitness MOC](out/fitness-moc.md)
sort Created desc
```
##### Questions
```dataview
table Created
from #💭/questions AND [Fitness MOC](out/fitness-moc.md)
sort Created desc
```
___
References:

Created:: 2021-08-04 20:28
