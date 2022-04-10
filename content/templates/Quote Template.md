<%tp.file.cursor(1)%>Status: <% tp.file.cursor(2) %>
Tags: #quote/<% tp.file.cursor(3) %>
Links: [[<% tp.file.cursor(4) %>
___
# <% tp.file.title %>
<% tp.file.cursor(5) %>
# Thoughts
___
# Backlinks
```dataview
list from [[<% tp.file.title %>]] AND !outgoing([[<%tp.file.title%>]])
```
___
References:

Created:: <% tp.date.now("YYYY-MM-DD HH:mm") %>