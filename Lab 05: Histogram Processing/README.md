# Objective: The objective of this lab is:

## To create and apply a piece-wise linear histogram transform. 
## To create and apply contrast stretching on histograms. 
## To create and apply histogram equalization.

### Piece-wise Linear Transform: 
Piece-wise linear transformation is usually used to process a histogram in a specific way. For instance, consider a situation in which it is required from you to isolate picture elements whose gray levels fall in a pre specified range from A to B. This process can be done in various ways (such as writing a computer program in which “if” statement can isolate the pixels) but a generic approach is to create a Transformation function and then applying that transformation function using cv2.LUT or your own mapping routine.

### Contrast Stretching:
Contrast stretching is a process which involves extending a range of input histogram to an output
histogram using following formula:
![Alt text](https://github.com/talha3111997/Image_Processing/blob/master/Images/contrast%20stretching.JPG?raw=true "Contrast stretching formula")


Where Smin and Smax are the goal ranges (Lower histogram in Figure 3) and Rmin and Rmax are
the range you wish to stretch (Upper histogram in Figure 3). Since R is a range [Rmin, Rmax], a simple
mathematical can be used to find out a one-to-one mapping for Ri (Rmin <= i <=Rmax). The process is
robust enough to stretch one histogram of range [A,B] to [C,D] where both ranges can or cannot be of
same gray-level values!

In some cases, a piece-wise linear transformation function can also be created to achieve
contrast stretching (as shown in Figure 5) in which a human expert selects two points (r1,s1) and
(r2,s2) manually to enhance contrast of the image. The values of both points can also be automatically
calculated using some predefined percentage of the available histogram! (e.g. 20% dark, 60% middle
and 20% light gray-levels).
HINT: you can use CDF values to calculate the predefined percentages.

### Histogram Equalization:
Histogram equalization is a method in image processing of contrast adjustment using the
image's histogram. Histograms of an image before and after equalization. Some important
points about the exercise. <br/>
 You should apply histogram equalization on any Grayscale image.  <br/>
 You should not use the builtin histogram equalization method available in python or OpenCV  <br/>
 You should use the formula mentioned below to implement the histogram equalization.  <br/>
