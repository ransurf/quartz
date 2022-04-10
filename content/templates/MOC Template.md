Status: #🗺️ 
Tags: 
Links: [[Note Taking]]
___
# MOC Template
## Tools
- [[Obsidian MOC]]
- [[Notion MOC]]

## Inputs
### Articles
```dataview
table Created
from [[MOC Template]]
from #📥 
where file.name[0] = "("
sort Created desc
```
### Videos
```dataview
table Created
from [[MOC Template]]
from #📥
where file.name[0] = "+"
sort Created desc
```
### Books
```dataview
table Created
from [[MOC Template]]
from #📥
where file.name[0] = "{"
sort Created desc
```
## References
### Thoughts
```dataview
table Created
from #💭/ AND [[MOC Template]]
sort Created desc
```
### Other Notes
```dataview
list from [[MOC Template]] AND !outgoing([[MOC Template]])
```
___
References:

Created:: 2022-02-11 22:18