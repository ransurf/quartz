---
aliases:
---
Status:
Tags: #cards/math232/unit1
Links: [[Math 232 Course Outline]]
___

# Linear Independence

## Principles
?
- [![Image from Gyazo](https://i.gyazo.com/e5e5bd5963c93173fd058c4867bb3586.png)](https://gyazo.com/e5e5bd5963c93173fd058c4867bb3586)
- Isolalte one, solve for other using newly found
- Otherwise, it is linearly dependent
### Graphed
[![Image from Gyazo](https://i.gyazo.com/59dd89956e94fcc5f01d27241f1e8c2e.png)](https://gyazo.com/59dd89956e94fcc5f01d27241f1e8c2e)
[![Image from Gyazo](https://i.gyazo.com/f35857a664db830ec9945e90438297cb.png)](https://gyazo.com/f35857a664db830ec9945e90438297cb)
<!--SR:!2022-03-26,23,170-->


### Checking
- For 2 vectors, check if multiple
- For sets with 3+ vectors, see if it is possible to combine 2+ to create the rest
	- Can also apply constants, set to 0, then isolate a variable and work way up to see if it is possible to find a value for all of them under one specific case

{v1, v2} are linearly dependent if and only if ;; v1 and v2 are parallel
<!--SR:!2022-02-12,2,178-->
{v1, v2, v3} are linearly dependent if and only if ;; v1, v2, v3 lie in the same plane.
<!--SR:!2022-02-12,2,178-->

Check linear independence of using matrix
?
- Each vector as a column, find solution other than 0

Check if s is linearly independent
[![Image from Gyazo](https://i.gyazo.com/39697b3c392f8fb35b2186c6b5afcfb4.png)](https://gyazo.com/39697b3c392f8fb35b2186c6b5afcfb4)
?
[![Image from Gyazo](https://i.gyazo.com/9baf869d3168c6b3c866c11db8e64ac6.png)](https://gyazo.com/9baf869d3168c6b3c866c11db8e64ac6)
- Last column shows us that m4 = m1+m2+m3

## Theorems
A set S with two or more vectors in Rn is linearly dependent if and only if at least one of the vectors in S is expressible as a linear combination of the other vectors in S.
?
- Prove both ways
- [![Image from Gyazo](https://i.gyazo.com/a3313ef92282417ce83bf67bf4eeceda.png)](https://gyazo.com/a3313ef92282417ce83bf67bf4eeceda)
- [![Image from Gyazo](https://i.gyazo.com/58a859fe38db5d8b49dc5315fa9d5b71.png)](https://gyazo.com/58a859fe38db5d8b49dc5315fa9d5b71)
	- There must be some other constant that negates the 1
<!--SR:!2022-02-13,2,150-->

## Examples
### Properties
Are the following sets linearly independent?
- (a) S = {(1, 0, 0),(0, 0, 1)}
- (b) S = {(0, 1, 0),(0, 3, 0)}
?
- a) Independent since no coefficient on one point can be applied to equal the other point
- b) Dependent since 2nd point can be multipled by 1/3 to be the same as the first point
<!--SR:!2022-05-01,59,210-->

Suppose u and v are non-zero vectors. Are the following sets linearly independent?
- (a) {u}
- (b) {u, v, 0}
?
- a) Yes only if u != 0, since if it were 0 then any coefficient would lead to 0
- b) No since any number could be applied as $c_3$, making it non linearly independent
	- If there is a zero vector in a collection, it is dependent
<!--SR:!2022-02-17,10,190-->

### Checking Linear Independence
Are the vectors (5, 4),(−1, 6) linearly independent?
?
- Yes
- Apply rule, isolate one variable and plug into other eqn
[![Image from Gyazo](https://i.gyazo.com/8250db542b4125e1db18d719637f6501.png)](https://gyazo.com/8250db542b4125e1db18d719637f6501)
<!--SR:!2022-04-23,51,198-->

Are the vectors (1, 0, 1),(−1, 0, 1),(2, 0, 2) linearly independent? What do the vectors span?
?
- Not linearly independent
- Use system of elimination to isolate one and plug into others
	- [![Image from Gyazo](https://i.gyazo.com/e719bc1e39773ddac3a435a8fe103070.png)](https://gyazo.com/e719bc1e39773ddac3a435a8fe103070)
- [![Image from Gyazo](https://i.gyazo.com/cd96c4470d885453209103c882bd4de3.png)](https://gyazo.com/cd96c4470d885453209103c882bd4de3)
	- Set one of the variables to anything, then find out what the other variable should be
		- Variables are not all 0, but statement is still true, so not linear independent
- Span can be reduced to  {(1 0 1), (-1 0 1)} since (2 0 2) is multiple of (1 0 1)
- [![Image from Gyazo](https://i.gyazo.com/a130d9478b3bf72b14e335342782d689.png)](https://gyazo.com/a130d9478b3bf72b14e335342782d689)
<!--SR:!2022-04-26,54,190-->

Express vector a as a linear combination other vectors B and C
?
- A = t(B) + s(C) for some values t and s
___
<!--SR:!2022-02-12,2,178-->

# Backlinks
```dataview
list from [[Linear Independence and Dependence]] AND !outgoing([[Linear Independence and Dependence]])
```
___
References:

Created:: 2022-01-11 20:12
