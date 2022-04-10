---
title: Two Operand Arithmetic Instructions
aliases:
---
Status:
Tags: #cards/cmpt295/assembly
Links: [x86-64 Assembly](out/x86-64-assembly.md)
___

# Two Operand Artihmetic Instructions

## Principles
- Destination and first operand are the same
- mem <- mem OP mem usually not supported
- We use ATT format, not intel format

## Types

### add\*
syntax, meaning/effect/examples
?
Syntax : add\* src, dest
Meaning/Effect : Dest <- Dest + Src
Examples : addq *%rax*, **%rcx**, **x** += *y*
<!--SR:!2022-04-16,30,150-->

### sub\*
syntax, meaning/effect/examples
?
Syntax : sub\* src, dest
Meaning/Effect : Dest <- Dest - Src
Examples : subq *%rax*, **%rcx**, **x** -= *y*
<!--SR:!2022-04-15,29,150-->

### imul\*
syntax, meaning/effect/examples
?
Syntax: imul\* src, dest
Meaning: Dest <- Dest \* Src
Examples: imulq $16, (*%rax*, **%rdx**, 8) **x** \*= *y*
___
<!--SR:!2022-04-08,22,130-->

# Backlinks
```dataview
list from [Two Operand Artihmetic Instructions](None) AND !outgoing([Two Operand Artihmetic Instructions](None))
```
___
References:

Created:: 2022-02-05 00:24
