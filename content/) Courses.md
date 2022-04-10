Status: #🔎 
Tags: [Learning](Learning)
Links: [My Inputs](My%20Inputs)
___
# ) Courses
## School Courses
```dataview
table year as Year, semester as Semester
from #sfu_course 
where file.name[0] = ")" 
sort year desc, semester desc
```
## Other Courses
```dataview
table Created as Created, field as Field
from #📥 AND !#sfu_course
where file.name[0] = ")" 
```
___
# Backlinks
___

Created:: 2021-08-21 17:08
