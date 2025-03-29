# Digital Rain

This C++ project aims to imitate the digital rain effect from The Matrix, using the Windows Console API to simulate falling characters. The application generates random raindrops that fall from the top of the terminal, with new characters continuously replacing them. In this project, I focused on implementing modern coding practices and object-oriented design while using a multifile structure to ensure better code organization, readability, and maintainability.

## [Design](/docs/pages/design.md)

## Algorithm
The algorithm for the Digital Rain effect iterating through a vector of RainDrop objects, each representing a single raindrop on the screen. 

The following steps describe the core algorithm:
Initialization: The raindrops are randomly initialized, with each raindrop receiving a random position, symbol, color, and length.
Movement: On each iteration of the loop, the raindrop moves one space down. If a raindrop reaches the bottom of the screen, it is reset to a new random position at the top of the console.
Redrawing: The screen is updated by redrawing each raindrop in its new position and replacing the old space with a " ".
Console Handling: SetConsoleCursorPosition is used to place raindrops at their respective positions, while SetConsoleTextAttribute controls the colour. 
## Problem Solving

## Reflection



<img src="https://raw.githubusercontent.com/Gavwalsh15/digital-rain-cpp/main/docs/assets/images/Screenshot 2023-09-28 121727.png" width="100" height="100">
