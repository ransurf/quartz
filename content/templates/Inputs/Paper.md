---
title: Paper
---
<% tp.file.cursor(1) %>---
started: <% tp.file.cursor(5) %>
finished:
rating: 
---
Status: #📥<% tp.file.cursor(2) %>
Tags: <% tp.file.cursor(3) %>
Links: [& Papers](out/-papers.md)
___
# <% tp.file.title %>
> [Link](<% tp.file.cursor(4) %>)
## Notes
<% tp.file.cursor(6) %>
### Ideas
### Actionable
## Thoughts/Questions
- 
### Review
### Connections
___
# Backlinks
```dataview
list from [<% tp.file.title %>](None) and !outgoing([<% tp.file.title %>](None))
```
___

Created:: <%tp.date.now("YYYY-MM-DD HH:MM") %>