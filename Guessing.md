# Random Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start])
    Start --> Init["Generate random number (1 to 100)"]
    Init --> Prompt[/"Prompt user for guess"/]
    Prompt --> ValidateInput{"Is input a valid number?"}
    ValidateInput -- No --> ErrorMsg[/"Display error: Invalid input"/]
    ErrorMsg --> Prompt
    ValidateInput -- Yes --> CheckGuess{"Is guess correct?"}
    CheckGuess -- Yes --> Correct[/"Display 'Correct!' message"/]
    Correct --> End([End])
    CheckGuess -- No --> HighOrLow{"Is guess too high or too low?"}
    HighOrLow -- High --> TooHigh[/"Display 'Too High!' message"/]
    HighOrLow -- Low --> TooLow[/"Display 'Too Low!' message"/]
    TooHigh --> Prompt
    TooLow --> Prompt
```

**Start**: The game begins

**Generate Random Number**: The computer selects a random integer between 1 and 100, this number is stored and not shown to the user.

**Prompt User for Input**: The program asks the user to guess a number in the given range.

**Validate Input**: The program checks if the input is a valid number. If it's not, the program shows an error message and prompts the user again.

**Check Guess**: If the input is valid, the program checks if it matches the random number.

**Correct Guess**: If the guess is correct, a congratulatory message is shown and the game ends.

**Incorrect Guess**: If the guess is wrong, the program checks whether the guess is too high or too low. A corresponding message ("Too High!" or "Too Low!") is displayed. The user is then prompted to guess again.

**End**: The game terminates once the correct number is guessed.