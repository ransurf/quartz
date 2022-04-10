---
title: Art MOC
---
Status: #🗺️ 
Tags: [Creativity](None)
Links: [040 Interests MOC](out/040-interests-moc.md)
___
# Art MOC
- [Photography MOC](out/photography-moc.md)

## Inputs
### Articles
```dataview
table Created
from [Art MOC](out/art-moc.md)
from #📥 
where file.name[0] = "("
sort Created desc
```
### Videos
```dataview
table Created
from [Art MOC](out/art-moc.md)
from #📥
where file.name[0] = "+"
sort Created desc
```
### Books
```dataview
table Created
from [Art MOC](out/art-moc.md)
from #📥
where file.name[0] = "{"
sort Created desc
```
## References
### Thoughts
##### Ideas
```dataview
table Created
from #💭/ideas AND [Art MOC](out/art-moc.md)
sort Created desc
```
##### Feelings
```dataview
table Created
from #💭/feelings AND [Art MOC](out/art-moc.md)
sort Created desc
```
##### Questions
```dataview
table Created
from #💭/questions AND [Art MOC](out/art-moc.md)
sort Created desc
```
___
References:

Created:: 2021-08-05 02:40
