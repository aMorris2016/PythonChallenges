## Hangman

Hangman is a classic word guessing game. The goal is to figure out an unknown word by guessing letters.
The player will be presented with a number of blank spaces representing the missing letters. If the letter guessed exists in the answer, 
then all places in the answer where that letter appears will be revealed. Every time the guess is wrong, player looses a life and the hangman begins to appear, piece by piece.

![hangman_img](https://user-images.githubusercontent.com/19298335/233436624-eeab6cd0-2fe5-4c48-adc2-6796126a9ffd.png)

To set up game:
1. Import necessary modules and data from hangman_art.py and hangman_words.py.
2. Choose a random word from the word list.
3. Initialize variables for end_of_game (set to False), lives (set to 6), and display (a list of "_" with length equal to the word length).
4. Print the hangman art logo at the start of the game.
5. Start a while loop that runs until end_of_game is True.
6. Get a letter guess from the user and convert it to lowercase.
7. Check if the letter has already been guessed by the user by checking if it's in the display list. If it is, print a message to inform the user and continue the loop.
8. If the letter is not in the display list, check if it's in the chosen_word. If it is, update the display list accordingly.
9. If the letter is not in the chosen_word, decrement the lives variable and print a message to inform the user.
10. If the lives variable reaches 0, set end_of_game to True and print a message to inform the user that they lost.
11. Check if all letters have been correctly guessed by checking if there are any "_" left in the display list. If there aren't any, set end_of_game to True and print a message to inform the user that they won.
12. Print the current state of the display list joined together as a string, and print the corresponding hangman art for the current number of lives left.
13. End the while loop and the game.

```
import random

from hangman_words import word_list
chosen_word = random.choice(word_list)
word_length = len(chosen_word)

end_of_game = False
lives = 6

#Import the logo from hangman_art.py and print it at the start of the game.
from hangman_art import logo
print(logo)

#Create blanks. Each "_" represents 1 letter.
display = []
guesses = []
for _ in range(word_length):
    display += "_"

while not end_of_game:
    guess = input("Guess a letter: ").lower()

    #If the user has entered a letter they've already guessed, print the letter and let them know.
    if guess in display:
        print(f"You've already guessed {guess}.")
        continue

    #Check guessed letter
    for position in range(word_length):
        letter = chosen_word[position]
    
        if letter == guess:
            display[position] = letter

    #Check if user is wrong.
    if guess not in chosen_word:
        # If the letter is not in the chosen_word, print out the letter and let them know it's not in the word.
        print(f"You guessed {guess}. That's not in the word. You lose a life.")
        lives -= 1
        if lives == 0:
            end_of_game = True
            print(f"You lose. Solution is {chosen_word}.")

    #Join all the elements in the list and turn it into a String.
    print(f"{' '.join(display)}")

    #Check if user has got all letters.
    if "_" not in display:
        end_of_game = True
        print("You win.")

   #Import the stages from hangman_art.py 
    from hangman_art import stages
    print(stages[lives])
    ```

Can you outsmart the game of Hangman? Test your word-guessing skills by uncovering a mystery word one letter at a time. 
But be warned - guess too many wrong letters and you'll meet a grisly fate by hanging! 

Play the game via the link below: 
https://replit.com/@aileenmorris201/hangman?v=1

