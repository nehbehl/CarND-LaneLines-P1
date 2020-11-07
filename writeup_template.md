# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 6 stages. First, I converted the images to grayscale, then I used gaussian blurring method to smooth out the edges and further used Canny edge detection algorithm to identify the edges. Later, I identified the region of my interest and created a masked image. In the end I used Hough Transform algorithm to get the left and right lanes and in the end overlaid those lines on the original image to get the final output.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by adding a logic to fetch x1, y1, x2 and y2 new values using the slope and intercept mathematical formulas.

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when there are more curved roads. 

Another shortcoming could be that if the roads are of different widths and sizes.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to further enhance the used algorithms for better tuning and performance.

Another potential improvement could be to explore other solutions in computer vision library to address the current problem set.
