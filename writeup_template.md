# **Finding Lane Lines on the Road** 

## My Pipeline consists of following steps

**Step1:** _Greyscale of the image_
**Step2:** _Apply gaussian blur_
**Step3:** _Find Canny edge_
**Step4:** _Find ROI and apply mask_
**Step5:** _Use Probabilistic Hough Line Transform to detect straight lines_
**Step6:** _Finally Drawline function which draws lines on the input video or image after detecting missing lines._
**Step7:** _I found the tuning parameters for hough lines and canny edges by trail and error method._

### Reflection

### 1. The draw_lines() function.

In order to draw a single line on the left and right lanes, i modified the draw_lines() function by separating line segments by their slope **((y2-y1)/(x2-x1))** to decide which segments are part of the left line vs. the right line. After identifying the slope, i determined to find y-intercept of the filtered lines by solving for _b_ in **y = mx + b**. To make left and right line stable i find the averages of 30 previous frames


### 2. Identify potential shortcomings with your current pipeline


Lane line detector is far from perfect. It can't detect lanes outside the perfect conditions or even curved lines.

May be my tuning parameters & draw line functions can be improved so that it can predict lane lines over steep curves.

I also see sometimes my lane goes beyond the lane markings and this has to be improved.


### 3. Suggest possible improvements to your pipeline
My tuning parameters has to improved. I found by trail and error method, but i should adopt a automated way or pass inputs to the algorighm to get better tunning parameters easily.


