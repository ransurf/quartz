---
title: Obsidian to Anki Formatting Quick Reference
---
Status:
Tags: 
Links: [Anki MOC](out/anki-moc.md)
___
# Obsidian to Anki Formatting Quick Reference
- [Anki Flashcard Templates](out/anki-flashcard-templates.md)
```ad-Flashcard
collapse:closed
STARTI [Basic] <% tp.file.cursor(2) %> Back: <% tp.file.cursor(3) %> Tags: <!--ID: 1632506947329--> ENDI

```
##### Inline Notes
```
STARTI [Basic] <% tp.file.cursor(2) %> Back: <% tp.file.cursor(3) %> Tags: <% tp.file.cursor(4) %>  <!--ID: 1632107333137--> ENDI
```

```
STARTI [<% tp.file.cursor(1) %>] <% tp.file.cursor(2) %> Back: <% tp.file.cursor(3) %> Tags: <% tp.file.cursor(4) %>  ENDI
```
##### Cloze Formatting
{cloze} or {1:cloze} or {1|cloze} 
___
References:

Created:: 2021-06-01 19:22 PM