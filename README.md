##Line Following Robot Simulation
This project simulates a line following robot using OpenCV and a PID controller.

#Overview
The simulation creates a track with a diagonal line. The robot (red circle) is supposed to follow the line. The robot uses a PID controller to adjust its vertical position based on the error from the line.

#Code Explanation
The track is a white image of size 600x400.
A black line is drawn from (50,350) to (550,50) with a thickness of 10.
The robot starts at the beginning of the line (50,350).
In each iteration, the robot captures a region of interest (ROI) around its current position (5 pixels above and below, 50 pixels to the left and right).
The moments of the ROI are calculated to find the center of the line.
The error is the horizontal distance between the center of the line and the center of the ROI.
The PID controller computes a correction to adjust the robot's vertical position.
The robot moves with a base speed in the x-direction and the correction in the y-direction.

#PID Tuning
The PID constants are set as:
Kp = 0.5
Ki = 0.0
Kd = 0.1
These can be adjusted to improve the tracking performance.

#Technologies Used:
OpenCV
NumPy

