---
title: = Thoughts
---
Status: #🔎
Tags: [Ideas](None)
Links: [My Inputs](out/my-inputs.md)
___
# = Thoughts
- Consider using thoughts as inputs that can create/add onto already existing notes
## Questions
```dataview
table Created
from #💭/questions
where file.name[0] = "="
sort Created desc
```
## Feelings
```dataview
table Created
from #💭/feelings
where file.name[0] = "="
sort Created desc
```
## Reflections
```dataview
table Created
from #💭/reflections
where file.name[0] = "="
sort Created desc
```
## Ideas
```dataview
table Created
from #💭/ideas
where file.name[0] = "="
sort Created desc
```
## Plans
```dataview
table Created
from #💭/plans
where file.name[0] = "="
sort Created desc
```
## All Unsorted
```dataview
list
where file.name[0] = "="
where file.name != "= Thoughts"
sort Created desc
```
___
# Backlinks
```dataview
list from [(](None)
where file.name[0] != "("
```

___
Created:: 2021-07-15 17:07
