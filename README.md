# guessing_random_numbers_game
It is the code for the game of guessing random numbers.


#include <stdlib.h>
#include <time.h>
#include <stdio.h>


int random_number()
{
	return rand()%101;
}


int main()
{
	srand(time(0));
	
int number = random_number();
int guess;
int counter;
	
 do
	{
		printf("Type a number between 1-100:");
		scanf("%d",&guess);
		counter++;
		if(guess < number)
		{
			printf("Try a larger number!!!\n");
		}
		else if(guess > number)
		{
			printf("Try a smaller number!!!\n");
		}
		else
		{
			printf("\nCongratulations, you found the number!!!");
			printf("number of guesses:%d",counter);
		}
    }while(guess != number);
	
return 0;
}
