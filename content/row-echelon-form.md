---
title: Row Echelon Form
aliases: gaussian elmination
---
Status:
Tags: #cards/math232/unit2
Links: [Augmented Matrix](out/augmented-matrix.md)
___

# Row Echelon Form
![Pasted image 20220121235258.png](None)

## Principles
- Can't use changed ones in the same step
- Focus on setting zeros under before moving on

Style of [Augmented Matrix](out/augmented-matrix.md) with the following properties
?
- Reduced using gaussian elimination
- Each row either consist of all zeros, or has a 1 as first non-zero entry (leading 1)
- Any rows of all zeros are grouped together at the bottom of matrix
- In two successive nonzero rows, the leading 1 in the lower row is to the right of the leading 1 in the upper row
- [![Image from Gyazo](https://i.gyazo.com/7d5b35e2dfc99c9e7bccad3262cfe805.png)](https://gyazo.com/7d5b35e2dfc99c9e7bccad3262cfe805)
<!--SR:!2022-03-11,29,190-->

[Free variables](out/free-variables.md) are when the column has no leading
- lead variables depend on [Free variables](out/free-variables.md)

## Examples
Solution set of
[![Image from Gyazo](https://i.gyazo.com/ec81238108185627605eb79421341a05.png)](https://gyazo.com/ec81238108185627605eb79421341a05)
?
None since 0=1 for the last one
<!--SR:!2022-02-19,9,150-->

Solution set of
[![Image from Gyazo](https://i.gyazo.com/08a477ce66336759d1239991084dc603.png)](https://gyazo.com/08a477ce66336759d1239991084dc603)
?
[![Image from Gyazo](https://i.gyazo.com/fe7c18d6e824ef65bd2c55d675e27f81.png)](https://gyazo.com/fe7c18d6e824ef65bd2c55d675e27f81)
- Choose the free, find leading, state point
- turn free into letter var
<!--SR:!2022-02-18,8,130-->

[![Image from Gyazo](https://i.gyazo.com/c2b5d3b1330270e5447bd3a9adda069b.png)](https://gyazo.com/c2b5d3b1330270e5447bd3a9adda069b)

___

# Backlinks
```dataview
list from [Row Echelon Form](out/row-echelon-form.md) AND !outgoing([Row Echelon Form](out/row-echelon-form.md))
```
___
References:

Created:: 2022-01-19 18:33
