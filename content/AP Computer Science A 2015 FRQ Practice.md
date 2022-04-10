Status:
Tags:
Links: [[AP Computer Science Study Progress]]
___
# AP Computer Science A 2015 FRQ Practice
## My Answers
```
1.
a)
int total = 0;
for (num:arr) {
	total+=num;
}
return total;

b)
int[] rowSumsArr = new int[arr2D.size()];
int i = 0;
for (arr:arr2D) {
	rowSumsArr.add(arraySum(arr));
	i++;
}
return rowSumsArr;

c)
int[] rowSumsArr = new int[arr2D.size()];
rowSumsArr = rowSums(arr2D);

for (int i=0; i<rowSumsArr.size()-1; i++) {
	for (int j=i+1; j<rowSumsArr.size(); j++) {
		if (rowSumsArr[i]==rowSumsArr[j]) {
			return false;
		}
	}
}
return true;

2.
a)
public class HiddenWord {
	private String word;
	
	public HiddenWord(String str) {
		word=str;
	}
	
	public String getHint(String guess) {
		String hint="";
		for (int i=0; i<guess.length(); i++) {
			if (word.substring(i, i+1).equals(guess.substring(i, i+1))) {
				hint+=word.substring(i, i+1);
			} else {
				String symbol = "*"
				for (letter:word) {
					if (guess.substring(i, i+1).equals(letter)) {
						symbol="+";
					} 
				}
				hint+=symbol;
			}
		}
		return hint;
	}
}
3.
a)
int val = 0;
for (sparse:entries) {
	if (sparse.getRow()==row && sparse.getCol()==col) {
		val=sparse.getValue();
	}
}
return val;

b)
numCols-=1;
for (int i=0; i<entries.size(); i++) {
	SparseArrayEntry s = entries.get(i);
	if (s.getCol()==col) {
		entries.remove(i);
	} else if (s.getCol()>col) {
		int row = s.getRow();
		int col = s.getCol();
		int val = s.getValue();
		entries.remove(i);
		entries.add(new SparseArrayEntry(row, col, val));
	}
}

4.
a)
interface NumberGroup {
	public boolean contains(int n) {
	}
}

b)
public class Range extends NumberGroup {
	private int[] nums;
	
	public Range(int min, int max) {
		nums = new int[];
		for (int i=min; min<max+1; i++) {
			nums.add(i);
		}
	}
}

c)
for (group:groupList) {
	for (val:nums) {
		if (val==num) {
			return true;
		}
	}
}
return false;
```
## Review
- Total 1:02 hours
- 1 took 2:38, 5:23, 6:18 | 2 took 12:37 | 3 took 9:22, 9:08 | 4 took 4:20, 7:04, 5:00
- 9, 9, 6, 7
- 31/36, 86 %
- Not bad
- 1.c they checked the values for the last object even though it isn't needed lmaoooo
- 2 their way is more convenient but w/e, my program should still do the job
	- They set the * as the else and used indexOf to see if it was in the rest of the array for the +
- 3.a Forgot to add declare type of object in for loop (SparseArrayEntry)
	- -1
- 3.b
	- Forgot to decrease col value of new entries by 1
		- -1 for not doing it, -1 for wrong final return
	- Could have just called get commands in the object creation parameters instead of storing them in values
- 4.a interface is declared public in example? And there is no prefix?
- 4.b Should be implements instead of extends
	- -1
	- I did it completely different in comparison to the question but I still did what it was asked
		- I feel like it was the question's fault for not specifying certain criteria and leaving the interpretation open ended
			- I guess in the future I should always implement the interface functions if im implementing an interface
				- If I get two numbers as the parameter I should probably have instance variables for them
- 4.c Should have known something was up when I didn't have any getters
	- You can't access the instance variables without gettersssssssssss
## Thoughts
- If you're using a method to set an array you don't need to set the size
	- implements are used for interfaces, extends are used for classes
		- Can only extend one class but can implement as many interfaces as you would like
- I've been able to grown accustomed to the split, I might change the top right key to += though as im not really sure about its current spot xddddddddddd
___
References: