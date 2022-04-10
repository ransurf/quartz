---
title: Hobbies MOC
---
Status: #🗺️ 
Tags:
Links: [040 Interests MOC](out/040-interests-moc.md)
___
# Hobbies MOC

## Inputs
### Articles
```dataview
table Created
from [Hobbies MOC](out/hobbies-moc.md)
from #📥 
where file.name[0] = "("
sort Created desc
```
### Videos
```dataview
table Created
from [Hobbies MOC](out/hobbies-moc.md)
from #📥
where file.name[0] = "+"
sort Created desc
```
### Books
```dataview
table Created
from [Hobbies MOC](out/hobbies-moc.md)
from #📥
where file.name[0] = "{"
sort Created desc
```
## References
### Thoughts
##### Ideas
```dataview
table Created
from #💭/ideas AND [Hobbies MOC](out/hobbies-moc.md)
sort Created desc
```
##### Feelings
```dataview
table Created
from #💭/feelings AND [Hobbies MOC](out/hobbies-moc.md)
sort Created desc
```
##### Questions
```dataview
table Created
from #💭/questions AND [Hobbies MOC](out/hobbies-moc.md)
sort Created desc
```
## Backlinks

___
References:

Created:: 2021-08-05 02:42