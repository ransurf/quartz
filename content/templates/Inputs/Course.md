<% tp.file.cursor(1) %>---
started: <% tp.file.cursor(5) %>
finished:
rating: 
---
Status: #📥<% tp.file.cursor(2) %>
Tags: <% tp.file.cursor(3) %>
Links: [[) Courses]]
___
# <% tp.file.title %>
> [Link](<% tp.file.cursor(4) %>)
## Notes
<% tp.file.cursor(6) %>
## Thoughts/Questions
- 
___
# Backlinks
```dataview
list from [[<% tp.file.title %>]] AND !outgoing([[<%tp.file.title%>]])
```
___

Created:: <%tp.date.now("YYYY-MM-DD HH:MM") %>