# PerfectStack
A classic, simple platform-stacking game... How many perfect stacks will you do?

## About:
This project was created using the Unity Game Engine (v.2021.3.8f1 LTS), learning the usage of the C# language for scripting, the (attempt at) practicing Object-Oriented Programming, scene transitions / stacking, custom lerping techniques (simple UI alpha value changes, 2D and 3D position changes over time), and trying to learn game design patterns.

The game itself is not a new concept. I decided to clone the game as it seemed simple enough whereby the core technical game mechanic is to spawn a platform, check position of current platform to previous platform, resize, reposition, then instantiate the 'overhanging' platform that would drop down - etc until game over.

Amongst these things I also realized I had done countless iterations to optimize for performance, especially for mobile, and the importance of staggering certain assets that required more memory allocation during its call to load (like music, if not 'streamed' from file).

Initially the target device was for mobile (android). For the sake of trying out the multi-platform publishing abilities in Unity, I decided change some settings and create a WebGL version for Perfect Stack.

Hosting the WebGL content onto Github pages had some issues, where the first upload resulted in an error:
> Unable to parse Build/0.9.3.framework.js.gz! This can happen if build compression was enabled but web server hosting the content was misconfigured to not serve the file with HTTP Response Header "Content-Encoding: gzip" present. Check browser Console and Devtools Network tab to debug.

Issue was resolved via solution: https://stackoverflow.com/a/73514279
A simple checkbox setting to enable decompression fallback, which from Unity's documents (https://docs.unity3d.com/Manual/webgl-deploying.html):
>The decompression fallback option enables Unity to automatically embed a JavaScript decompressor into your build. This decompressor corresponds to your selected compression method, and decompresses your content if the browser fails to do so.

