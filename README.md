# Lottery
import random

def select_lottery_winners():
    # Get the number of participants and winners
    num_participants = int(input("Enter the number of participants: "))
    num_winners = int(input("Enter the number of winners: "))
    
    # Check if the number of winners is less than or equal to the number of participants
    if num_winners > num_participants:
        print("Number of winners cannot be more than the number of participants.")
        return
    
    # Generate a list of participants
    participants = [f"Participant {i+1}" for i in range(num_participants)]
    
    # Randomly select winners
    winners = random.sample(participants, num_winners)
    
    # Display the winners
    print("The winners are:")
    for winner in winners:
        print(winner)

# Run the lottery selection
select_lottery_winners()
