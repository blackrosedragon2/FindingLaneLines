# **Finding Lane Lines on the Road** 

## Writeup

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Descrption of my pipeline

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I added a gaussian blur after which I applied a canny edge detection algorithm followed by masking edges outside of my region of interest. I then applied a hough line transform and drew lines on the greyscale image. Then i merged the color image with my line to produce the final output

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by taking the mean of their slopes calculated ymin and ymax and then drawing a line between them

### 2. Shortcomings with my current pipeline


One potential shortcoming would be what would happen if the road is curved, this does not support polynomial functions hence any type of curve will give the wrong output

Another shortcoming could be if the lane lines are not clearly visible

### 3. Possible improvements to pipeline

A possible improvement would be to add polynomial curve fitting rather than drawing lines

