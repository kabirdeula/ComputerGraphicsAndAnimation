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