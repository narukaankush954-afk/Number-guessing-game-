#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int number, guess, attempts = 0;

    // Seed random number generator
    srand(time(0));

    // Generate random number between 1 and 100
    number = rand() % 100 + 1;

    printf("🎯 Welcome to the Number Guessing Game!\n");
    printf("I have chosen a number between 1 and 100.\n");
    printf("Try to guess it!\n\n");

    // Loop until the user guesses the number
    do {
        printf("Enter your guess: ");
        scanf("%d", &guess);
        attempts++;

        if (guess > number) {
            printf("Too high! Try a smaller number.\n\n");
        } else if (guess < number) {
            printf("Too low! Try a bigger number.\n\n");
        } else {
            printf("🎉 Congratulations! You guessed it in %d attempts.\n", attempts);
        }
    } while (guess != number);

    return 0;
}
 
