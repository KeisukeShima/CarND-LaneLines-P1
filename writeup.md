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

My pipeline consisted of 6 steps. First, I converted the images to grayscale, then I apply Gaussian smoosing, Canny. And I defined a four sided polygon to mask and apply it. And then, I use Hough transorm. Finally, I generated line-detected image.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by  line's slope. Then, I caliculate average of the position of the lines and draw the single lane.

<!-- If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1] -->


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the image size changed.
<!-- 
Another shortcoming could be ... -->


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to adjust masked area using their image size.
<!-- 
Another potential improvement could be to ... -->
