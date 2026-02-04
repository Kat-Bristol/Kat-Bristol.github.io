---
layout: post
title: Python Guessing Number Game
image: "/posts/games_guess_the_number.png"
tags: [Python]
---

import random
random.randint(1, 10)

LOWER_BOUND = 0
UPPER_BOUND = 100
GUESS_LIMIT = 5
GUESS_COUNTER = 0
CORRECT_NUMBER = random.randint(LOWER_BOUND, UPPER_BOUND)

print(
      f'Try guessing the number that I am thinking. It is between {LOWER_BOUND} and {UPPER_BOUND}. '
      f'Good luck, you have {GUESS_LIMIT} guesses'
      )
      
while True:
    try:
        user_guess = int(input('What is your guess?? '))
    except ValueError:
        print('Please enter a valid number')
        continue
    
    if not (LOWER_BOUND <= user_guess <= UPPER_BOUND):
        print(f'Your guess is out of range! Try a guess between {LOWER_BOUND} and {UPPER_BOUND}')
        continue
    
    GUESS_COUNTER += 1
    remaining_guesses = GUESS_LIMIT - GUESS_COUNTER
    
    if user_guess == CORRECT_NUMBER:
        print(f'Wow, you got it in {GUESS_COUNTER} guesses - well done!')
        break
    elif user_guess < CORRECT_NUMBER:
        print(f'Your guess is too low, try again! Guesses remaining: {remaining_guesses}')
    else:
        print(f'Your guess is too high, try again! Guesses remaining: {remaining_guesses}')
        
    if remaining_guesses == 0:
        print(f"Sorry, you're out of guesses. The number you were after was {CORRECT_NUMBER}")
        break



