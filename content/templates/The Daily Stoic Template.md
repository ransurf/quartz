 <% tp.file.cursor(1) %>Status:
Tags: #TDS/<%tp.date.now("MM") %>/<%tp.date.now("DD") %> <% tp.file.cursor(5) %>
Links: [[The Daily Stoic Reflections]]
___
# <% tp.file.title %>
Message:: <% tp.file.cursor(2) %>

## Reflections
 ```query
line:"### [[<%tp.file.title%>]]"
```
___
# Backlinks
```dataview
list from [[<% tp.file.title %>]] AND !outgoing([[<% tp.file.title %>]])
```
___

Created:: <% tp.date.now("YYYY-MM-DD HH:mm") %>
