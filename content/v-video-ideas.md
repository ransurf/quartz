---
title: !V Video Ideas
---
Status:
Links: [Youtube MOC](Youtube%20MOC)
___
# Video Ideas
> [Video Ideas Brainstorming](Video%20Ideas%20Brainstorming)
> [Youtube Kanban](Youtube%20Kanban)
## Ideas
###### Coding
###### School
```dataview
table created, category
from #videoidea
where contains(lower(category), "school")  and !started
sort created desc
```
###### Productivity
```dataview
table created, category
from #videoidea
where contains(lower(category), "productivity")  and !started
sort created desc
```
###### Trying
```dataview
table created, category
from #videoidea
where contains(lower(category), "trying")  and !started
sort created desc
```
###### Obsidian
```dataview
table created, category
from #videoidea
where contains(lower(category), "obsidian") and !started
sort created desc
```
###### Thoughts
```dataview
table created, category
from #videoidea
where contains(lower(category), "thoughts")  and !started
sort created desc
```
###### Lifestyle
```dataview
table created, category
from #videoidea
where contains(lower(category), "lifestyle")  and !started
sort created desc
```
###### Misc
```dataview
table created, category
from #videoidea
where contains(lower(category), "misc") and !started
sort created desc
```
###### Unsorted
```dataview
table created, category
from #videoidea
where category = null
where file.name != "Video Idea Template"  and !started
sort file.ctime desc
```
## Finished
- [Obsidian Video Ideas](Obsidian%20Video%20Ideas)
- 

---

References:
