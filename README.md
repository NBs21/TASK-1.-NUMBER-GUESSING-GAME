# Name:        NUMBER-GUESSING-GAME
# Purpose:     Cod Soft TASK-1 (C++)
# Create a program that generates a random number and asks the user to guess it. Provide feedback on whether the guess is too high or too low until the user guesses the correct number.
# Author:      NURFUL SHAIKH
# Created:     11-11-2023

#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;
int main()
{
    int num, guess, tries = 0;
    srand(time(0));
    num = rand() % 100 + 1; // random number between 1 and 100
    cout << "Guess My Number Game\n\n";
    do
    {
        cout << "Enter a guess between 1 and 100 : ";
        cin >> guess;
        tries++;
        if (guess > num)
            cout << "Too high!\n\n";
        else if (guess < num)
            cout << "Too low!\n\n";
        else
            cout << "\nCorrect! You got it in " << tries << " guesses!\n";
    } while (guess != num);
    return 0;
}
