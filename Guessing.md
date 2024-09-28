```mermaid
---
title: Random Number Guessing Game
config: 
    look: handDrawn
    theme: neutral
---
flowchart TD
Computer(Computer picks random number 1-10)-->user(User guesses number)
user--> correct(Correct?)
correct-->|Yes|outgood(Good job, you did it!)
outgood-->play
play(Play Again?)-->|Yes|Computer
play-->|No|END(END)
correct-->|no|incorrect(Too High or Too Low?)

incorrect-->|Too High|printhi(Print 'Too High')
incorrect-->|Too Low|printlow(Print 'Too Low')
printlow-->user
printhi-->user
correct-->|Exception|wrongdt(Print 'Wrong Data Type') 
wrongdt--> user
```

# ABOUT THIS FLOWCHART

* First step is to have the computer pick a number from 1-10  
* The user then guesses what the answer is  
* Is the answer correct?
	* Yes
		* Output "Good Job! Play Again?"
			* Yes - Computer picks a new number.
			* No - Ends the game
	* No
		* Too High or Too Low?
			* Too High - Outputs "Too High" and prompts the user to guess again.
			* Too Low - Outputs "Too Low" and prompts the user to guess again.

	* Exception
		* 