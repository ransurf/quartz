---
title: { Books MOC
---
tags: #🗺️ 
Links: [Index](out/index-archived.md), [Interests](out/040-interests-moc.md)
___
# { Books MOC
Also see: [Book Applications](out/references/books/applications/book-applications.md)

## Book Lists
### Library
- [Potential Books List](out/potential-books-list.md)
### Plan To Read
```dataview
table started, finished, rating, practiced
FROM #literature/books/planning
SORT planned desc
```
- [Plan-to-Read List](out/references/books/plan-to-read-list.md)
### Currently Reading
```dataview
table started, finished, rating, practiced
FROM #literature/books/reading
SORT started desc
```
### On-Hold
- [Envy - Theory of Social Behavior](out/references/books/summaries/envy-theory-of-social-behavior.md)
- [The Intelligent Investor](out/references/books/summaries/the-intelligent-investor.md)
- [The Well-Educated Mind](out/the-well-educated-mind.md)
- [Make it Stick by Peter Brown](out/make-it-stick-by-peter-brown.md)
- [The Visual MBA](out/the-visual-mba.md)
- [The War of Art](out/the-war-of-art.md)
- [On-Hold List](out/on-hold-list.md)
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
 - [Refind Daily Reads](out/references/books/refind-daily-reads.md)

