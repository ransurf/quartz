---
title: Outfits MOC
---
Status: #🗺️ 
Tags: 
Links: [Clothes MOC](out/clothes-moc.md) - [Fashion](out/fashion.md)
___
# Outfits MOC
- MUJI dark blue button up, white shirt, black pants, light shoes
	- Dark baggy look
- Kristine's brown button up, yellow hurley t shirt, gray old navy pants, light shoes
	- Subtle gradient to earth tones

## Inputs
### Articles
```dataview
table Created
from [Outfits MOC](out/outfits-moc.md)
from #📥 
where file.name[0] = "("
sort Created desc
```
### Videos
```dataview
table Created
from [Outfits MOC](out/outfits-moc.md)
from #📥
where file.name[0] = "+"
sort Created desc
```
### Books
```dataview
table Created
from [Outfits MOC](out/outfits-moc.md)
from #📥
where file.name[0] = "{"
sort Created desc
```
## References
### Thoughts
##### Ideas
```dataview
table Created
from #💭/ideas AND [Outfits MOC](out/outfits-moc.md)
sort Created desc
```
##### Feelings
```dataview
table Created
from #💭/feelings AND [Outfits MOC](out/outfits-moc.md)
sort Created desc
```
##### Questions
```dataview
table Created
from #💭/questions AND [Outfits MOC](out/outfits-moc.md)
sort Created desc
```
### Other Notes
```dataview
list from [Outfits MOC](out/outfits-moc.md) AND !outgoing([Outfits MOC](out/outfits-moc.md))
```
___
References:

Created:: 2021-08-17 15:51
