---
title: !M Meal Ideas MOC
---
Status: #🗺️ 
Tags: 
Links: [Cooking MOC](Cooking%20MOC) - [Food MOC](Food%20MOC)
___
# !M Meal Ideas MOC
### Ideas
- [Slow Carb Diet Meal Plan](Slow%20Carb%20Diet%20Meal%20Plan)
- Spinach omelette
- Chicken breast with brocolli/premade salad
- Side of mixed berries
- Bento box
## Meals
```dataview
table Type, Serving, MealPrep
from [!M Meal Ideas MOC](!M%20Meal%20Ideas%20MOC)
where file.name != "Meal Idea Template" AND file.name[0] = "!" AND file.name[1] = "M"
```
## Inputs
### Reddit Searches
[r/Cheap_Meals "Student Budget"](https://www.reddit.com/r/Cheap_Meals/search?q=student+budget&restrict_sr=on)
[r/MealPrepSunday "Student Budget"](https://www.reddit.com/r/MealPrepSunday/search?q=student&restrict_sr=on)
### Articles
```dataview
table Created
from [!M Meal Ideas MOC](!M%20Meal%20Ideas%20MOC)
from #📥 
where file.name[0] = "("
sort Created desc
```
### Videos
```dataview
table Created
from [!M Meal Ideas MOC](!M%20Meal%20Ideas%20MOC)
from #📥
where file.name[0] = "+"
sort Created desc
```
### Books
```dataview
table Created
from [!M Meal Ideas MOC](!M%20Meal%20Ideas%20MOC)
from #📥
where file.name[0] = "{"
sort Created desc
```
## References
### Thoughts
##### Ideas
```dataview
table Created
from #💭/ideas AND [!M Meal Ideas MOC](!M%20Meal%20Ideas%20MOC)
sort Created desc
```
##### Feelings
```dataview
table Created
from #💭/feelings AND [!M Meal Ideas MOC](!M%20Meal%20Ideas%20MOC)
sort Created desc
```
##### Questions
```dataview
table Created
from #💭/questions AND [!M Meal Ideas MOC](!M%20Meal%20Ideas%20MOC)
sort Created desc
```
### Other Notes
```dataview
list from [!M Meal Ideas MOC](!M%20Meal%20Ideas%20MOC) AND !outgoing([!M Meal Ideas MOC](!M%20Meal%20Ideas%20MOC))
```
___
References:

Created:: 2021-08-15 12:42
