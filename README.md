#**Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### 1. My pipeline.

First, I selected the color of the desired region and then reduces noise to identify the boundaries of the region. After that, I applied the Grayscale transform to get image in one color and then applied Gaussian blur.
Then that image grayscaled image passed to canny edge detection algorithm. After getting Edges and getting lane line region, isolated features of particular shape within an image is calulated using Hough Transform.

Before applying this pipeline, I passed grayscaled image after applying gaussion to Canny Edges detection algorithm, that was working fine too but that was not working fine on curvey lane lines. See below video:
[![Watch the video](https://i.ytimg.com/vi/ca4LhJGvoYo/hqdefault.jpg)](https://youtu.be/ca4LhJGvoYo)

Final Video After applying pipeline
[![Watch the video](https://i9.ytimg.com/vi/2Iw32hkBwUU/hqdefault.jpg?sqp=CLTRuOIF&rs=AOn4CLCqhNRAVlNU1RZoHviSOhFpVddzWA)](https://youtu.be/2Iw32hkBwUU)

### 2. Identify potential shortcomings with your current pipeline

One potential shortcoming would be robustious, it can only detect the line in the center of the screen. 

Another shortcoming could be that it will fail when entering into curve or circumstance becoming complex, it could not detect any line.

### 3. Suggest possible improvements to your pipeline

A possible improvement would be to change the parameters to overcome some situations. Also improvising the lane lines detection algorithm can help us in improving it more further.