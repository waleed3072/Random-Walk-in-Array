# Character Array 2D in C

## Introduction
A program that generates a random walk across a n×m array where n and m are given as command line arguments. The array will contain characters (all ’.’ initially). The program randomly walks from element to element, always going up, down, left, or right by one element (NOT diagonally). The elements visited by the program will be labeled with the letters A through Z, in the order visited. Here’s an example of the desired
output for the command ./randwalk 12 15:
. . . . . . . X Y . . . . . .  
. . . . . . . W Z . . . . . .  
. . . . . . . V U . . . . . .  
. . . . . . R S T . . . . . .  
. . . . . . Q . . . . . . . .  
. . . . . . P O N . . . . . .  
. . . . . . . . M . . B A . .  
. . . . . . . . L K . C . . .  
. . . . . . . . I J E D . . .  
. . . . . . . . H G F . . . .  
. . . . . . . . . . . . . . .  
. . . . . . . . . . . . . . .  
Completed ’A’ through ’Z’  
  
Here is another example of a completed termination for ./randwalk 7 9:  
. . . . T S R O N  
. . . . U . Q P M  
. . . . V . H I L  
. . . . W Z G J K  
. . . . X Y F E D  
. . . . . . . . C  
. . . . . . . A B  
Completed ’A’ through ’Z’  
  
Here’s an example of a premature termination ./randwalk 5 7:  
. . K L C B A  
. . J M D . .  
. . I N E . .  
. . H G F . .  
. . . . . . .  
The letter N got trapped!  
Y is blocked on all four sides, so there’s no place to put Z.  

### Hint
Use the srand and rand functions to generate random numbers. After nerating a number, look at its remainder when divided by 4. There are four possible values for the remainder (0, 1, 2, and 3) indicating the direction of the next move. Before performing a move, check that (a) it won’t go outside the array, and (b) it doesn’t take us to an element that already has a letter assigned. If either condition is violated, try moving in another direction. If all four directions are blocked, the program must terminate.