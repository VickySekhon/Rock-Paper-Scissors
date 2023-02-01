#My thought process:
#prompt user1 and user2 to enter their chosen option (R,P,S)
#setup if statements that contain the games conditions (rock beats scissors, scissors beats paper, paper beats rock)

import random

# Declare variables to store the scores of the player and the computer
com_points = 0
player_points = 0

# Define a header to display the options
header = "|Options Display:"

# Print the welcome message and list of options
print("Welcome to Rock, Paper, Scissors By: Vicky Sekhon")
print()
options = ["Rock","Paper","Scissors"]
print(f"Choose an option from: {options} (0 = Rock, 1 = Paper, 2 = Scissors)")

# Start the game loop
while True:
    # Get the player's choice and the computer's choice
    player = (options)[int(input("Enter your choice: "))]
    com = random.choice(options)

    # Display the choices
    print()
    print(f"""{header:>27s}|
    ---------------------------------------------------------------------------
    |Player: {player:7}|  |Computer: {com:7}|
    """)

    # Define the game conditions
    game_conditions = [
        # user          computer          result
        [options[0], options[1], f"Paper Wins! Computer now has {com_points} points!"],
        [options[0], options[2], f"Rock Wins! Player now has {player_points} points!"],
        [options[1], options[0], f"Paper Wins! Player now has {player_points} points!"],
        [options[1], options[2], f"Scissors Wins! Computer now has {com_points} points!"],
        [options[2], options[0], f"Rock Wins! Computer now has {com_points} points!"],
        [options[2], options[1], f"Scissors Wins! Player now has {player_points} points!"],
        [options[0], options[0], "Tie!"],
        [options[1], options[1], "Tie!"],
        [options[2], options[2], "Tie!"],
    ]

    # Check the game conditions and determine the result
    result = None
    for condition in game_conditions:
        if player == condition[0] and com == condition[1]:
            result = condition[2]
            if "Computer" in result:
                com_points += 1
            elif "Player" in result:
                player_points += 1
            break

    # If no valid condition was found, set the result to "Invalid choice"
    if result is None:
        result = "Invalid choice"

    # Display the result
    print(result)
    print()
