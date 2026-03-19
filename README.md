import time
import sys
Password = 'admin'
attempts = 3
name = input('Fill in your name: ')
age = int(input('Fill in your age: '))
while attempts > 0:
    entered_password = input('Enter password: ')
    if entered_password == 'admin':
        print('Correct password.')
        break
    attempts -= 1
    if attempts == 0:
        print('Access denied!')
        sys.exit()

if age >= 18:
    print('Welcome! ' + name + '!')
elif age == 16:
    print('Were the same age, welcome!')
else:
    print('Sorry, not there yet!')
if Password == 'admin' and age >= 18 or 16:
    time.sleep(1)
    print('Gaining access to the game..')
    time.sleep(1.5)
    print('loading... almost ready.')
    time.sleep(1.5)
    print('Welcome to the game, ' + name + '!')
    time.sleep(1.5) 

    Game = input('would you like to play a game? (yes/no) ')
    if Game == 'yes': print('great! Lets play.')
    elif Game == 'no': print('ok, maybe next time.') 
    if Game == 'no':
        sys.exit()

    print('loading game...')
    time.sleep(1.5)
    print('Lets begin!')
    time.sleep(1.5)
    
    print('You will now get the choice between 2 colours, red and blue.')
    print('Its a 50/50 chance, if you get it right you win, if you get it wrong you lose.')
    time.sleep(3.5)
    print('we will now proceed!')

    import random
    colours = ('red', 'blue') 
    computer_choice = random.choice(colours)
    user_choice = input('Pick a colour (red/blue): ')
    print('You picked ' + user_choice + ' nice choice...')
    print('Here we go!')
    time.sleep(0.8)
    countdown = 3
    while countdown > 0:
        print(countdown)
        time.sleep(1)
        countdown -= 1
    if user_choice == computer_choice:
        print('Congratulations! You win!')
    else:
        print('Sorry, you lose! The correct colour was ' + computer_choice + '.')
        time.sleep(1.5)
print('Thanks for playing!')
time.sleep(2)
print('closing system... Goodbye!')
time.sleep(3)
sys.exit() 
