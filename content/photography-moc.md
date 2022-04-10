---
title: Photography MOC
---
Status: #🗺️ 
Tags: [Cameras](out/cameras.md) - [Hobbies MOC](out/hobbies-moc.md)
Links: [040 Interests MOC](out/040-interests-moc.md)
___
# Photography MOC
- [Street Photography](out/street-photography.md)

## Inputs
### Articles
```dataview
table Created
from [Photography MOC](out/photography-moc.md)
from #📥 
where file.name[0] = "("
sort Created desc
```
### Videos
```dataview
table Created
from [Photography MOC](out/photography-moc.md)
from #📥
where file.name[0] = "+"
sort Created desc
```
### Books
```dataview
table Created
from [Photography MOC](out/photography-moc.md)
from #📥
where file.name[0] = "{"
sort Created desc
```
## References
### Thoughts
##### Ideas
```dataview
table Created
from #💭/ideas AND [Photography MOC](out/photography-moc.md)
sort Created desc
```
##### Feelings
```dataview
table Created
from #💭/feelings AND [Photography MOC](out/photography-moc.md)
sort Created desc
```
##### Questions
```dataview
table Created
from #💭/questions AND [Photography MOC](out/photography-moc.md)
sort Created desc
```
### Other Notes
```dataview
list from [Photography MOC](out/photography-moc.md) AND !outgoing([Photography MOC](out/photography-moc.md))
```
___
References:

Created:: 2021-08-04 20:32