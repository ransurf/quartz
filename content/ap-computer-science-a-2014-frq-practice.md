---
title: AP Computer Science A 2014 FRQ Practice
---
Status:
Tags:
Links: [AP Computer Science Study Progress](out/ap-computer-science-study-progress.md)
___
# AP Computer Science A 2014 FRQ Practice
## Code
```
1.
a)
int i = 0;
String scrambled = word;
while (i<word.length()-1) {
	if (word[i].equals("A") {
		scrambled[i]=word[i+1];
		scrambled[i+1]=word[i];
	}
	i++;
}
return scrambled;

b)
int i = 0;
while (i<wordList.size()) {
	String word = wordList.remove(i);
	String scrambled = scrambleWord(word);
	
	if (!(word.equals("scrambled")) {
		wordList.add(scrambled);
	}
	i++;
}
2. GridWorld

3.
a)
public SeatingChart(List<Student> studentList, int rows, int cols) {
	int i = 0;
	seats = new Student[rows][cols];
	for (int c=0; c<cols; c++) {
		for (int r=0; r<rows; r++) {
			if (i<studentList.size()) {
				seats[r][c] = studentList.get(i);
			}
			i++;
		}
	}
}
b)
int numRemoved = 0;
for (int r=0; r<seats.length(); r++) {
	for (int c=0; c<seats[0].length(); c++) {
		Student s = seats[r][c];
		if (s.getAbsenceCount()>allowedAbsences) {
			seats[r][c]=null;
			numRemoved++;
		}
	}
}

return numRemoved;

4.a)

public class Trio implements MenuItem {
	private String name;
	private double price;
	
	public Trio(Sandwich sndwch, Salad sld, Drink drnk) {
		name = sndwch.getName() + "//" + sld.getName() + "//" + drnk.getName() + " 									Trio";

		if (drnk.getName().equals("Cappuccino")) {
			price = 6.25;
		} else {
			price = 4.00;
		}
	}
	
	public String getName() {
		return name;
	}
	
	public double getPrice() {
		return price;
	}
}
```
## Review
- 1 took 7:33, 5:27, 2 took 8:31, 5:42, 4 took 14:33
- 6, 8, 7
- 21/27, 77%
	- Still 5
- 1.a used wrong syntax for substrings lmao
	- -3
- 3.b) Forgot to do null check for empty seats
- -1
- 4. Misinterpreted the example items to be the absolute items so I did a lazy way of coding the program
	- Should have stuck to doing comparisons to see which were the two most expensive objects
		- -2
## Thoughts
- Me using the wrong syntax for string really costed me marks
- I guess next time I should do things the fail-proof way
- Did not think at all about null checks on the 2nd question bruh
___
References: