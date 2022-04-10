Status: #🗺️ 
Tags: 
Links: [[000 Index]]
___
# 030 Career MOC
> [[Youtube MOC]]
> [[Coding MOC]]
> [[Job]]
## Principles

Roles should update every 3-4 years
- Either promotion or work somewhere else
## Inputs
### Articles
```dataview
table Created
from [[020 Career MOC]]
from #📥 
where file.name[0] = "("
sort Created desc
```
### Videos
```dataview
table Created
from [[020 Career MOC]]
from #📥
where file.name[0] = "+"
sort Created desc
```
### Books
```dataview
table Created
from [[020 Career MOC]]
from #📥
where file.name[0] = "{"
sort Created desc
```
## References
### Thoughts
```dataview
table Created
from #💭/ AND [[020 Career MOC]]
sort Created desc
```
### Other Notes
```dataview
list from [[020 Career MOC]] AND !outgoing([[020 Career MOC]])
```
___
References:

Created:: 2022-01-07 03:31
