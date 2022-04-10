**

# 2 Player Chess Python Major Project

### Assignment Description

The final part of the project is to create a video based presentation of your project. In this presentation, you will outline your entire project from the first task through to the end product. The method in which you do this and the software to use is up to you, however, you must have the following in the video:

-   Explanation/Rationale for choosing the product you chose.
    
-   Description and run through of your problem-solving strategies.
    
-   Demonstration of your final game, play the game with narration.
    
-   Details of the code, line by line/section by section. Including what that line/section does, discussing the coding concepts used.
    
-   Discuss how your project changed over the course of the project. 
    
-   Include any difficulties and celebrations you encountered throughout the project.
    

### Introduction/Explanation

What was once seen as a complex game only for the analytical-minded has suddenly risen in popularity in mainstream media. Famous online personalities and renowned chess players have been pumping out chess-related content and have been competing in various tournaments online for hundreds of thousands of people to watch. Despite this sudden upbringing of the game, my interest began a few years prior, back when my cousin first challenged me to a chess game with his brand-new chess board. What started as an innocent hobby spiraled into countless hours sunk into watching professional matches, learning new strategies, and placing bets on matches. I decided to make a chess program to pay homage to the memorable experiences the game has created in my life, and to challenge myself and see if I could truly build such a complex program to finish off the class.

  

Without further ado, I’d like to share my  journey towards building a chess program in python.

### To-Do List

\-Make squares buttons and have pieces as images

### Description

\-Make board

\-Make classes for pieces

\-Only allow legal piece moves

\-Determine where they can go based off position

\-Prevent pieces from moving through other pieces

\-Prevent pieces from eating their own pieces

\-Castling

\-Promotion

\-Winning

  

Qualification

I’ve only worked with python for around maybe 2 months, so the jump in difficulty I’m going to experience by trying to make this program will be excruciating.  With my previous hardest programs being a hangman game and an account information storage, both with very basic GUI, this program will probably require me to spend countless hours learning new concepts, painstaking troubleshooting, and having no clue on what to do.

With my current basic understanding of Tkinter and Class fundamentals, coding this program will definitely help me further understand such concepts and prepare myself for the challenges that will await in university.

  

### Progress

Jan 10, 2021

First things first, I searched online to see the GUI’s of other people’s chess programs. After some browsing, I decided to work towards having a board and pieces, nothing more, nothing less.

  

It didn’t take too long to encounter my first problem, which was creating the board.

  

Jan 11th, 2021

After learning about frames and using tkinter commands in loops and functions, I was able to create an 8x8 checkerboard with each square as a button.

A tough decision I had to make was to think of how the players would choose what pieces to move, and how I would move the pieces. I came up with two options: I could have the buttons I made store the images of the pieces and be the player’s method of selecting pieces, or I could track their cursor location and clicks to find out what pieces they have selected, and move pictures of pieces to different coordinates depending on their move.

I figured buttons were easier since the player(s) then could use the button as an input rather than have to check cursor location in relation to a window. Furthermore, I could also attach the images of the pieces onto the button and change it as I please.

  

Jan 12th, 2021

Today, I planned to create dictionaries that would help the program arrange the starting positions of all pieces. After 2 hours, I managed to upload the pictures onto the program, but when I tried applying it to the buttons, they just shrank, didn’t respond when clicked, and didn’t even display the picture! I decided to just take a break, and work on it the next day.

  

Jan 13th 2021

I had to study for and take a math test as well as study for finals, so I wanted to take a break for this day.

  

Jan 14th 2021

After searching around on Stack Overflow, I managed to find my solution: after setting the config of the button, I also needed to set the image of the button to the picture (yeah I don’t really get it but it works!). Now I just need to think of an efficient way to set each button with the correct image, and then I can finally get into the fun stuff: movement and the actual game itself :D

By the end of the day, I was able to place all the pieces on the board.

  

Jan 15th 2020

I managed to only allow pieces to move if their desired square was allowed by their moveset, the only problem is that they can move wherever and can even self-destruct… hmm.

To counteract this, I made a function that would check whether the move would be valid and made use of an if-statement depending on the piece to see if the location they were trying to move to would be possible regarding their movement.

  

Jan 16th 2021

I kind of realized that I neglected the movement of black pieces in my code from yesterday, so I quickly fixed that. I then went on to finishing the movement restrictions for the bishop, knight, and queen.

  

Next, I kept track of the amount of turns, and used that variable to determine whose turn it was (I gave white the option to move during even-number turns, and black for odd-number turns). From there, I placed an if statement before the whole piece-movement process to make sure that these regulations took place.

  

Jan 17th 2021

I quickly went and allowed pawns to capture opposing pieces on the diagonals, which wasn’t too hard. Next, I began working on further improving the piece movement by creating a function that checked to see whether a piece's destination already had a piece with its own color, and prevented the move from happening if there was.

  

Now, it was time to prevent pieces from jumping across hella pieces, just like this.

I had already managed to prevent pieces from moving if their destination had a piece of their own color already on the square, but I have nothing to check for their trip to that square since the piece just teleports. As tedious as it may sound, I was thinking of creating a for loop that would check the squares in between each square. If I had made the pieces their own individual objects I could have easily calculated this, but if I were to change that I would have to rework almost all my code. 

  

After a few minutes of troubleshooting, I managed to implement my previous idea into my code. I’ve only done it with the rook’s vertical movement since calculating loops for straight movements would be easier than diagonal movements like the bishops, so now I just need to find out how to do the latter.

  

By the end of my coding session, I managed to fix the movement of the rook. Since the knight can jump, the king can only move one square, and pawn movement has already been set, I’ll just have the queen’s and bishop’s movement to restrict, and after that, movement should be completely finished!

  

Jan 18th 2021

I struggled a lot on trying to check the squares of the diagonals, but after my entire work period for today, I managed to solve it! I ended up creating 4 versions of checking, depending on whether it was travelling NW, NE, SW, or SE. From then, I would set the x and y values accordingly, and would increase the file and rank values at the same time to incorporate the diagonal checking. Initially I used a for loop to check x and y, but that ended up making the program check more than y values for every x value.

  

Now, all that’s left is promotion, castling, and the check system!

  

Castling

\-check to see if rook has moved through turning on boolean in rook movement

\-check to see if king has moved through turning on boolean in king movement

\-work on not allowing castle when path is under check after working on check

  

Promotion

\-when wp reaches rank 8 or bp reaches rank 1, menu will pop up asking what piece they want to convert it into

\-gonna be a separate method, shouldn’t be too hard though

\-could check if pawn is going to rank 8 after moved

  

Check

\-check to see whether king is in check by seeing if every piece of other opponents could travel to that space in the next move

  

Jan 19th 2021

I spent around 30 minutes on the promotion menu, but just wanted to relax for the day; I had an integral test today, a chem test thursday, and have been doing this daily for over a week.

  

Jan 20th 2021

I managed to have the piece changed to the corresponding button that was clicked, but for some reason players weren’t allowed to move their pieces after. I tried destroying the main loop, but what worked was making the select piece function nested in the promotion menu function, which allowed me to delete the promo root. With that done, all I need to do is castling and the check system! (And make this video that you’re watching, of course)

  

Jan 21st 2021

And so the quest to get a properly-working check system began…

Luckily, I was able to utilize my previous methods of determining whether a piece was able to move to the desired square; to see if the king was in check, I iterated through all the squares, checking the opposite colored pieces to see if they were able to attack the king. 

\-there was a bit of confusion with replacing the pictures and knowing when to initiate the check, but after some trial and error I was able to sort it out. Since both the squares selected by the players and the movement system used the same variables, running the movement system to look for checks would replace the user’s selections and not run as intended. To combat this, I stored the user-selected values in some make-shift values, and set it back after the check function did its thing 

\-I would check whether the king was in check after the move was made, and if it was in check as a result of the move or if it was already in check in the first place, the move would be reverted. There were some bugs due to me having to change the square 1 and square 2 values for the iteration to occur, but it was all sorted

I’m at the final stretch- all I have to do is add in castling, and the game will be finished.

  

Jan 22nd 2021

To allow the user to castle, I would check to see if they tried to move their king two to the left or two to the right from the default spot, which is how you would request a castle in an online chess engine. Right here is the code; I called a function and checked to see if it was true. In the function, I used if functions to make sure that the king or the rook it wants to castle with hasn’t already moved the game, and then proceeded to check if the squares in-between were open. If the requirements were met, I would allow a castle.

  

After over 20 hours of mentally draining coding and troubleshooting, I finally did everything I seeked to do in this python program. Along the way I’ve conquered plenty of difficult problems, learned a lot more than if I were to make an easier program, and really screwed myself for finals by spending too much time working on this instead.

  

Anyways, let me show you the finished product in action.

  

Overview of code

I already went over some parts of the program during my daily journaling, but this will be more of a thorough rundown of all the code and functions. Even though there are areas for improvement, I’m really proud of myself for creating a complex program considering my prior experience and knowledge.

  

First, I imported Tkinter for my UI, string to have access to an organized alphabet string, os and sys to retrieve the images of the pieces from the files, and PIL to help with displaying images on the UI.

  

All my functions are stored under a single frame class, and at the bottom I create the root for the window, and run the functions to create the board: import\_pieces and set\_pieces.

  

import\_pieces retrieves all the files of the images for the pieces, and stores them as python images.

  

Set\_pieces prepares the board, by setting the images of the square buttons as their corresponding starting pieces, while filling the rest of the board with blank images.

  

The constructor method for the class contains a lot of variables that are accessible to the functions within the board class. Hopefully the comments and names of the variables should be enough to help you understand what they’re for.

  

Set\_squares uses for loops to create buttons and pair them into a dictionary with their corresponding position on the board. When pressed, these buttons call the select\_piece function which is where all the fun begins.

  

So, let’s run through a game, and see how the program aids the progression of a match.

  

To move the pieces, you first click on the first button of the piece you want to move, then the button of the square you wish to move it to.

Each square button, when clicked, runs the select\_piece function, which first checks to see who’s turn it is.

As you can see, I can’t move a black piece since white always has the first move in a game. 

-   To do this, I created a variable to store the number of turns played so far, and let white move when the number is even and black move when the number is odd. For a move to happen, the piece selected must be the same color as whoever has the turn.
    

If I select the pawn on d2 as my first square, it runs this line of code, which stores the position and button of the square, and increases the variable self.buttons\_pressed by 1.

When I select the second square, the position and button of the square is stored once again. If the second square is the same as the first, it sets the buttons pressed to 0 and reverts the 1st selection you made, making it useful if you want to deselect a piece. Lets select the pawn on e2 instead, and move it to e4. Since the two squares are different this time, the program then runs the functions allowed\_piece\_move and friendly\_fire in an if statement to see whether the move is allowed.

Allowed\_piece\_move finds out what piece is displayed on the first square selected, and checks to see if that piece is allowed to move to the second square by triggering piece-specific if-statements. For example, to evaluate whether a king was allowed to the second square, I would check and see if the change in rank and file of the two squares selected was less than 2. In this case, a pawn is allowed to move forward two squares if they are still in their starting position and if there is no piece directly in front of them, so the function returns True.

For pieces that must have a clear path to their destination, the function clear\_path is called with the kind of piece as the argument. From there, I use for loops and if statements to individually check and see if each square on the path to see is empty. If so, the function returns false. 

Looking back at the if statement, both conditions are satisfied, so the inner code runs.

Before moving the piece, the current square 1 and square 2 values are stored in temporary variables to prepare for the check function changing them. The image displayed on the second square is then changed to the first square’s image, and the first square’s image becomes blank.

After, an if statement is used to see if the king is in check. This checks not only if the king was in check at the beginning of the turn, but also after the move was made. 

In the in\_check function, the previous values are stored to be replaced after the function has finished doing its thing. Next, it uses a for loop to check if the opposing color’s pieces have a chance at capturing the king on the next move. This is done by setting the first square to every opponent piece, and the second square as the king’s current position which is found by iterating through all the buttons to see where the king is. Finally, it runs the allowed\_piece\_move function for each square with an opponent’s piece. As soon as it realizes that a piece can capture the king, the function returns True. If not, the function restores the square 1 and square 2 values to the ones that were selected by the user and returns False. In this case, in\_check would return False, so the pieces won’t revert back to their previous positions, which would have been the case if it returned True. Now the move has been successfully displayed, and what’s left are some if statements to see if the king and rooks have moved to help with the castling function, as well as an if-statement to see if a pawn is eligible for a promotion. I’ll demonstrate those two functions in a bit as this game progresses.

Since it’s black’s turn, I do the same move I did for white. To show that the check system is working, I move my light-square bishop to b5, pinning the pawn on d7. As you can see, I can’t move the pawn, since the in\_check function would return negative and run code to revert the move. Instead, I’ll move my pawn to c6, attacking the bishop. Next, I’ll develop my knight to f3, allowing white to castle on their next move. The black pawn takes the knight, and then white castles. Let’s run through the castle function:

The castle function is called in the allowed\_piece\_move function, and is triggered when the king moves forward at either of these squares. If the king or rook it wants to castle with hasn’t moved, it then checks to see if the squares in between the two pieces are clear. If so, the function moves the rook to the proper square, and the king is given permission to move two spaces.

Lastly, let’s go over the pawn promotion process. If a pawn manages to get all the way to the other side of the board, the if-statement for pawn promotion will be triggered and the function will be run. Then, a menu pops up, letting the player choose what piece it should promote to. 

-   This is done by creating a new tkinter root with buttons for each possible piece. When pressed, the return\_piece function is called, which changes the pawn image to the requested piece that is the same color as the pawn.
    

  
So that’s about it! In regards to how my program has changed overtime, I don’t think it really has; there were no major shifts in my code, and if anything I was simply adding onto my foundation of already existing code, like how the movement system is integral to my check system. 

  
  

Despite the excessive amount of time I’ve spent creating this program and editing this video, I don’t really regret any second of it. It was a very hands-on learning process, and it helped me see what it was like to tackle complex problems with little guidance. Instead of copying a YouTube video,  barely understanding what is being done, I was able to overcome even the toughest of tribulations, and reap the rewards in the form of a working program I can call my own. Lastly, I would like to say thanks to Mr. Knight for all the help throughout the class and for thinking I could do this in the first place, the people on Stack Overflow who helped me learn new coding techniques, and you for watching the video. Consider liking the video if you enjoyed it, and if you want to see more videos about my life, be sure to subscribe. 

  
  
  
  
  
  
  
  
  

I then move the light-bishop to b5, pinning the pawn in front of the queen. 

Since moving the pawn forward would result in a discovered check, black won’t be able to play the move.

  
  
  
  
  
**