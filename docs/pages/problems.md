# Problems and Challenges

## Buffer Resizing:
One of my first issues was when the screen is made smaller the text will wrap causing the X values of the coord to be incorrect and the charater not to be cleared. 
To sligltly combat this I added a check to see if the screen size was changed the I would use ```system("Cls")``` this helped a small bit but didnt always work and sometimes we get that still.
The other option was to call ```system("Cls")``` every loop but that sadly caused a 'flashing effect'. Some other students use a double buffer which if I had more time would have been cool to implement.

## Tracking Location:
Orignally I wanted you to be able to move the window around the screen the rain would move with you but similar to the buffer issue I found it hard to track the coordinates. So that idea was scrapped.

## Extracting Y 
When using ```csbi.dwSize.Y``` it returns the max size of the buffer with scroll but I only want the part of the screen we see so Iopted to use. 
```csbi.srWindow.Bottom - csbi.srWindow.Top``` which gets the screen size not the buffer size.
## Safe area 
I found sometimes if you tried to print to the last line in the buffer it would but the charater in a seemingly random spot but that turned out to be the way I read in the Y it was reading the whole screen so there was an extra space to print to but you could not.

