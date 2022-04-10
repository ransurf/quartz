Status:
Tags:
Links: [[AP Computer Science Study Progress]]
___
# AP Computer Science A 2013 FRQ Practice
## Code
```
1.
a)
for (DownloadInfo song : downloadList) {
	if (song.getTitle().equals(title)) {
		return song;
	}
}
return null;

b)

for (String title : titles) {
	if (getDownloadInfo(title) != null) {
		getDownloadInfo(title).incrementTimesDownloaded();
	} else {
		downloadList.add(new DownloadInfo(title));
	}
}

2.
a)
board = new int[playerCount];
int i = 0;
while (i<board.size()) {
	board[i] = (int) (Math.random() * 9) + 1;
	i++;
}
currentPlayer = (int) (Math.random() * (playerCount-1);

b)
int numTokens = board[currentPlayer];
board[currentPlayer] = 0;
int i = currentPlayer;
while (numTokens > 0) {
	if (i=board.size()-1) {
		i = 0;
	} else {
		i++;
	}
	board[i] += 1;
	numTokens--;
}

3. GridWorld

4.
a)
view = new double[numRows][numCols];
for (val:scanned) {
	for (int r=0; r<numRows; r++) {
		boolean isBackwards = (r%2)==1;
		int bCol = numCols-1;
		for int c=0; c<numCols; c++) {
			if (!isBackwards){
				view[r][c] = val;
			} else {
				view[row][bCol] = val;
				bCol--;
			}
		}
	}
}

b)
double sum = 0;
int numViews = 0;
for (int r=startRow; r<=endRow; r++) {
	for (int c=startCol; c<=endCol; c++) {
		sum += view[r][c];
		numViews++;
	}
}
return sum/numViews;
```
## Review
- 43:44 total, 25/27 | 92.5% | 5
- 1 took 3, 12:40 | 2 took 7, 5 | 4 took 12:30, 3
- 9, 7, 9 respectively
- 2.a Should be `Math.random() * 10 + 1`
	- I can use normal for loops instead of while loops and would still be able to access different  indexes
	- Range of `Math.random() * 10` would be 0-9.999, and the int would truncate it to 0-9
		- Hence the + 1
			- If only I hadn't mainly used randInt previously smh
				- -1
	- Messed up calculation for currentPlayer too
		- 1
- 2.b they used % instead of resetting value
	- Used variable `nextPlayer` instead of `i`
- 4.a
	- They had an if statement to check my equivalent of `isBackwards` and then had a for loop for it
		- Backwards for loop is `for (int i = size-1; i>=0; i--)`
	- Just used an index for `scanned` instead of for since the row and col for loops restrict boundaries
## Thoughts
- Nice to understand Math.random() finally
- My solutions are unorthodox but they work sooo
	- At least I'm knowledgeable enough of my tools to create abstract solutions
___
References: