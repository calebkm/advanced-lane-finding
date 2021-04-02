## Advanced Lane Finding

GOAL​: Given a sample video showing a vehicle driving down the highway, detect and display the approximate lane position, including information about the radius of curvature of the road and the vehicle distance from center of the lane.

STEPS​: In order to find the lane, here are the steps in the processing pipeline:
1) Calibrate the camera to find the ​calibration matrix and distortion coefficients.
2) Using the camera calibration, undistort the video frame.
3) Detect edges in each video frame using a combination of color and gradient
thresholds to generate a binary image.
4) Create a “birds eye view” from the binary image of each video frame by transforming the image perspective.
5) Use a sliding window (or prior measurement) to find the right and left lane lines.
6) Fit each lane line to a polynomial to determine the road radius of curvature.
7) Determine the vehicle off set from center using the left and right lane lines averaged compared to the center of the image frame.
8) Merge the found lane lines back on to the original image frame and include the curvature and centering data.

Have a look at the final [video output!](output_videos/project_video.mp4)