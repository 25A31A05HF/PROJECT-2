#include <iostream>
#include <cstdlib>   // for rand() and srand()
#include <ctime>     // for time()

using namespace std;

int main() {
    srand(time(0));  // Seed for random number

    int secretNumber = rand() % 100 + 1;  // Random number between 1 and 100
    int guess;
    int attempts = 0;

    cout << "===== Number Guessing Game =====" << endl;
    cout << "Guess a number between 1 and 100" << endl;

    do {
        cout << "Enter your guess: ";
        cin >> guess;
        attempts++;

        if (guess > secretNumber) {
            cout << "Too high! Try again.\n";
        } 
        else if (guess < secretNumber) {
            cout << "Too low! Try again.\n";
        } 
        else {
            cout << "Correct! You guessed it in " << attempts << " attempts.\n";
        }

    } while (guess != secretNumber);

    return 0;
}
