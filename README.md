# PerfectStack
A classic, simple platform-stacking game... How many perfect stacks will you do?

## About:
This project was created using the Unity Game Engine (v.2021.3.8f1 LTS), learning the usage of the C# language for scripting, the (attempt at) practicing Object-Oriented Programming, scene transitions / stacking, custom lerping techniques (simple UI alpha value changes, 2D and 3D position changes over time), and trying to learn game design patterns.

The game itself is not a new concept. Intially decided to clone the game as it seemed simple enough whereby the core technical game mechanic is to spawn a platform, check position of current platform to previous platform, resize, reposition, then instantiate the 'overhanging' platform that would drop down - etc until game over.

Amongst these things I also realized I had done countless iterations to optimize for performance, especially for mobile, and the importance of staggering certain assets that required more memory allocation during its call to load (like music, if not 'streamed' from file).