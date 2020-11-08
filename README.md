# **Finding Lane Lines on the Road** 



---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/solidYellowLeft.jpg

---

### Reflection

My pipeline consisted of 6 stages. First, I converted the images to grayscale, then I used gaussian blurring method to smooth out the edges and further used Canny edge detection algorithm to identify the edges. Later, I identified the region of my interest and created a masked image. In the end I used Hough Transform algorithm to get the left and right lanes and in the end overlaid those lines on the original image to get the final output.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by adding a logic to fetch x1, y1, x2 and y2 new values using the slope and intercept mathematical formulas.


![alt text][image1]


### 2. Potential shortcomings in current project


One potential shortcoming would be what would happen when there are more curved roads. 

Another shortcoming could be that if the roads are of different widths and sizes.


### 3. Possible improvements to the pipeline

A possible improvement would be to further enhance the used algorithms for better tuning and performance.

Another potential improvement could be to explore other solutions in computer vision library to address the current problem set.
