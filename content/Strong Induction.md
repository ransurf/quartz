Status: 
Tags: #archivedCards/macm101/induction 
Links: [[Mathematical Induction]]
___
# Strong Induction

Principles
?
- Easier to do than normal induction
-  If unsure which induction to use, use strong induction
- if p(i) is true for all i less than or equal to k then p(k+1) is true", where p(k) is some statement depending on the positive integer k
- Show that the statement [ P(1) ∧ P(2) ∧ … ∧ P(k) ] → P(k + 1) is true for all positive integers k
<!--SR:!2021-12-10,4,130-->

Steps
?
1. Prove initial steps, P(a), P(a+1), ... , P(b) is true
1. Assume P(i) for a<= i <= k
1. Prove P(k+1) using proven initial steps
<!--SR:!2021-12-10,7,166-->


## Examples
Two players take turns removing any positive number of matches they want from one of two piles of matches. The player who removes the last match wins the game. Show that if the two piles contain the same number of matches initially, then the second player can always guarantee a win.
?
- Let P(n) denote the statement `the second player wins when there are initially n matches in each pile`. 
- Basis step: P(1) is true, because in this case there is only one match in each pile, and the first player has only one choice, removing one match from one pile. 
	- Then the second player removes the match from the other pile and wins. 
- Inductive step: Suppose that P(j) is true for all j with 1 ≤ j ≤ k. 
	- We prove that P(k + 1) is true, that is, that the second player wins when each pile contain k + 1 matches. 
	- Suppose that the first player removes r matches from one pile leaving k + 1 – r matches there. 
	- By removing the same number of matches from the other pile the second player creates the situation of two piles with k + 1 – r matches in each. Apply the inductive hypothesis.
<!--SR:!2021-12-12,3,130-->

[Walkthrough on stack exchange](https://math.stackexchange.com/a/2355651)
## Practice
No. 1a, 2b (page 208)
No 3, 4a, 7b, page 244
___
# Backlinks
```dataview
list from [[Strong Induction]] AND !outgoing([[Strong Induction]])
```
___
References:

Created:: 2021-11-02 14:01
