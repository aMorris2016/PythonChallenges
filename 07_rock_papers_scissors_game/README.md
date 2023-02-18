## Rock, Paper, Scissors Game
A classic game of rock, paper, scissors translated to Python code. The random module was imported in order to generate the computer's random choice.

The game is played where players deliver hand signals that will represent the elements of the game; rock, paper and scissors. 
According to the official [World Rock Paper Scissors Association](https://wrpsa.com/the-official-rules-of-rock-paper-scissors/), 
the outcome of the game is determined by 3 simple rules:

- Rock wins against scissors.
- Scissors win against paper.
- Paper wins against rock.

![rock_paper_scissors](https://user-images.githubusercontent.com/19298335/219845747-d5ae1034-40f7-4e76-9973-acdec8916100.gif)

```
rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

import random
game = [rock, paper, scissors]

#Take the player's input
signal = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors: "))

#Show player's hand
if signal > 2:
    print("You typed an invalid number. You lose.\n")
else:
  print(game[signal])
  
#Generate computer's random choice
print("Computer's choice")
computer = random.randint(0,2)
print(game[computer])

#Determine winner
if signal == computer:
  print("It's a tie.")
elif signal == 0:
  if computer == 2:
    print("You win!")
  else:
    print("You lose.")
elif signal == 1:
  if computer == 0:
    print("You win!")
  else:
    print("You lose.")
elif signal == 2:
  if computer == 1:
    print ("You win!")
  else:
    print("You lose.")
```

Try the game via the link below and see if you can beat the computer:

https://replit.com/@aileenmorris201/rock-paper-scissors?v=1
