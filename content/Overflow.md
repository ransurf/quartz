---
title: Overflow
---
Status:
Tags:
Links: [Binary](out/binary.md)
___
# Overflow
Since integers can only hold x amount of bits, an overflow will occur when the calculated answer holds more than it's total capacity
- As a result, it truncates the value to fit inside the variable
	- ex) 9999 goes to 0000 on a pokewalker, where the 1 is disregarded

If 2 Two's Complement numbers are added, and they both have the same sign (both positive or both negative), then overflow occurs **if and only if the result has the opposite sign**. Overflow never occurs when adding operands with different signs.

___
References: