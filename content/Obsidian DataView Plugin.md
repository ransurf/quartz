# Obsidian DataView Plugin
Status:
Tags: 
Links: [[Obsidian Community Plugins]]
___
> - Dataview makes soooo much more sense when you can trust that the content of the note is one “unit” (book, day, task, meeting, idea, whatever) and then you add whatever metadata fields are useful to you for retrieving and linking that info.
## Usage

### Commands
`list where contains(lower(file.name), "my")` helps sort for words in a title
`where file.name[x]` helps check for prefixes
### Example Usage
````
```dataview

TABLE|LIST|TASK <field> [AS "Column Name"], <field>, ..., <field> FROM <source> (like #tag or "folder")

WHERE <expression> (like 'field = value')

SORT <expression> [ASC/DESC] (like 'field ASC')

... other data commands

```
````
## Uses
### Not-mentioned links from other notes
````
```dataview
list from [[<% tp.file.title %>]] AND !outgoing([[<% tp.file.title %>]])
sort Created desc
```
````
- Doesn't include any links that are previously mentioned in the note
## Features
- Create tables/lists depending on certain criteria
	- Sorting lists
- Creating custom fields for notes to help with categorization
	- ex) Date modified, aliases, tags
## Practices
- `where tags = "{emoji}"`
- Sorting out daily video ideas
- Creating a list for book notes
> the filter and color group in graph view uses the same query as in search. so you can test out your query in search first. for example, to exclude certain tags. i try this out in the search bar:
> ![](https://cdn.discordapp.com/attachments/709712341066842113/854539810935930880/unknown.png)
___
References: [Website](https://blacksmithgu.github.io/obsidian-dataview/docs/intro) - [Bryan Jenks Video](https://youtu.be/2234DXKbNgM?t=464)

Created:: 2021-06-19 23:24
