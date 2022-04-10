---
title: MACM101 Assignments
---
Status: 
Tags: 
Links: [notes/) MACM 101 - Discrete Mathematics I](None)
___
# MACM101 Assignments
## [Assignment 10](https://canvas.sfu.ca/courses/66056/files/17753314?wrap=1)
- [7](https://math.stackexchange.com/questions/2475298/prove-that-2n-1-is-divisible-by-3-for-all-positive-integers-n)
- 
## [Assignment 9](https://canvas.sfu.ca/courses/66056/files/17665680?wrap=1)
### 7
https://math.stackexchange.com/questions/1926378/prove-the-identity-sum-i-0n-n-choose-i-i-n2n-1-using-combinatori?noredirect=1&lq=1
### 9
 [![Image from Gyazo](https://i.gyazo.com/1d599d5f6f10e719082f62d01fefe9a9.png)](https://gyazo.com/1d599d5f6f10e719082f62d01fefe9a9)
## [Assignment 8](https://canvas.sfu.ca/courses/66056/files?preview=17581507)

[6](https://courses.engr.illinois.edu/cs173/fa2011/Homework/hw7-solutions.pdf) | [7](https://math.stackexchange.com/questions/1008654/solving-a-question-about-fibonacci-and-lucas-numbers-using-induction)
Harmonic numbers:
[![Image from Gyazo](https://i.gyazo.com/2663d6d7ce9207ee0feb695e53c3f473.png)](https://gyazo.com/2663d6d7ce9207ee0feb695e53c3f473)

- 4
	- yea, by assuming the statement is true for all i in the range of 1 <= i <= k
	- when you go to verify P(k+1), 1 <= ⌊(k+1)/2⌋ <= k
	- so then lets set ⌊(k+1)/2⌋ = i
	- and as you know C_i <= 4(i-1)^2 by the inductive hypothesis
	- at least that's what i did
	- cuz tbh I dont know if anything that im doing is actually correct
	- from there you can expand

	- Well think about it
	- By the inductive hypothesis, we made i <= k
	- And think
	- What is C_(k+1) less than
	- And what is C_i less than
	- That's pretty much all I can give without basically giving away the answer

 - i have no idea if i did it right but what i did was replace the C(k+1) with the definition of C terms and used 1/2*k +1/2 as the subscript on that
    - and then when i used the inductive hypothesis i just used the fractions

- 8
	- Let the Chomp board have n rows and n columns. We claim that the first player can win the game by making the first move to leave just the top row and left-most column. (He does this by selecting the cookie in the second column of the second row.) Let P(n) be the statement that if a player has presented his opponent with a Chomp configuration consisting of just n cookies in the top row and n cookies in the left-most column (both of these including the poisoned cookie in the upper left corner), then he can win the game. We will prove \/nP(n) by strong induction. We know that P(l) is true, because the opponent is forced to take the poisoned cookie at his first turn. Fix k 2 1 and assume that P(j) is true for all j :=:; k. We claim that P(k + 1) is true. It is the opponent's turn to move. If she picks the poisoned cookie, then the game is over and she loses. Otherwise, assume that she picks the cookie in the top row in column j, or the cookie in the left column in row j, for some j with 2 :=:; j :=:; k + 1. The first player now picks the cookie in the left column in row j, or the cookie in the top row in column j, respectively. This leaves the position covered by P(j - 1) for his opponent, so by the inductive hypothesis, he can win.
## [Assignment 7](https://canvas.sfu.ca/courses/66056/files/17512611?wrap=1)
## [Assignment 6](https://canvas.sfu.ca/courses/66056/files?preview=17436167)
## [Assignment 5](https://canvas.sfu.ca/courses/66056/files/17360020?wrap=1)
- 6
	- The set B is empty. Indeed, if B 6= ∅, say, a ∈ B, then either a ∈ A or a 6∈ A. In the first case a ∈ A ∩ B implying a 6∈ A 4 B and A 4 B 6= A. In the second case a ∈ A 4 B, but a 6∈ A. Again, we get A 4 B 6= A.
- Forgot to prove 8, thought it meant prove by using diagram
## [Assignment 4](https://canvas.sfu.ca/courses/66056/files?preview=17294643)
## [Assignment 3](https://canvas.sfu.ca/courses/66056/files/17173248?wrap=1)
###### Comparison
1
- b) even? where did z come from

2
- b) Our answers are the same right? according to slide 7-13 at least
- c) I think the two quantifiers are swapped since "everybody" is the one doing the fooling, so they would be x
- d) which one is ur answer wut? also do you sure on whether we are supposed to introduce quantifiers for things like nancy and fred cuz i have no clue xd
- e) still unsure on how to introduce quantifiers for people, also it says exactly so you need !

4
- b) do you know if we're supposed to prove/explain why?

5
- i think you should also probably include the one person right?

6
- a) I think the question wants us to have our answer in the "if, then structure"
	- Do you think we can just denote the positive integer thing as a universe or do we have to have the predicate?


___
###### Answers
# Backlinks
```dataview
list from [MACM101 Assignments](out/macm101-assignments.md) AND !outgoing([MACM101 Assignments](out/macm101-assignments.md))
```
___
References:

Created:: 2021-10-04 22:11
