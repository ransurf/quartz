---
title: AP Computer Science A 2016 FRQ Practice
---
Status:
Tags:
Links: [AP Computer Science Study Progress](out/ap-computer-science-study-progress.md)
___
# AP Computer Science A 2016 FRQ Practice
## My Answers 
```
1. 
a)
public class RandomStringChooser {
	private String[] wordArray;
	
	public RandomStringChooser(String[] words) {
		wordArray = words;
	}
	
	public String getNext() {
		if (wordArray.size()==0) {
			return "NONE";
		}
		int i = (Math.random()*wordArray.size()) - 1;
		result = wordArray[i];
		wordArray.remove(i);
		return result;
	}
}

b)
public RandomLetterChooser(String str) {
	String[] letterArray = getSingleLetters(str);
	if (letterArray.size()==0) {
			return "NONE";
		}	
	int i = (Math.random()*letterArray.size()) - 1;
		result = letterArray[i];
		letterArray.remove(i);
		return result;
}

2.
a)
machineId = message.substring(0, message.indexOf(":"));
description = message.substring(message.indexOf(":")+1);

b)
int i = description.indexOf("keyword");
if (i==-1) {
	return false;
}
if (!(i==0 || description.substring(i-1, i).equals(" ")) {
	return false;
}
else if (!(i==description.length()-keyword.length() || description.substring(i+keyword.length(), i+keyword.length()+1).equals(" "))) {
	return false;
}
return true;

c) 
List<LogMessage> list = messageList;
for (message : list) {
	description = message.getDescription();
	int i = 0;
	if (description.containsWord(keyword)) {
		list.remove(i);
	} else {
		i++;
	}
}
return list;

3.
a)
boolean result1 = false;
boolean result2 = false;
if (blackSquares[r][c]==false) {
	result1 = true;
}
if ((c==0 || puzzle[r-1][c]==0) || (r==0 || puzzle[r][c-1]==0)) {
	result2 = true;
}
return result1 && result2;

b)
int rows = blackSquares.size();
int columns = blackSquares[0].length;
puzzle = Square[rows][columns];
int num = 1;
for (int r=0; r<rows; r++) {
	for(int c=0;c<columns;c++) {
		if (toBeLabelled(r, c, blackSquares)) {
			Square sq = new Square(blacksquares[r][c], num);
			num++;
		} else {
			Square sq = new Square(blacksquares[r][c], 0);
		}
		puzzle[r][c] = sq;
	}
}

4.
a)
int total = 0;
for (word:wordList) {
	for (int i=0;i<word.length();i++) {
		num++;
	}
}
return num;

b)
int totalGapWidth = formattedLen-totalLetters(wordList);
return totalGapWidth/(wordList.size()-1);

c)
String result = "";
int numExtraSpaces = leftoverSpaces(wordList, formattedLen);
int spacesLeft = wordList.size()-1;
String space = "";
for (int i=0;i<basicGapWidth(wordList, formattedLen);i++) {
			space+=" ";
	}
for(word:wordList) {
	for (int i=0;i<word.length();i++) {
			result+=word[i];
	}
	if (numExtraSpaces>0) {
		result+=" ";	
	}
	if (spacesLeft>0) {
		result+=space;
	}
}
return result;

```
## Review
- Total 1:37 hours
- 1 took 14.5, 6, 5 mins | 2 took 13.5, 12, 12 mins | 3 took 12, 6 mins | 4 took 4.5, 11 mins
- 6, 5, 9, 9
- 29/36, 80% which would be a 5
- 1.a forgot to initialize words variable, incorrect method of transferring values
	- `words = new ArrayList<String>()`
	- use a for loop to add every word in wordArray to words
		- -1
	- Forgot to typecast
		- -1
	- they just returned remove
- 1.b i remade the program instead of using super LMAO
	- It still works, but they wanted u to use super
	- -1
- 2.c i cant just set an arraylist as another arraylist lmao
	- they added the logmessage into the
	- -4, -2 if they allow my scuffed method
- 2.b they set default as true and had it return true for every possible occurence
	- -1 for out of bounds error
- 4.c Could be more efficient
	- Instead of adding each letter individually I can just add the whole word lul
## Thoughts
- Idk if I wanna use the split keyboard for coding seeing as my test is in a week and having to use it severely impacted my typing speeds
	- Why is the + and = in such a wack spot xddd
- READ UP NOTES ON ARRAYLISTS AND LISTS...
	- Don't forget about using super
	- TIL list.remove() returns something
	- Arraylists don't have set lengths
- Huge comeback for the final questions lmao
___
References:

