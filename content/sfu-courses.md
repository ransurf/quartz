---
title: SFU Courses
---
Status: 
Tags: 
Links: [SFU](out/sfu.md)
___
# SFU Courses
## [mySchedule](https://myschedule.erp.sfu.ca/criteria.jsp?access=0&lang=en&tip=1&page=results&scratch=0&advice=0&term=0&sort=none&filters=liiiiiiii&bbs=&ds=&cams=BRNBY_GNWC_METRO_OFFST_SURRY_VANCR&locs=any&isrts=)
## Current Courses
```dataview
table credits, wqb
from #sfu_course 
where file.name != "Course Template"
where year = 1 AND semester = 2
```
## Principles
### Time Dedication
- 1 class hour + 1-2 study hours per course credit
	- 3 class hours and 6-9 study hours for a 3 credit course
	- 36-48 hours per week on 
## Course Plan
- [Course Selection Plan (Computer Science)](out/course-selection-plan-computer-science.md)

### Game Dev
IAT 167
___
# Backlinks
```dataview
list from [SFU Courses](out/sfu-courses.md) AND !outgoing([SFU Courses](out/sfu-courses.md))
```
___
References:

Created:: 2021-08-23 20:47
