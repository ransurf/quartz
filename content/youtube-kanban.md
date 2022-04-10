---
title: Youtube Kanban
---
Status: 
Tags: 
Links: [Youtube MOC](out/scripts/youtube-moc.md)
___
# Youtube Kanban
## In Progress
> #📹/🟥 == Details
> #📹/🟧 == Outline
> #📹/🟨 == Script
> #📹/🟩 == Audio/Video Production
> #📹/🟦 == Thumbnail/Description
> #📹/🟪 == Ready to Upload
> #📹/⬛ == Finished
### [!V Video Ideas](out/v-video-ideas.md)
### Details
```dataview
table created, status, category
from #videoidea AND #📹/🟥 

sort created desc
```
### Outline
```dataview
table created, status, category
from #videoidea AND #📹/🟧 

sort created desc
```
### Script
```dataview
table created, status, category
from #videoidea AND #📹/🟨 

sort created desc
```
### Audio/Video Production 
```dataview
table created, status, category
from #videoidea AND #📹/🟩

sort created desc
```
### Thumbnail/Description 
```dataview
table created, status, category
from #videoidea AND #📹/🟦 

sort created desc
```
### Ready to Upload  
```dataview
table created, status, category
from #videoidea AND #📹/🟪 

sort created desc
```
### Finished
```dataview
table created, status, category, finished
from #videoidea AND #📹/⬛ 

sort created desc
```
___
# Backlinks
```dataview
list from [Youtube Kanban](out/youtube-kanban.md) AND !outgoing([Youtube Kanban](out/youtube-kanban.md))
```
___
References:

Created:: 2021-08-12 18:25
