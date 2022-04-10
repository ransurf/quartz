---
title: Course
---
<% tp.file.cursor(1) %>---
started: <% tp.file.cursor(5) %>
finished:
rating: 
---
Status: #📥<% tp.file.cursor(2) %>
Tags: <% tp.file.cursor(3) %>
Links: [) Courses](out/-courses.md)
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
list from [<% tp.file.title %>](None) AND !outgoing([<%tp.file.title%>](None))
```
___

Created:: <%tp.date.now("YYYY-MM-DD HH:MM") %>