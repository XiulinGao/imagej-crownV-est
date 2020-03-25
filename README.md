imagej-crownV-est
=================

This is the workflow I built to estimate tree crown volume from 2D images of the tree crown taken from the four cardinal directions with
using both ImageJ and R.




Procedure
----------


1. Manually define the contour and vertical axis of each half of a tree crown using ImageJ by polygon selection, and save the coordinates of vertices of the polygon. Scale should be calibrated beforehand.

![Fig.1] (/Users/gaoxiulin/fig1.png)


2. Automatically calculate area and centroid (x, y) for each of the non-self-intersecting closed polygon in R.  See [ref](https://www.seas.upenn.edu/~sys502/extra_materials/Polygon%20Area%20and%20Centroid.pdf) 



3. Estimate volume based on [Pappus's centroid theorem](https://mathworld.wolfram.com/PappussCentroidTheorem.html) by rotating the lamina around the vertical axis.


4. Average the two estimated volume for each image and then average four for one tree sample. 


*note*: I'm not familiar with ImageJ macro language, so step 1 is still manual and can be tedious if one have a large amount of images to process. Feel free to improve step 1 !

