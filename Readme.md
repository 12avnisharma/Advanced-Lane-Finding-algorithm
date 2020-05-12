## [Basic Lane Detection](./Advanced_Lane_finding_project.ipynb/)

# INTRODUCTION

Built an advanced lane-finding algorithm using distortion correction, image rectification, color transforms, and gradient thresholding. Identified lane curvature and vehicle displacement. Overcame environmental challenges such as shadows and pavement changes.

In this project, I have used computer vision techniques to identify lane boundaries and compute the estimate the radius of curvature given a frame of video of the road.  

# OBJECTIVE
The goals / steps of this project are the following: 
- Compute the camera calibration matrix and distortion coefficients given a set of chessboard images. 
- Apply a distortion correction to raw images. * Use color transforms, gradients, etc., to create a thresholded binary image.
- Apply a perspective transform to rectify binary image ("birds-eye view"). * Detect lane pixels and fit to find the lane boundary.
- Determine the curvature of the lane and vehicle position with respect to center. * Warp the detected lane boundaries back onto the original image. 
- Output visual display of the lane boundaries and numerical estimation of lane curvature and vehicle position. 


To achieve this, the following steps are taken:
- Computed the camera calibration matrix and distortion coefficients of the camera lens used given a set of chessboard images taken by the same camera
- Used the aforementioned matrix and coefficient to correct the distortions given by the raw output from the camera
- Use color transforms, and sobel algorithm to create a thresholded binary image that has been filtered out of unnecessary information on the image 
- Apply perspective transform to see a “birds-eye view” of the image as if looking from the sky 
- Apply masking to get the region of interest, detect lane pixels, 
- Determine the best fit curve for each lane the curvature of the lanes
- Project the lane boundaries back onto the undistorted image of the original view 
- Output a visual display of the lane boundaries and other related information 

# HOW TO USE
- You need to setup dependencies to run a Jupyter Notebook on your computer and setup a handful of packages such as `opencv`
```
import numpy as np
import cv2
import glob
import matplotlib.pyplot as plt
%matplotlib qt

from moviepy.editor import VideoFileClip
```

# Relevant Links
- Udacity's project page
- - https://github.com/udacity/CarND-Advanced-Lane-Lines

# RELEVANT FILES

### Video Output
- Youtube Link to the video output: https://www.youtube.com/watch?v=YZHnHehf9kA
- Youtube Link to Harder video output: https://www.youtube.com/watch?v=9iEn2jB9TeU 
