---
title: ETFs
---
Status: 
Tags: 
Links: [Types of Stocks](out/types-of-stocks.md)
___
# ETFs
```dataview
table Description, MER
from [ETFs](out/etfs.md) AND !outgoing([ETFs](out/etfs.md))
where file.name != "Stock Template" AND file.name[0] = "$" AND file.name[1] = "S"
sort file.name desc
```
___
# Backlinks
```dataview
list from [ETFs](out/etfs.md) AND !outgoing([ETFs](out/etfs.md))
```
___
References:

Created:: 2021-08-11 13:53
