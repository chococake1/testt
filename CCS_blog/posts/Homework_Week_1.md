---
title: Week 1 Homework
published_at: 2024-03-30
snippet: Week one of homework!
disable_html_sanitization: true
---

# Homework Week 1

## Creating a Grid
<iframe src="https://editor.p5js.org/chococake1/full/my2HtE39e" width="600px" height="642px"></iframe>

![Checkerboard Grid](/grid/grid1.png)
I started by using the square p5js of squares moving as a base, this was because it already had way of organising squares depending on how much there were

![Checkerboard Grid](/grid/grid2.png)
Next, I Changed the colours of the squares and the background, changed the canvas shape, I planned to make a checkerboard pattern like a chess board

![Checkerboard Grid](/grid/grid3.png)
![Checkerboard Grid](/grid/grid4.png)
![Checkerboard Grid](/grid/grid5)
I tried messing around with making all the squares the same shape

![Checkerboard Grid](/grid/grid7.png)
Until I got to this which looked similar to a row in a checkerboard

![Checkerboard Grid](/grid/grid8.png)
![Checkerboard Grid](/grid/grid9.png)
I oriented the rows and repeated them to create this grid effect, I’m not to sure where the number 71 fits in on line 15, but I got it after trial and error
I also realized at this point that it was going to be much larger than the originally planned eight by eight chess board grid I was going for

![Checkerboard Grid](/grid/grid10.png)
I copied what I had and moved it all down, creating this stripe effect, but also assuring that the black squares were at least big enough to fill in the empty gaps!


![Checkerboard Grid](/grid/grid11.png)
I moved the copied effect slightly to the left to complete the checkerboard look

![Checkerboard Grid](/grid/grid12.png)
![Checkerboard Grid](/grid/grid13.png)
The squares were not completely aligned correctly so after some trial and error I got it more accurately, though it still has some small mistakes, such as the edges of some black squares overlapping.

**Reflection**
In reflection, this probably was not the most effective way of making a checkerboard pattern, many numbers I had no idea of arriving at such as the 37.5, 71 and 37 on line 20, resulting in the pattern being a little faulty, and the way I just copied and moved the second set of squares is inefficient in the longer term.

## This Other Grey
<iframe src="https://editor.p5js.org/chococake1/full/EcKVk0QSc" width="600px" height="642px"></iframe>
The artwork I chose from Rafaël Rozendaal was his 2017 website, ‘thisgrey’, a monochrome house made of simple geometry such as rectangles and triangles. Rozendaal was able to achieve these effects using some timed increasing of brightness, each element of the house, in my case, I used frameCount. Rozendaal has each element of the house asynchronous, increasing and resetting at differing rates, I achieved this by making each shape start, increase, and reset at a different brightness levels. ![image](https://github.com/chococake1/CCS_blog/assets/101231598/9bc2cfe8-fab4-4ec7-aaed-b4bb4c40a346)

![Grey House](/house/house1.png)
I started by creating the canvas and a variable for brightness which would increase every 30 frames in addition to a background, which used the brightness variable and reset every time it reached 100.

![Grey House](/house/house2.png)
Next, I made a square and aligned it on the bottom to look like a rectangle, I also realised increasing once every 30 frames was very slow, so I got rid of the division on line 8.

![Grey House](/house/house3.png)
I aligned the square to more closely replicate how it looks on Rozendaal’s website in addition to using the ‘fill’ function to colour the square, both the background and rectangle would increase in brightness at different speeds, I would also add a random numbers to each element to start, reset and increase at different brightness levels.

![Grey House](/house/house4.png)
Next, I added a rectangle window after trial and error to get the position and shapes close enough, in addition to separate fill function.

![Grey House](/house/house5.png)
![Grey House](/house/house6.png)
Similar to the window I added another rectangle to create the door with Its’ own fill function, I also slightly altered the window to more closely match Rozendaal’s.

![Grey House](/house/house7.png)
![Grey House](/house/house8.png)
Next, I added a triangle, I had no idea how it worked but after messing around with it, I figured out each number in the triangle function correlated to a position of each of the triangle’s angles. It also has Its’ own fill function.

![Grey House](/house/house9.png)
![Grey House](/house/house10.png)
![Grey House](/house/house11.png)
Finally, I added the chimney, which was simply a rectangle behind the triangle roof, after aligning it, I moved it behind the triangle by moving the actual code to draw it to before the triangle roof. (The final image makes it hard to see the chimney but Its’ there)

**Reflection**
In conclusion, I’m satisfied with how it turned out, the reason I chose this work was because I thought it was one of the more possible works on Rozendaal’s website with what we had learnt in class. Parts I could improve on include the fill function, there probably is a better way of making each shape change at different speeds without having to do each manually, and randomizing the initial brightness of each shape.
