Status: 
Tags: #archivedCards/cmpt125/bigo 
Links: [[Big O Notation]]
___
# Big O Notation Definition

## Principles
?
- Way of measuring the time complexity (running time) of algorithms
- Denoted by f(N), running time for inputs of size N
- **Formally:** Let f(N) and g(N) be two functions on positive integers.​  
We say that f = O(g) if there exists a large enough constant C (e.g. C = 1000) such that **f(N) <=  C* g(N)** for all sufficiently large N.​
- Alternatively, f = O(g) if limsup(n->infinity) of f(N)/g(N) < infinity
<!--SR:!2021-12-19,6,210-->

## Examples

Let f(N)  = 1.5N2 + 4N+ 3. Prove that f(N) = O(N3)​
?
Proof: Let C = 9. We want to prove that f(N) < $CN^3$ for all N >= 1.​
- Indeed, f(N) = $1.5N^2$ + 4N + 3 **<**  $1.5N^3$ + $4N^3$ + $3N^3$ **<** $9N^3$
- Therefore f = $O(N^3)$
- Upsize everything, add coefficients, compare and mulitplicate constants, focuses on highest n
	- ex) f(N)  = $2N^4$ + $10N^3$ would be O($N^4$)
	- Constants matter in practice but not theory
<!--SR:!2021-11-05,13,290-->

Example: Show f is not O(N)
?
1. f(N) > CN for all N large enough
2. Try c = 100; for all N>100, f(N) > 1.5 x 100 x N > CN
3. At lim f(N)/g(N) > $1.5N^2/{N}$ = 1.5N -> Infinity
<!--SR:!2021-12-26,11,230-->


___
# Backlinks
```dataview
list from [[Big O Notation Definition]] AND !outgoing([[Big O Notation Definition]])
```
___
References:

Created:: 2021-10-18 21:31
