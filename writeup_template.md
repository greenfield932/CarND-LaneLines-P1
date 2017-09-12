# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)
[sourceimg]: ./writeup_data/source.jpg
[image1]: ./writeup_data/step1.png
[image2]: ./writeup_data/step2.png
[image3]: ./writeup_data/step3.png
[image4]: ./writeup_data/step4.png
[image5]: ./writeup_data/step5.png
[image6.1]: ./writeup_data/step6.1.png
[image6.2]: ./writeup_data/step6.2.png
[image7]: ./writeup_data/step7.png

---

### Reflection

### 1. Pipeline description

Initial image

![alt text][sourceimg]

My pipeline consisted of 7 steps.

Step1. Make a color split with treshold for yellow (in HSV space) and white (in RGB space) colors

![alt text][image1]

Step2. Apply blur to result image to make mask more smooth, this helps to remove some noise and prepare image for canny algorithm

![alt text][image2]

Step3. Convert image to grayscale

![alt text][image3]

Step4. Apply Canny algorithm

![alt text][image4]

Step5. Prepare region of interest

![alt text][image5]

Step6. Apply Hough analysis to find lines

![alt text][image6.1]

Filter out bad lines (lines that close to horizontal), split all found lines in 2 groups by their slope (left and right lines with positive and negative slope), make average lines for left and right group

![alt text][image6.2]

Step7. Draw transparent lines by combining initial image and resulted lines image with blending technique

![alt text][image7]
### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
