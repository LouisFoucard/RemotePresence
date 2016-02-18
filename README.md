# RemotePresence
Remote presence with the Oculus Rift DK1 headset, Arduino, stereo webcams and a python interface. 

Short Description of the files:

-webcam_oculus.ipynb: This takes care gathering the images from the webcams, apply barrel transform and display the resulting stereo image.  The video feed from the webcams is warped into a oculus-compatible format using OpenCV. 

-servoControl.ipynb: This takes care of gathering sensor data from the oculus and sends the approriate commands to the 3 servos controlling the webcam's positions. Python-ovrsdk (https://github.com/wwwtyro/python-ovrsdk) is used to interface between the oculus IMU and the python script.
The Python-Arduino-Command-API library (https://github.com/thearn/Python-Arduino-Command-API) is used to send commands to the arduino controlling the servos.

The biggest problem as you can see is lag, both in the mechanical displacments and displaying the video. Upcoming updates/improvements: faster servos, run on desktop with GPU to accelerate the OpenCV processing of webcam images into a Rift compatible format.

Here is a short gif that shows the setup in action (takes a while to load):

![alt tag](https://github.com/LouisFoucard/RemotePresence/blob/master/RemotePresence.gif)
