tags: #🗺️ 
Links: [[Index (Archived)|Index]], [[040 Interests MOC|Interests]]
___
# { Books MOC
Also see: [[Book Applications]]

## Book Lists
### Library
- [[Potential Books List]]
### Plan To Read
```dataview
table started, finished, rating, practiced
FROM #literature/books/planning
SORT planned desc
```
- [[Plan-to-Read List]]
### Currently Reading
```dataview
table started, finished, rating, practiced
FROM #literature/books/reading
SORT started desc
```
### On-Hold
- [[Envy - Theory of Social Behavior]]
- [[The Intelligent Investor]]
- [[The Well-Educated Mind]]
- [[Make it Stick by Peter Brown]]
- [[The Visual MBA]]
- [[The War of Art]]
- [[On-Hold List]]
### Finished
```dataview
table started, finished, rating, practiced
FROM #literature/books/finished
SORT file.ctime desc
```
### Implemented
```dataview
table started as Started, finished as Finished, rating as Rating
FROM #literature/books/implemented 
SORT file.ctime desc
```

### Others
````
```dataview
table started as Started, finished as Finished, rating as Rating
FROM #literature/books/
SORT file.ctime desc
```
````


## Related
 - [[Refind Daily Reads]]

