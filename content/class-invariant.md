---
title: Class Invariant
---
Status: 
Tags: 
Links: [C++ MOC](out/c-moc.md)
___
# Class Invariant
## Principles
Conditions that must always be held for a class
1.  Condition on a function argument is that, it should always be > 0 (greater than zero) or should not be null.
2.  Minimum_account_balance property of an account class states, it cannot go below 100. So all public functions should respect this condition and ensure class invariant.
3.  Rule based dependency between variables, that is, the value of one variable depends on another, so if one changes, using some fix-rule, the other must also change. This relationship between 2 variables must be preserved. If it does not, then invariant is violated.
___
# Backlinks
```dataview
list from [Class Invariant](out/class-invariant.md) AND !outgoing([Class Invariant](out/class-invariant.md))
```
___
References:

Created:: 2022-01-22 15:52
