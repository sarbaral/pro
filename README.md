import random

def guess_number(num_guesses):
    # generate a random number between 1 and 10
    number = random.randint(1, 10)
    
    # loop for the number of guesses
    for i in range(num_guesses):
        # ask the player to guess the number
        guess = int(input("Guess the number between 1 and 10: "))
        
        # compare the player's guess with the actual number
        if guess == number:
            print("Congratulations! You guessed the number in", i + 1, "guesses.")
            return True
        elif guess < number:
            print("Too low, try again.")
        else:
            print("Too high, try again.")
    
    # if the loop completes without a correct guess, reveal the answer
    print("Sorry, you ran out of guesses. The number was", number)
    return False

#  list of players' names, 
players = ["Sar", "pallav", "Charlie", "TJ"]

# loop over the players and let each one play the game
for player in players:
    print("It's", player + "'s turn to play.")
    
    
    ### pren
    num_guesses = int(input("How many guesses would you like to have? "))
    result = guess_number(num_guesses)
    if result:
        print(player + " wins!")
    else:
        print(player + " loses!")
