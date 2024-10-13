# Game-Rock-Paper-Scissors
this is project of conGnoRise internship

import random


# Game Rock, Paper, Scissors
def play_game():
    print("Welcome to Rock, Paper, Scissors Game!")

    # Score
    user_score = 0
    computer_score = 0

    # Choices
    choices = ['rock', 'paper', 'scissors']

    while True:
        # Your input
        user_choice = input("\nChoose rock, paper, or scissors: ").lower()

        # Valid choice
        if user_choice not in choices:
            print("Invalid choice. Please choose 'rock', 'paper', or 'scissors'.")
            continue

        # Computer's choice
        computer_choice = random.choice(choices)

        # Display user and computer choices
        print(f"\nYou chose: {user_choice}")
        print(f"Computer chose: {computer_choice}")

        # Game winner
        if user_choice == computer_choice:
            print("\nIt's a tie!")
        elif (user_choice == 'rock' and computer_choice == 'scissors') or \
                (user_choice == 'scissors' and computer_choice == 'paper') or \
                (user_choice == 'paper' and computer_choice == 'rock'):
            print("\nYou win this round!")
            user_score += 1
        else:
            print("\nYou lose this round!")
            computer_score += 1

        print(f"\nScore: You {user_score} - {computer_score} Computer")

        #If you wants to play again
        play_again = input("\nDo you want to play again? (yes/no): ").lower()
        if play_again != 'yes':
            break

    # Final message
    print("\nThanks for playing!")
    print(f"Final Score: You {user_score} - {computer_score} Computer")


# Game start
play_game()

