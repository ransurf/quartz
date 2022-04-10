Status:
Tags: 
Links: [[Routines]]
___
# My Routines
```dataview
list 
where contains(lower(file.name), "my") AND contains(lower(file.name), "routine")
```
___
# Backlinks
```dataview
list from [[My Routines]] AND !outgoing([[My Routines]])
where !contains(lower(file.name), "my") AND contains(lower(file.name), "routine")
```
___
References:

Created:: 2021-08-31 00:33
