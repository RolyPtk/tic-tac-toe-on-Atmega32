# tic-tac-toe-on-Atmega32

# Introduction

This X and O game (tic-tac-toe) was part of one of the projects I made during my 2nd year of studies.
The projects consists of an Atmega32 development board strictly dedicated to have fun with, and an 128x64 LCD display.
The programming part was done in mikroC PRO for AVR, while the simulation (before testing on the board itself) was done using Proteus 8 professional.
Certainly, I couldn't have completed the project without testing the code on the board, as I needed to play the game and test the code for bugs, hence I used
Proteus only to get used to the GLCD libraries which I've never worked with. I tested some of the libraries (useful for the project) using Proteus, and when I was
confident enough with most of the code, I started running it on the board as well.

# Code, issues met during the project

The sintax of the code is in C, I used methods such as void check_button_pressed(), void draw_X_O(int pozitie), int check_Win(), void draw_Grid(), void delay2S(), and also the GLCD_line/circle methods from the GLCD library to implement the application. 
The first issue I met (which I wasn't aware of before starting the project) was the compilation limitation I met in mikroC PRO for AVR of 4KB. Basically, you cannot compile more than that specific amount of memory (saddest limitation of an application I used to program in). Hence, limitation => optimization. A lot of optimization. This also meant that I couldn't implement everything I wanted (you can see the commented lines of code which could have made the game a nicer UI on the LCD). 
Another issue I met was with the reading of the input from the boards buttons. The input wasn't read cleanly when the user was pressing the button since the app was running in the loop too fast => I solved this by implementing delays.

# Result

....



# Proteus circuit implementation

<img width="1042" height="782" alt="Proteus circuit sample" src="https://github.com/user-attachments/assets/cc7ac66e-8e0c-4b82-9ccc-1735992e12e0" />


