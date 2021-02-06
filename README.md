# Guess.py-
#an interactive number guessing game

#def guess_check()
#tells whether the guess is too high or low
def guess_check(n,r):
   if n!=r and n<r:
      print("Your guess is too low.")
   elif n!=r and n>r: 
      print("Your guess is too high.")
#end guess_check()


#def correct_guess()
#prints a congratulatory msg if guessed correctly
def correct_guess():
   print("You win!")
   print()
#end correct_guess()


#def second_guess()
#checks if the second guess is correct or not
def second_guess():
   n = int(input("Enter your second guess: "))
   if n==r:
      correct_guess()
   else:
      guess_check(n, r)
      print()
      third_guess()
#end second_guess


#def third_guess()
#checks if third guess is correct or not
def third_guess():
   n = int(input("Enter your third guess: "))
   if n==r:
      correct_guess()
   else:
      guess_check(n, r)
      print()
      print("You lose. The number was "+str(r)+".")
      print()      
#end third_guess()

#--------main program----------------------------------------------------

import random
print()
print("I'm thinking of an integer in the range 1 to 10. You have three guesses.")
print()

r = random.randint(1,10)
n= int(input("Enter your first guess: "))

#if checks if first guess is correct or not
if n==r:
   correct_guess()
else: 
   guess_check(n,r)
   print()
   second_guess()
#end if 
