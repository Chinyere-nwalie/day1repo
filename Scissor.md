# My rock, paper, scissor game.
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
---'    ____)____
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
game_choice = [rock, paper, scissors]
user_choice = int(input("What do you chose. Type 0 for rock. 1 for paper. 2 for scissor.\n"))
if user_choice >= 3 and user_choice < 0:
    print("You entered an invalid number, you lose!")
else:
  print(game_choice[user_choice])
  computer_choice = random.randint(0, 2)
  print(f"computer choose: {computer_choice}")
  print(game_choice[computer_choice])
  if user_choice == 0 and computer_choice == 2:
     print("You win!")
  elif computer_choice == 0 and user_choice == 2:
     print("You lose!")
  elif user_choice > computer_choice:
     print("You win!")
  elif computer_choice > user_choice:
     print("You lose!")
  elif computer_choice == user_choice:
     print("it's a tie!")
