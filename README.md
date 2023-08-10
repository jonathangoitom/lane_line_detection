# Finding Lane Lines on the Road

This repository contains a lane detection model that aims to identify and draw lane lines on individual images and video streams. The model utilizes a pipeline of computer vision techniques, including color selection, region of interest selection, grayscaling, Gaussian smoothing, Canny Edge Detection, and Hough Transform line detection. The goal of this project is to piece together a robust pipeline that can effectively detect lane lines, average/extrapolate them, and overlay them onto the original images.


## Project Overview

Lane detection is a crucial task in autonomous driving and advanced driver assistance systems. This project focuses on developing a lane detection pipeline for both images and video streams. The pipeline consists of several stages that process the input data and produce output images with detected and extrapolated lane lines.


## Pipeline Steps

The pipeline consists of the following steps:

1.   **Color Selection**: The input image is filtered to select specific colors that correspond to lane lines. This helps to enhance the visibility of the lanes.
2.  **Region of Interest Selection**: A region of interest (ROI) is defined to focus only on the area of the image where lane lines are expected. This helps to reduce noise and improve the accuracy of lane detection.
3.  **Grayscaling**: The ROI image is converted to grayscale, simplifying the data for subsequent processing stages.
4.  **Gaussian Smoothing**: A Gaussian blur is applied to the grayscale image to reduce noise and smoothen the edges. This step is essential for improving the accuracy of edge detection.
5.  **Canny Edge Detection**: The Canny edge detection algorithm is used to identify potential lane line edges in the image.
6.  **Hough Transform Line Detection**: The Hough Transform algorithm is applied to detect lines in the edge-detected image. This step identifies line segments representing the lane lines.
7.  **Lane Line Averaging and Extrapolation**: The detected line segments are averaged and extrapolated to form two lines representing the left and right lane lines.
8.  **Drawing Lane Lines**: The final step involves overlaying the detected and extrapolated lane lines onto the original image.


## Results

The output of the lane detection pipeline will encompass both images and videos in which the detected and extrapolated lane lines are superimposed onto the original frames. A reference sample video clip is provided to facilitate comparison and assess the pipeline's accuracy and effectiveness.

![Output Image](https://github.com/jonathangoitom/lane_line_detection/assets/107156253/9e450be5-9f26-4aa2-ac3c-be3ba425c478)

