---
title: Todoist Sync Plugin
---
Status: 
Tags: 
Links: [Obsidian Plugins](out/obsidian-plugins.md) - [Todoist](out/todoist.md)
___
# Todoist Sync Plugin
[Filters](https://get.todoist.help/hc/en-us/articles/205248842-Filters)
[Github](https://github.com/jamiebrynes7/obsidian-todoist-plugin)
## Parameters
````
```todoist
{
"name": "Todoist",
"filter": "(overdue | today | no date) & ",
"sorting": ["date", "priority"]
}
```
````
## Examples
### Projects
````
```todoist
{
"name": "Project Tasks",
"filter": "(today | overdue) & #School ",
"sorting": ["priority"]
}
```
````
___
# Backlinks
```dataview
list from [Todoist Sync Plugin](out/todoist-sync-plugin.md) AND !outgoing([Todoist Sync Plugin](out/todoist-sync-plugin.md))
```
___
References:

Created:: 2021-09-11 13:14
