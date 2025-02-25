#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main()
{
	int random,guess;
	int no_of_guess = 0;
	srand(time(NULL));
	
	printf("WELCOME TO THE WORLD OF GUESSING NUMBERS!\n\n\n");
	random = rand() % 100 + 1;  //Generates between 1 and 100.
	
	do {
		printf("Please enter your guess(Between 1 to 100): ");
		scanf("%d", &guess);
		no_of_guess++;
		
		if (guess<random)
		{
			printf("Guess larger number! \n");
			
		}
		else if (guess>random)
		{
			printf("Guess smaller number! \n");
		}
		else {
			printf("CONGRATS! YOU HAVE SUCCESSFULLY GUESSED THE CORRECT NUMBER IN %d ATTEMPTS! ", no_of_guess);
		}
	} while (guess != random);
	
	printf("\n Bye-Bye, Thanks for Playing.");
	printf("\n Developed by Kushagra Srivastava");
	return 0;
}
