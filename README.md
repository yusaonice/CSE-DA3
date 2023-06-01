# CSE-DA3
SNAKE GAME IN C
This is a very common and memorable game for us all. The programming for this game is very rudimentary and utilises basic c concepts, in addition to a few new functions I have come across.
This game requires us to make a few main functions which will be included in our Driver Code.
There are a few functions that I have used many times
1.gotoxy(a,b) = this is a user defined function. Its cause of functionality is due to SetCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), //coord//))
This allows to print whatever we want at the desired location by mentioning the coordinates.
2.fflush() = clears the out put buffer and helps in avoiding EOF
3. system(“cls”) = helps in clearing the display on the screen, so that we can printf something else.
4. kbhit()= checks if a key has been pressed
MAIN FUNCTIONS
1.	Border()
We have used this function to create a Border for the game. It also used the Food() function to display the food, “F” , at random coordinates within the perimeters of the border.
We have used two forloops and the GotoXY() function that helps us print the required symbol at the required outputs.
2.	Print()
This function is used to print the introduction and rules of the game. It uses the getch() and system(“cls”) which works together. The user after reading the instructions, presses a key ( this is where getch() works) and consequently the screen is cleared ( this is where system “cls” works)..
3.	Load()
This function is used to make the display fancier. We use a forloop that iterates slowly and the output is printed on screen . To begin the game,  the user has to press and key ( hence the use of getch() as last line in the function)
4.	GotoXY and gotoxy();
These functions use the SetConsoleCursorPosition(a,b) to print the required text/symbol/at the mentioned coordinates.
5.	Move()
Makes up majority of the driver code. It is a do-while loop. It also initialises the movement of the snake initially.  The “do” part of the code includes us executing the Food() function[generates food at random spots] For example, if the key pressed if the right key; then the Right() function is executed and so on so forth for the rest of the directions.
The function also has the condition to stop the game once the player presses ‘esc’
6.	Left(),Right(),Up(),Down()=
To move the snake, the program uses the arrow keys. The use of each key has a specific function designated to them. The function, dictates the length of the snake , the speed of the snake (Hence the use of Delay()) and the position of the head of the snake.
For example if we call function Up()= the function will iterate through the current length of the snake, it will give head[0]==’^’ and the rest of the snake’s body as ‘*’. That is how we see the snake in motion.
The rest of the directions work in the same way
9.Food(); this function uses the rand() to generate food at random coordinates within boundary. The condition is set as, if the x and y coordinates of the head match the coordinates of the food; then the length of the snake increases , and so does its speed.
The function then generates another food item at random location
The function also takes care of the initial condition where the coordinates of the food are zero initially. It will locate the food at random spots.
10. score()
This function will take into account the score of the player as well as the no of lives the player has. It uses the GotoXY ()[user defined] to print score and lives at the respective coordinates/ positions.


The code uses structure called coordinates, which will take care of the coordinates of the food item, the snake’s head and its length.

Points I wish to explain
1.	We have created a structure named coordinates. Almost every function used in the program uses coordinates so that we can apply it to the game.
2.	This is extremely helpful in the directions of left(),right(),up(),down().
The functions match the coordinates of the snake’s head and food’s coordinate to increase the score.
