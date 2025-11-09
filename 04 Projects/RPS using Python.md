```python
import random

while True:
    possible_move = ["Rock", "Paper", "Scissors"]
    user_move = input("Enter: ")
    comp_move = random.choice(possible_move)
    user_win = "U win!"
    print("You chose", user_move, "and\nComputer chose", comp_move)

    if user_move == comp_move:
        print("It's a tie!")
    elif user_move == "Rock" and comp_move == "Scissor":
        print("U win!")
    elif user_move == "Paper" and comp_move == "Rock":
        print("U win!")
    elif user_move == "Scissors" and comp_move == "Paper":
        print(user_win)
    else:
        print("You lose!")
        
    play_again = input("Play Again? (y/n): ")
    if play_again.lower() != "y":
        print("Cya next time!")
        break
```
