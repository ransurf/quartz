---
title: Obsidian Breadcrumbs Plugin
---
Status: 
Tags: 
Links: [Obsidian Plugins](out/obsidian-plugins.md)
___
# Obsidian Breadcrumbs Plugin
## Principles
- Allows a new hierarchical form
### Relationships
- Down
- Same
- Up
- next
- prev
### Creating Structure
Tag notes
- `BC-tag-note: {tag}`
- `BC-tag-note-field: {relationship}`
- Any note with `tag` will have a `relationship` with the current note

Link notes
- `BC-link-note: {relationship}`
- This is most useful imo

Folder notes
- `BC-folder-note: {relationship}`
- All other notes in the relationship will have the main note as `relationship`

Traverse notes
- `BC-traverse-note: {relationship}`
- Depth-first traversal
- Helps with connecting things with an already hierarchical structure

Hierarchy Notes
- Hierarchy note must be set
- Allows you to declare hierarchies using bulleted points in a text file
```md
- [A](None)
	- [a](None)
	- [b](None)
```
### Views
Matrix
- Labels
Trail
- 
Stats

Down
- Bullet list

Ducks
- Use quieries to remove brad-crumbs

Visualization
- Graph view

### Additional Features
- Write breadcrumbs current file
- Create index of all hierarchies
- Jump around relationships
- Create new {relationship} note
	- Automatically adds metadata
___
# Backlinks
```dataview
list from [Obsidian Breadcrumbs Plugin](out/obsidian-breadcrumbs-plugin.md) AND !outgoing([Obsidian Breadcrumbs Plugin](out/obsidian-breadcrumbs-plugin.md))
```
___
References:

Created:: 2022-01-07 01:58
