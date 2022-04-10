---
title: My Routines
---
Status:
Tags: 
Links: [Routines](None)
___
# My Routines
```dataview
list 
where contains(lower(file.name), "my") AND contains(lower(file.name), "routine")
```
___
# Backlinks
```dataview
list from [My Routines](out/my-routines.md) AND !outgoing([My Routines](out/my-routines.md))
where !contains(lower(file.name), "my") AND contains(lower(file.name), "routine")
```
___
References:

Created:: 2021-08-31 00:33
