---
layout: page
title: Projects
---

<br/><br/>

# CU Boulder

### STM32 Battleship game:
Using an STM32f429 discovery board I programmed the game of battleship. Using the provided I wrote software to run the game of battleship with both one-player and two-player options. The on board systems it uses is the touch screen, which is communicated with using I2C and a timer and a GPIO button running using interrupts. This project was interesting because we essentially wrote software that in any other scenario would be written using some form of class based language, but we wrote it in C. This had many challenges as during the class I made this in, we mostly interacted with peripherals through GPIO with little care for data structures. However much of this game required some form of data organization, because once all the embedded side of the project was finished (GPIO, Touch screen, timers) it was all data handling and workflows. Through finishing this project I feel like a better C developer, knowing to pass references to structs as an argument of a function instead of having the function return a struct.

One challenge I faced while programming this was handling the AI when it finally made a hit. As a human player, I can pretty easily deduce where to check next based on the given information, but to reproduce that algorithmically/iteratively is another question. After scrapping a terrible nested if-else statement I decided to settle for creating a depth first search approach, which would be concise, but not entirely efficient as far as winning the game goes.

### RISC-V pipelined processor:
I created a schematic and designed a simulation for a RISC-V pipelined processor in my Computer Organization class. This involved writing the logic for all stages, fetch, decode, execute, memory, and writeback. This also included never jump branch prediction, and memory/writeback bypassing. I would say this was a team effort as much of the simulation was already coded for me, but much of the instruction definition and stage logic was left for me to figure out. This shows not only a competency with the C language, but also an understanding of the control and data flow of a RISC-V processor. 

### Tiago-Lite:
For this project I programmed a Tiago-Lite robot to dynamically grab jars off one table and put them on a different table. This was done using Python and the WeBots simulator. This project involved writing functions for a behavior tree to drive the robot's decision making, using camera input to detect the jars and their position, and lidar to map the environment and determine where the robot is able to move. I worked on this alone, some code and guidance was provided by the professor, but all of the code and robot logic was written by me. This took a lot of understanding of how robots function, and how the data received by the sensors could be turned into something the robot can understand. It also required a good understanding of behavior trees and how they can simulate artificial intelligence and decision making.

### Verilog mastermind game:
I wrote a program in Verilog for a Xilinx FPGA that was essentially the game of Mastermind, where there is a pseudo-randomly generated pattern and you have 10 guesses to determine the pattern, and each guess will show the number of correct options in the correct spaces and the number of correct options in the incorrect spaces. As stated this was written in Verilog for the Xilinx FPGA. All the code was written by hand by myself. This project was written using a rather complex state machine as the design restrictions on this specific FPGA were 4 buttons and 16 switches, so there was a bit of knowledge on how to play required. Essentially you had one state machine keeping track of the current guess and another keeping track of the current button input, as well as an array remembering what the previous guesses were so a player could go back and review them.

One challenge of this was setting up that array memory system so a player could return to previous guesses and see how they were scored to make informed guesses on further attempts. This was essentially solved by having each switch refer to a turn, and by having only that switch set you could see what that guess was, and how it was scored. This unfortunately required execution knowledge of the player, but once understood, I think it worked quite nicely.

<br/><br/>

# Data Science

## Predictive Models

### Air BnB Price Predictor

Worked on a team to create a neural network that predicts the price of an Air BnB.

I worked with two other data scientists to create a model that predicts price of an Air BnB. I believe that model creation is not something that can easily be done by multiple people, and we were finding that there was not enough work for us all to do something meaningful for the project. Instead we made it a bit of friendly competition, and we all created models and used the model that had the lowest MAE (mean average error). Unfortunatly my model did not win the competition, but you can find it below if you are curious at looking at it.

The repo for the project can be found [here on github](https://github.com/AirBnB-dream-team/DS).

The repo for my personal model can be found [here on github](https://github.com/Phatdeluxe/Unit_4_build_week).

### Adult Diabetes Predictor

Using an XGBoosted regressor, trained a model to predict the % of adults with diabetes.

A toy app of the model can be found [here on Heroku](http://adult-diabetes-predictor.herokuapp.com/).

A blog post I wrote about the work can be found [here on Medium](https://medium.com/@ethan.skamarock/can-changes-be-made-to-reduce-diabetes-26e9237a7673?source=friends_link&sk=e1b5a6c2a42e4362dbc5a3d9d69e6ade).

The repo can be found [here on github](https://github.com/Phatdeluxe/adult_diabetes_prediction)

<br/><br/>

## Data Exploration

### C4ADS Nuclear Fuel Cycle

I worked on a project for C4ADS. The goal of this project was to create a model that could predict whether or not a company had the capability to create precision materials that could be used in the creation of nuclear fuels or weaponry.
I made a longer post about his that can be found [here on my website](http://www.ethanskamarock.com/2020-05-07-nuclear-fuel-cycle.md/)

### Drug abuse data storytelling project

Looked through the CDC's Multiple Cause of Death (Detailed Mortality) and found some disturbing statistics.

A blog post can be found [here on medium](https://medium.com/@ethan.skamarock/will-there-ever-be-change-to-this-epidemic-3c4ae69a30ba).

The repo can be found [here on github](https://github.com/Phatdeluxe/Portfolio-Projects/blob/master/Portfolio_project_OD_deaths.ipynb/).

<br/><br/>

## App Creation

### Med-Cabinet Strain Recommender

Worked on a team to create a python backend that took a bunch text, used NLP to create a prediction, and returned Medical Marijuana strain recommendations.

I worked on creating an SQlite database with all the strain information and taking the prediction, querying the database, and returning the strain information in a JSON object for the front end.

The DS repo for this project can be found [here on github](https://github.com/build-med-cabinet-3/Machine-learning)
