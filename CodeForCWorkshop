#include <stdio.h> // must be included for every program
#include <time.h> // use for generating random number for a seed
#include <math.h>

// create a constant
#define GUESSES 4

// global variables
int a = 5; // initialize variable a
int b; // reference variable b

// reference function
void guessingGame();

int main(void) {
  // references variables 
  int x;
  int y = 10;

  int A[5];
  
  // & reference operator
  // * dereference operator


  /*
    For printing data types in c, you need %(datatype value), this means:
    %d for integers
    %lf for double
    %f for float
    %c for characters
    %s for strings
    */
  char letter = 'A';
  printf("%c\n", letter);

  char name[] = "Michael";
  printf("This is my name, %s\n", name);

  char sentence[] = {"My name is Michael"};
  printf("%s\n", sentence);
  
  
  int *z = &a; // this pointer variable, z, stores the memory address of a
  printf("%d\n", z);
  int *z2 = a; // this pointer variable, z, stores the value of a
  printf("%d\n", z2);

  double a2 = a + 2;
  printf("%lf\n", a2);

  int mult = 5 * 10;
  printf("%d\n", mult);
  // x^y = pow(x, y)
  int a3 = pow(a, a); // 5 ^ 5
  printf("%d\n", a3);

  // size of gets the size of the array A and since it is int, it multiplies it by 4 for the number of bytes
  for(int i = 0; i<sizeof(A)/sizeof(A[0]); i++){
    A[i] = i + 5;
    printf("%d\n", A[i]);
  }
  
  // Guessing Game function
  guessingGame();
  
  printf("Hello World\n");
  return 0;
}

// define function
void guessingGame(){
  srand(time(NULL));
  int randomNumber = rand() % 11;
  int guess, input;
  int numberOfGuesses = 1;
  int playAgain = 1;
  
  printf("This function is a guessing game where the computer will generate a random number and you have three guesses to guess the correct number from 0 to 10\n");
  while(numberOfGuesses < GUESSES){
    printf("Enter the number that you think is the correct number?\n");
    scanf("%d", &guess);
    if(guess == randomNumber){
      printf("Congratulations, you guessed the correct number %d in %d guesses!\n", randomNumber, numberOfGuesses);
      break;
    }
    else if(guess < randomNumber){
      printf("Your guess of %d was too low.\n", guess);
    }
    else if(guess > randomNumber){
      printf("Your guess of %d was too high.\n", guess);
    }
    numberOfGuesses++;
    if(numberOfGuesses == GUESSES){
      printf("Sorry, but you did not guess the correct number in 3 tries. The correct number was %d.\n", randomNumber);
    }
  }
  printf("Would you like to play again? Enter 0 if you would like to quit or else enter 1 to play again.\n");
  scanf("%d", &input);
  if(input != 0){
    guessingGame();
  }
}
