# Rock-paper-scissors

This is a game which allows the user to input their choice  which is then compared to the computers random choice.
The random module is first importde then a touple is created to house the options "rock, paper, scissors". 
The computer then picks a random choice from the options. The player using the input function chooses his choice.
A 'while' loop is used to create a loop that can only break when the player inputs a choice from the options otherwise the loop will continue asking the player to pick a choice. 
The if.. elif..else statement then determines whether the player or computer win or tie by comparing the choices.
A 'while' loop is then used to allow the game to continue if the player picks 'yes' and if he picks 'no' the loop ends and the game is ended with the statement 'Thanks for playing'
The code used:

import random

options = ("rock", "paper", "scissors")

running = True

while running:

    player = None
    computer = random.choice(options)

    while player not in options:
        player = input("Enter a choice (rock, paper, scissors): ")

    print(f"Player: {player}")
    print(f"computer: {computer}")

    if player == computer:
        print("It's a tie!")
    elif player == "rock" and computer == "scissors":
        print("You win!")
    elif player == "paper" and computer == "rock":
        print("You win!")
    elif player == "scissors" and computer == "paper":
        print("You win!")
    else:
        print("You lose!")

    play_again = input("Play again ? (yes/no): ").lower()
    if not play_again == "yes":
        running = False

print("Thanks for playing !!")




