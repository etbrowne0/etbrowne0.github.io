```mermaid
flowchart TD
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
correct-->|Exception|wrongdt(Wrong Data Type) 
wrongdt--> user
Start([Start]) --> End([End])
```