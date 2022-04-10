---
title: Partial Fraction Decomposition
---
Status:
Tags: #math/calculus/integrals 
Links: [Integrals of Rational Functions](out/integrals-of-rational-functions.md)
___
# Partial Fraction Decomposition
 > Used for turning rational functions with factorable denominators as sum/differences of multiple rational fractions with linear or quadratic denominators
> - Opposite of finding a LCD
## Steps
1. Use polynomial long division if possible
2. Completely factor the denominator only
	- If not factorable, you must use the other methods
3. Use a table to determine the term(s) of use in decomposition for each factor
	- Replace factors with PF terms
	- A,B, etc, are unknown values
- | Denominator Factor           | Term in PF                         |
| ---------------------------- | ---------------------------------- |
| Linear: ax+b                 | A/ax+b                             |
| Repeated linear: (ax+b)^2    | A/ax+b + B/ax+b...                 |
| Quadratic: ax^2+bx+c         | Ax+B/ax^2+bx+c                     |
| Repeated quad: (ax^2+bx+c)^2 | Ax+B/ax^2+bx+c + Cx+D/ax^2+bx+c... |
4. Set rational function equal to partial fractions
	- Remember to add all multiples of the denominator (x-1), (x-1)^2
		- Numerator is dependent on the bracket interior
1. Multiply by the denominator to eliminate fractions
2. Use "cover-up" method or "expand and compare" method to determine the value of A,B,C, etc
	- [Partial Fraction Cover-Up Method](out/partial-fraction-cover-up-method.md)
	- Expand and Compare
		- Distribute uppercase variables to factors
		- Variables must combine to equal the appropriate coefficients of the initial numerator
3. Rewrite rational function as sum/difference of partial fractions using values of A,B,C, etc
## Anki
START
Cloze
Partial Fraction:
2. Set rational function equal to {partial fractions}
	- $x+a$ is over A
	- $x^2+a$ is over Ax+B
	- Remember to add all multiples of the denominator ex) $(x-1), (x-1)^2$
		- Numerator is dependent on the {bracket interior}
3. Multiply by {the denominator} to eliminate fractions
4. Solve for a certain variable by choosing an x value that {cancels other factors}
5. If unable to find an x value to isolate a constant, pick an appropriate number and {plug in the values of the known constants}
	- Can continue testing values to form a linear system
Back:
DECK: IntegralCalculus
Tags: RationalIntegrals
<!--ID: 1623789433571-->
END
## Practice
[Section E and F and G](None)
___
References:

Created:: 2021-06-12 14:59