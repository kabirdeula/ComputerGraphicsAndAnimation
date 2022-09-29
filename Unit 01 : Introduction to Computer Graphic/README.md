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

## Bresenham's Line Drawing Algorithm

### Bresenham's algorithm for m <= 1.

    Step 1: Input the line endpoints and store the left endpoint in (x0, y0).
    
    Step 2: Load (x0, y0) into the frame buffer i.e. plot the first point
    
    Step 3: Calculate constant Δx, Δy, 2Δy -2Δx and obtain the initial decision parameter as:
    
            p0 = 2Δy – Δx

    Step 4: At each xk along the line, starting at k=0 perform the following test:
            
            • If pk < 0
                Plot pixel (xk+1, yk) and
                Set pk+1 = pk +2Δy
            
            Otherwise:
                Plot pixel (xk+1, yk+1), and
                Set pk+1 = pk + 2Δy - 2Δx
    
    Step 5: Repeat step 4 Δx times
    
    Step 6: End

### Bresenham's algorithm for m > 1.

    Calculate m, if |m| >1:
    Such case occurs when Δx < Δy, so m = (Δy/ Δx) >1.

    In such case role of x and y are interchanged that is we can step along y-direction in unit steps and calculate successive x-values

    Calculate initial decision parameter p0 = 2Δx – Δy.

    If pk < 0, select point (xk, yk+1), and set pk+1 = pk + 2Δx
    
    Otherwise, if pk > 0, select point (xk + 1, yk+1), and set pk+1 = pk + 2Δx - 2Δy.
    
    If x1>x2, and y1>y2 then start from (x2, y2) to (x1, y1) i.e, interchange coordinates.

## Midpoint Circle Algorithm / Bresenham’s Circle Drawing Algorithm:

Here, for a given radius “r’ and screen center position (xc, yc), first algorithm is set up to
calculate pixel position around a circle path centered at the coordinate origin (0, 0). Then each
calculated position (x, y) is moved to its proper screen position by adding xc to x and yc to y.

    Step 1: Input radius “r” and circle center (xc, yc)
    
    Step 2: Obtain the first point on the circumference by assuming that circle is centered on the origin i.e. (x0, y0) = (0, r)

    Step 3: Calculate the initial decision parameter as p0 = 5/4 – r. (if r is integer then set p0 = 1 – r).

    Step 4: Repeat until x > = y at each xk position, starting at k = 0, performing the following
        if (pk < 0){
            Select pixel (xk+1, yk)
            Set pk+1 = (Pk+2xk+3)
        } else {
            select pixel (xk+1, yk-1)
            set pk+1 = pk + 2xk – 2yk +5
        }

    Step 5: Move each calculated pixel position (x, y) by center (xc, yc) as:
        x = x + xc
        y = y + yc
    
    Step 6: Determine symmetry points on the other seven octants:
    
    Step 7: End