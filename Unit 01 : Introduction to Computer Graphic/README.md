# Unit 1 : Introduction to Computer Graphic

## Introduction

Computer graphics is a graphical tool used to create an image of any object in an electronic device. It's not only used to create but also used to perform transformation and shading effects on an image.

In any device, an image is formed and is displayed in pixel. Pixel is a small addressable unit of screen which stores a small part of an image. Each pixel contains 3 colors: red, green, and blue. Each color is of 8 bit i.e. red is 8 bit, green is 8 bit and blue is 8 bit. Hence, 1 pixel is 24 bit (3 byte).

More the no. of pixels greater will be memory. So, the price will be increased.

## DDA (Digital Differential Analyzer) Algorithm

    Step 1: Input the line endpoints and store the left endpoint in (x1, y1) and right endpoint in (x2, y2).
    
    Step 2: Calculate the values of dx and dy i.e. dx = x2 - x1, dy = y2 - y1
    
    Step 3: if (abs(dx) > abs (dy)) {
                Step-length = abs (dx)
            }else{
                Step-length = abs (dy);
            }
    
    Step 4: Calculate the values of x-increment and y-increment
            
            x-increment = dx/steplength
            y-increment = dy/steplength
    
    Step 5: set x= x1 and y = y1
    
    Step 6: plot (x, y)
    
    Step 7: for k = 1 to step length do
                • x = x + x-increment
                • y = y + y-increment
                • Perform round off and plot each calculated (x, y) i.e., Plot (round(x), round(y))
    
    Step 8: End