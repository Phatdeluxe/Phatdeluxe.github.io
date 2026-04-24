## Battleship on an STM32

Using an STM32f429 discovery board I programmed the game of battleship. Using the provided I wrote software to run the game of battleship with both one-player and two-player options. 
The on board systems it uses is the touch screen, which is communicated with using I2C and a timer and a GPIO button running using interrupts. 
This project was interesting because we essentially wrote software that in any other scenario would be written using some form of class based language, but we wrote it in C. 
This had many challenges as during the class I made this in, we mostly interacted with peripherals through GPIO with little care for data structures. 
However much of this game required some form of data organization, because once all the embedded side of the project was finished (GPIO, Touch screen, timers) it was all data handling and workflows.
Through finishing this project I feel like a better C developer, knowing to pass references to structs as an argument of a function instead of having the function return a struct.

One challenge I faced while programming this was handling the AI when it finally made a hit. As a human player, I can pretty easily deduce where to check next based on the given information, but to reproduce that algorithmically/iteratively is another question.
After scrapping a terrible nested if-else statement I decided to settle for creating a depth first search approach, which would be concise, but not entirely efficient as far as winning the game goes.
