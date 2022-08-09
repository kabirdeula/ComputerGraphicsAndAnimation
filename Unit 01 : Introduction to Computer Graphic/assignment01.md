# Assignment 1

<p style="text-align: justify">
1. Suppose a system has resolution of 640 x 480. What is the size of the frame buffer(in KB) to store 24 bit per pixel.
</p>

    Here,
    resolution = 640 x 480
    bit depth = 24 bit
    Total Size = resolution x bit
               = 640 x 480 x 24
                 --------------
                    8 x 1024
               = 900 KB.

<p style="text-align: justify">
2. Consider a system with resolution 1280 x 1024. What is the size of the frame buffer(in MB) to store 12 bit per pixel.
</p>

    Here, 
    resolution = 1280 x 1024
    bit depth = 12 bit
    Total Size = resolution x bit
               = 1280 x 1024 x 12
                 -----------------
                  8 x 1024 x 1024
               = 1.875 MB

<p style="text-align: justify">
3. Suppose the RGB raster system is to be designed using an 8 inch x 10 inch screen with a resolution of 100 pixels per inch in each direction. If we want to store 6 bit per pixel in the frame buffer. How much storage (in KB) do we need in the frame buffer.
</p>

    Here, 
    resolution = 8 x 100 x 10 x 100
    bit depth = 6 bit
    Total Size = 8 x 100 x 10 x 100
                --------------------
                  8 x 1024 x 1024
               = 0.572 MB