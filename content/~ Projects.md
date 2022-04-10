tags:
Index: [[Index (Archived)|Index]], [[My Inputs|Ideas]]
___
# ~ Projects
## Monthly Projects
```dataview
table deadline
FROM #projects/monthly
WHERE file.name != "Project Template" and !hibernating
WHERE completed = null
SORT deadline desc
```
## Weekly Projects
```dataview
table deadline
FROM #projects/weekly
WHERE file.name != "Project Template" and !hibernating
WHERE completed = null
SORT deadline asc
```
## Hibernating
```dataview
table deadline
FROM #projects
WHERE file.name != "Project Template" and hibernating
WHERE completed = null
SORT deadline desc
```
## Kanban Boards
- [[Youtube Kanban]]
## Archived
```dataview
table archived
FROM #projects/archived
WHERE file.name != "Project Template"
SORT completed desc
```
## Completed
```dataview
table completed
FROM #projects
WHERE file.name != "Project Template" AND completed != null
SORT completed desc
```
___