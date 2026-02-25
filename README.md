#include<iostream>
#include<cstdlib>
#include<ctime>
using namespace std;

int main() {

    srand(time(0));

    int target = rand() % 100 + 1;
    int guess;
    int attempts = 0;

    do {
        cout << "Enter your guess: ";
        cin >> guess;
        attempts++;

        if(guess > target)
            cout << "Too high, try again\n";
        else if(guess < target)
            cout << "Too low, try again\n";

    } while(guess != target);

    cout << "Correct! You guessed in " << attempts << " attempts\n";

    return 0;
}
