# Random Guessing Game Flowchart

This flowchart represents the structure of a random guessing game. The game follows these steps:
1. The computer generates a random number within a specified range.
2. The player is prompted to guess the number.
3. If the guess is correct, the game ends, and the player wins.
4. If the guess is incorrect, the game provides feedback: either "Too high" or "Too low".
5. The game loops back to allow the player to guess again until the correct number is guessed.

```mermaid
flowchart TD
    Start -->|Generate random number| RandomNumber[Computer selects a random number]
    RandomNumber --> UserInput[Player guesses a number]
    UserInput --> CheckGuess{Is the guess correct?}
    CheckGuess -->|Yes| Correct[Player guessed correctly]
    CheckGuess -->|No, too high| TooHigh[Guess is too high] --> UserInput
    CheckGuess -->|No, too low| TooLow[Guess is too low] --> UserInput
    Correct --> End[End of game]
