# Desgin
Object-Oriented Design:
- The rain is used to define the raindrops and manage their state, such as position, character, and length. This allows for cleaner, more modular code and makes it easier to manage the behavior of individual raindrops. 

- A custom class is used to generate random numbers for character selection, colour and lenght.

Modern C++ Techniques:
- std::vector: This is used to store raindrop objects dynamically. It allows for efficient resizing, especially when the console size changes, ensuring the rain effect can adapt to different screen sizes.

- Smart Pointers & Memory Management: In some parts of the project, I’ve used smart pointers to manage memory safely, reducing the risk of memory leaks and ensuring better resource management.

- Use of the auto keyword to let the compilier decide on the data type which improves maintainabity and improves readability.

Modular Design:
- The project is structured into multiple files, each serving a specific purpose—such as handling console output, managing raindrop behaviors, and performing tests. This modular approach improves code organization and makes the project easier to maintain and extend.

## Design Choices:
Through out the project I tried to keep the display logic and rain algorithm as seperate as possible. This mean if I was to change to a different console it would make it easier.
With that in mind I made the RNG class sepereate rather than a member function of the rain. This increases the dependacies but makes it more modular if you were to use a different RNG class that is possible.
With all that being said I should have seperated the console function into its own class to de-clutter the test file.

## Rain Class:
<img src="https://raw.githubusercontent.com/Gavwalsh15/digital-rain-cpp/main/docs/assets/images/rain-class.png">

## RNG Class:
<img src="https://raw.githubusercontent.com/Gavwalsh15/digital-rain-cpp/main/docs/assets/images/RNG-class.png">
