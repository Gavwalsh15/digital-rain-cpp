# Digital Rain

## Introduction 
This C++ project is an application that mimics the Digital Rain effect from The Matrix. Developed in C++, it use various functions from the Windows Console API to handle text rendering and create the dynamic falling drops effect. The project focuses key C++ concepts such as object-oriented design, modern C++ coding styles and methods.

## Design & Test
The design of the project revolves around creating a fluid and efficient simulation. 

Key design elements include:

Object-Oriented Design: Classes are used to define the raindrops and manage their state, such as position and character type, while also maintaining the flow of the digital rain and a Random Number generator class.
Modern C++ Techniques: 
Modular Design:

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
