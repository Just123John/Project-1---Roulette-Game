# Project-1---Roulette-Game
import random

def game():
    loaded_true = random.randint(1, 6)
    #print(loaded_true)

    action = input('Will you spin the chamber or fire?   |||    [A] Spin the Chamber   [B] Fire    |||   Answer: ').lower()
    while action not in ['a', 'b']:
        action = input('Will you spin the chamber or fire?   |||    [A] Spin the Chamber   [B] Fire    |||   Answer: ').lower()

    while action == 'a':
        loaded_true = random.randint(1, 6)
        #print(loaded_true)
        print('*spins chamber*')
        action = input('Will you spin the chamber or fire?   |||    [A] Spin the Chamber   [B] Fire    |||   Answer: ').lower()
        while action not in ['a', 'b']:
            action = input('Will you spin the chamber or fire?   |||    [A] Spin the Chamber   [B] Fire    |||   Answer: ').lower()

    if action == 'b':
        if loaded_true == 1:
            print('You died! :(')
        elif loaded_true != 1:
            print('You live to see another day.')
            replay = input('Would you like to play again?  |||   [A] Yes    [B] No    ||| ').lower()
            while replay not in ['a', 'b']:
                replay = input('Would you like to play again?  |||   [A] Yes    [B] No    ||| ').lower()
            if replay == "a":
                game()
            else:
                print('You walk away alive.')

game()
