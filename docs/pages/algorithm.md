The algorithm for the Digital Rain effect iterating through a vector of RainDrop objects, each representing a single raindrop on the screen. 

The following steps describe the core algorithm:

- Initialization: The raindrops are randomly initialized, with each raindrop receiving a random position, symbol, color, and length.

- Movement: On each iteration of the loop, the raindrop moves one space down. If a raindrop reaches the bottom of the screen, it is reset to a new random position at the top of the console.

- Redrawing: The screen is updated by redrawing each raindrop in its new position and replacing the old space with a " ".

- Console Handling: SetConsoleCursorPosition is used to place raindrops at their respective positions, while SetConsoleTextAttribute controls the colour. 

- Resizing: When the buffer size is changed a check is done to see if we can fit more rain in the space. Currently set to half the X size. The same check is done for making it larger or smaller. 

This Algorithm should be portable enough to use in a different setting where a differnt display console is used. As all the Console handling is seperte to the rain logic. 

Windows Buffer info: 
```
struct WindowsBufferInfo {
    SHORT BufferSizeX = 120;
    SHORT BufferSizeY = 30;
    int ScreenWidth = 1920;
    int ScreenHeight = 1080;
    COORD windowLocation = { 0 , 0 };
    COORD lastBufferSize = { BufferSizeX , BufferSizeY };
};
```

# RNG Algorithm:

The Mersenne Twister is a widely used random number generator, implemented in the Standard Library as std::mt19937. It is named after Mersenne numbers, mathematical formula ($M_p​$ = $2^p$−1). The "twisting" process mixes the state to produce more randomness. It’s performed by applying bitwise operations like XOR and shifting the bits of the state.

Key Points:

- It is fast: The Mersenne Twister can generate random numbers very quickly.

- Long period: It can generate a large amount number of random numbers before repeating, making it suitable for tasks where you need a lot of randomness without patterns.

- Randomness: The numbers it produces are spread out evenly, making them useful for simulations, games, and other applications that need randomness.

- Not for security: It’s not designed for cryptography where secure randomness is needed, as it can be predicted if you know the seed.