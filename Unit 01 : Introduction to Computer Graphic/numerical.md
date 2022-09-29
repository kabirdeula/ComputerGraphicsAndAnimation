# Numerical Problems and Solutions

## 1. Suppose a system has resolution of 640 x 480. What is the size of the frame buffer(in KB) to store 24 bit per pixel.

    Here,
    resolution = 640 x 480
    bit depth = 24 bit
    Total Size = resolution x bit
               = 640 x 480 x 24
                 --------------
                    8 x 1024
               = 900 KB.

---

## 2. Consider a system with resolution 1280 x 1024. What is the size of the frame buffer(in MB) to store 12 bit per pixel.

    Here, 
    resolution = 1280 x 1024
    bit depth = 12 bit
    Total Size = resolution x bit
               = 1280 x 1024 x 12
                 -----------------
                  8 x 1024 x 1024
               = 1.875 MB.

---

## 3. Suppose the RGB raster system is to be designed using an 8 inch x 10 inch screen with a resolution of 100 pixels per inch in each direction. If we want to store 6 bit per pixel in the frame buffer. How much storage (in KB) do we need in the frame buffer.

    Here, 
    resolution = 8 x 100 x 10 x 100
    bit depth = 6 bit
    Total Size = 8 x 100 x 10 x 100
                --------------------
                  8 x 1024 x 1024
               = 0.572 MB.

---

## 4. Find out the DDA with the given points (1, 5) and (7, 2).

    Given,
    x1 = 1                      y1 = 5
    x2 = 7                      y2 = 2

    dx = x2 - x1                dy = y2 - y1
       = 7 - 1                     = 2 - 5
       = 6                         = -3

    Here,
    |dx| > |dy|, |6| > |3| true

    So, step-length = |dx| = 6

                       dx          6     
    x-increment =  ----------- =  --- = 1
                   step-length     6

                       dy          -3     
    y-increment =  ----------- =  ----- = -0.5
                   step-length      6

    The intermediate pixel position are shown in the following table:

  |   k   | xk + 1 | yk + 1 | (xk + 1, yk + 1) | round |
  | :---: | :----: | :----: | :--------------: | :---: |
  |   0   |    1   |    5   |       1, 5       | 1, 5  |
  |   1   |    2   |   4.5  |       2, 4.5     | 2, 4  |
  |   2   |    3   |    4   |       3, 4       | 3, 4  |
  |   3   |    4   |   3.5  |       4, 3.5     | 4, 3  |
  |   4   |    5   |    3   |       5, 3       | 5, 3  |
  |   5   |    6   |   2.5  |       6, 2.5     | 6, 2  |
  |   6   |    7   |    2   |       7, 2       | 7, 2  |

---

## 5. Find out the DDA with the given points (1, -6) and (4, 4).

    Given,
    x1 = 1                      y1 = -6
    x2 = 4                      y2 = 4

    dx = x2 - x1                dy = y2 - y1
       = 4 - 1                     = - 6 - 4
       = 3                         = -10

    Here,
    |dx| > |dy|, |3| > |10| false

    So, step-length = |dy| = 10

                       dx           3     
    x-increment =  ----------- =  ------ = 0.3
                   step-length      10

                       dy           10     
    y-increment =  ----------- =  ------ = 1
                   step-length      10

    The intermediate pixel position are shown in the following table:

  |   k   | xk + 1 | yk + 1 | (xk + 1, yk + 1) | round |
  | :---: | :----: | :----: | :--------------: | :---: |
  |   0   |    1   |   -6   |       1, -6      | 1, -6 |
  |   1   |   1.3  |   -5   |       1.3, -5    | 1, -5 |
  |   2   |   1.6  |   -4   |       1.6, -4    | 1, -4 |
  |   3   |   1.9  |   -3   |       1.9, -3    | 1, -3 |
  |   4   |   2.2  |   -2   |       2.2, -2    | 2, -2 |
  |   5   |   2.5  |   -1   |       2.5, -1    | 2, -1 |
  |   6   |   2.8  |    0   |       2.8, 0     | 2, 0  |
  |   7   |   3.1  |    1   |       3.1, 1     | 3, 1  |
  |   8   |   3.4  |    2   |       3.4, 2     | 3, 2  |
  |   9   |   3.7  |    3   |       3.7, 3     | 3, 3  |
  |   10  |    4   |    4   |       4, 4       | 4, 4  |

---

## 6. Digitize a line end points (10, 15) and (15, 18) using BSA algorithm.

    Given,
    x1 = 10                      y1 = 15
    x2 = 15                      y2 = 18

    Δx = |x2 - x1|                 Δy = |y2 - y1|
       =  15 - 10                     =  18 - 15
       =  5                           =  3

           y2 - y1      Δy       3
    |m| = --------- = ------ = ----- = 0.6 < 1
           x2 - x1      Δx       5
    
    P0 = 2Δy - Δx
       = 2 * 3 - 5
       = 1

    Plot (x1, y1) = (10, 15)

    Intermediate pixels calculation and decision parameter are shown in table below:
  
  |   k   |   Pk  | xk + 1, yk + 1 |
  | :---: | :---: | :------------: |
  |   0   |   1   |     11, 16     |
  |   1   |   -3  |     12, 16     |
  |   2   |   3   |     13, 17     |
  |   3   |   -1  |     14, 17     |
  |   4   |   5   |     15, 18     |

## 7. Digitize a line end points (20, 10) and (30, 18) using BSA algorithm.

    Given,
    x1 = 20                      y1 = 10
    x2 = 30                      y2 = 18

    Δx = |x2 - x1|                 Δy = |y2 - y1|
       =  30 - 20                     =  18 - 10
       =  10                          =  8

           y2 - y1      Δy       8
    |m| = --------- = ------ = ----- = 0.8 < 1
           x2 - x1      Δx       10
    
    P0 = 2Δy - Δx
       = 2 * 8 - 10
       = 6

    Plot (x1, y1) = (20, 10)

    Intermediate pixels calculation and decision parameter are shown in table below:
  
  |   k   |   Pk  | xk + 1, yk + 1 |
  | :---: | :---: | :------------: |
  |   0   |   6   |     21, 11     |
  |   1   |   2   |     22, 12     |
  |   2   |   -2  |     23, 12     |
  |   3   |   14  |     24, 13     |
  |   4   |   10  |     25, 14     |
  |   5   |   6   |     26, 15     |
  |   6   |   2   |     27, 16     |
  |   7   |   -2  |     28, 16     |
  |   8   |   14  |     29, 17     |
  |   9   |   10  |     30, 18     |

## 8. Digitize a line end points (4, 10) and (10, 20) using BSA algorithm.

    Given,
    x1 = 4                       y1 = 10
    x2 = 10                      y2 = 20

    Δx = |x2 - x1|                 Δy = |y2 - y1|
       =  10 - 4                      =  20 - 10
       =  6                           =  10

           y2 - y1      Δy       10
    |m| = --------- = ------ = ----- = 1.6 > 1
           x2 - x1      Δx       6
    
    P0 = 2Δx - Δy
       = 2 * 6 - 10
       = 2

    Plot (x1, y1) = (4, 10)

    Intermediate pixels calculation and decision parameter are shown in table below:
  
  |   k   |   Pk  | xk + 1, yk + 1 |
  | :---: | :---: | :------------: |
  |   0   |   2   |      5, 11     |
  |   1   |   -6  |      5, 12     |
  |   2   |   6   |      6, 13     |
  |   3   |   -2  |      6, 14     |
  |   4   |   10  |      7, 15     |
  |   5   |   2   |      8, 16     |
  |   6   |   -6  |      8, 17     |
  |   7   |   6   |      9, 18     |
  |   8   |   -2  |      9, 19     |
  |   9   |   10  |     10, 20     |

## 9. Digitize a line end points (3, 10) and (6, 2) using BSA algorithm.

    Given,
    x1 = 3                       y1 = 2
    x2 = 6                       y2 = 10 
    
    [∴ Since y1 is greater than y2 we interchange the values from y1 to y2.]

    Δx = |x2 - x1|                 Δy = |y2 - y1|
       =  6 - 3                       =  10 - 2
       =  3                           =  8

           y2 - y1      Δy       8
    |m| = --------- = ------ = ----- = 2.67 > 1
           x2 - x1      Δx       3
    
    P0 = 2Δx - Δy
       = 2 * 3 - 8
       = -2

    Plot (x1, y1) = (3, 2)

    Intermediate pixels calculation and decision parameter are shown in table below:
  
  |   k   |   Pk  | xk + 1, yk + 1 |
  | :---: | :---: | :------------: |
  |   0   |   -2  |      3, 3      |
  |   1   |   4   |      4, 4      |
  |   2   |   -6  |      4, 5      |
  |   3   |   0   |      5, 6      |
  |   4   |   -10 |      5, 7      |
  |   5   |   -4  |      5, 8      |
  |   6   |   2   |      6, 9      |
  |   7   |   -8  |      6, 10     |
  

## 10. Digitize a line end points (1, 9) and (6, 1) using BSA algorithm.

    Given,
    x1 = 1                       y1 = 1
    x2 = 6                       y2 = 9 
    
    [∴ Since y1 is greater than y2 we interchange the values from y1 to y2.]

    Δx = |x2 - x1|                 Δy = |y2 - y1|
       =  6 - 1                       =  9 - 1
       =  5                           =  8

           y2 - y1      Δy       8
    |m| = --------- = ------ = ----- = 1.6 > 1
           x2 - x1      Δx       5
    
    P0 = 2Δx - Δy
       = 2 * 5 - 8
       = 2

    Plot (x1, y1) = (1, 1)

    Intermediate pixels calculation and decision parameter are shown in table below:
  
  |   k   |   Pk  | xk + 1, yk + 1 |
  | :---: | :---: | :------------: |
  |   0   |   2   |      2, 2      |
  |   1   |   -4  |      2, 3      |
  |   2   |   6   |      3, 4      |
  |   3   |   0   |      4, 5      |
  |   4   |   -6  |      4, 6      |
  |   5   |   4   |      5, 7      |
  |   6   |   -2  |      5, 8      |
  |   7   |   8   |      6, 9      |
  