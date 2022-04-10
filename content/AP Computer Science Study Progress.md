Links: [[AP]]

## April 5

-   2009 multiple choice, 35 questions in 41 mins
    

-   Got 26/34, 76%
    
-   Gotta brush up on sorting, and remember the little nitpicks of java
    
-   RECURSION NNNN
    

## April 6

-   44:30 minutes
    

-   8, 9, 12, 14.5 minutes respectively, 8, 5, 9, 7 points respectively
    

-   (1.b) Jan 1 returns 1, so there should have been a -1 to counteract it to make it work as intended
    

-   Gotta think about that stuff a bit more
    

-   (2) the thought of a variable for the number of days, including those that aren’t active
    

-   I should’ve picked up on it since the user was adding steps even if it wasn’t considered an active day
    

-   (4.a) forgot to assign the number of rows and columns for the 2d array
    
-   4.b) traversed the row given rather than column, used col as limit instead of the length of lights (lights\[0\].length)
    

-   rowLength = array.length;
    
-   colLength = array\[0\].length;
    

-   Not bad considering I hadn't touched the language in a while, #2 was scuffed since I forgot to consider an instance variable that should be recorded, which cost me 4 marks lmao. The concepts they ask are super easy, so I might just re-read the notes I took and then keep doing free response questions until I get 100%, then I'll do mcq until the week prior to the exam where I do free response questions every other day. Only problem is that there aren't many mcq practice questions :/
    

-   Daily frq until 100%
    
-   Do all the multiple choice I can find
    
-   Do at least 2 practice frqs before exam (6th, 7th)
    

## April 7

-   55 minutes
    

-   9.75, 11.3, 10.25, 23 respectively, 9, 5, 7, 3 respectively
    

-   24/36, 66% alaskdjflk;sajfsalk;fj
    

-   (2.a) I still need to initialize arraylists ( `arrayList = new ArrayList<Object>()` )
    

-   Faulty logic on storing pairs
    

-   First for loop should be -1 since the last string will be already included through previous iterations
    
-   Last loop should be i+1 to prevent duplicates
    

-   Forgot to create the word pair object to put in the arraylist lul
    
-   (3) Forgot to include “implements StringChecker”, forgot private prefix on instance variables
    
-   (4.a) Assumed that it was not necessary to declare the size of the arrays
    

-   Used array.add() which doesn’t even exist
    

-   Array\[r\] = array2D\[r\]\[c\];
    

-   (4.b) Used redundant code to find first row, when all i had to do was square\[0\]
    
-   Used square\[0\].length to find length of row, oops
    
-   I think I was being overconfident yesterday, should continue to keep doing practice frqs
    

-   Spend time reviewing CS notes before I take my next exam
   
## April 8
-   56 minutes
    

-   11, 6.5, 19, 20 mins respectively, 6, 9, 8, 8 points respectively
    
-   31/36 = 86%, with reference sheet would have been 33/36 = 91% :(
    

-   (1.a) Forgot to initialize instance variable in constructor again…
    

-   `digitList = new ArrayList<Integer>();`
    

-   Had incorrect parameter order for arrayList.add()
    

-   Index first, then item
    

-   (2) Nothing wrong, but when in doubt, implement it out
    
-   (3.a) Returned a value when the function was directly changing the instance variable lul
    

-   Shouldn’t happen if I pay attention to the function header
    

-   (4.a) forgot to include the row and column of a 2d array
    

-   I think I forgot to include it again when I transplanted my code
    

  

-   Not bad, I kind of want to be faster though
    
-   I’ll be sure to reference the reference sheet in future practices
    
-   Just gotta keep doing more practice quizzes to remember the little nitpicks of java
    
-   Remember to initialize instance variables in constructors
    
-   I think I'm gonna take a break from doing frqs for a week or two, and I can pick them up and start reviewing the book then since i still have a whole month before the test

## May 10
- [[AP Computer Science A 2016 FRQ Practice]]
## May 11
- [[AP Computer Science A 2015 FRQ Practice]]
## May 12
- [[AP Computer Science A 2014 FRQ Practice]]
## May 13
- [[AP Computer Science A 2013 FRQ Practice]]
## May 14
### Progress
- Spent some time doing mc AP CS questions on runestone textbook, 33/45 (73%) correct in 53 minutes
	- Finished part chap 3 question 15
	- Could be better if I used all my time efficiently
	- Gotta work on managing time since I won't be able to go back
		- Be so good I don't need it all
### Mistakes
#### C1
- combined for loops should be multipled
- arraylist should have Integer instead of int
- rushed guessing for the output of a loop
	- ended at length-1 but the loop printed the value of the counter+1 so it would have reached the end
- tricky and new array alteration question, I can see where I went wrong though
#### C2
- Forgot what a binary search was and how to calculate the amount of iterations needed
- Thought a while loop would be able to fill a 2d array lul
- misread comparison sign...
- got tricked by if else recursive
	- print only got called if no recursion, so only the end would be called
- Stupid click for demorgans law question, forgot to account for and/or conversion
#### C3
- Messed up an array altering line wtf
	- assumed set didnt remove previous value oops
- Lost with binary searching
	- Thought mid was a new int value, not the index spot
- you can't set instance variables of a super class without using constructor
## May 16
#### C4
- Weird instruction, two times a variable was set and it was asking for the one I didn't think of
- fibonacci wack
	- Bruh i could have just calculated it with my hand...
	- I was thinking of sums for some reason??????????
- Thought an answer was wrong because count increased before operation, but count wasnt even part of the operation...
- I need to go over subclasses in classes
- Decided to guess a bin search for some reason
- Trolling in recursive return checking
- Forgot about insertion sort
	- Goes by index to see if it can be moved
#### C5
- if there are no brackets, having the left of an or will result in true
- These questions need better wording ngl
	- Making me tilt and just guess
- Didn't bother to acknowledge the r\<c
- Yo they don't even know their exponent rules..
- If you call a super class method and the method called has a function in the object class, it will refer to that
- Forgot to run loop one more tiome emememem
- Messed up substring thing
## May 17
- [[Barron's APCS Practice Test 1]]