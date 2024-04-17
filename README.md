# Object_Detection
Yolov5-opencv
# OPENCV build tip: Follow this tutorial: https://qengineering.eu/install-opencv-on-jetson-nano.html
Reason: Jetson Nano has a 4 GB Ram, which is not enough to support the build process.
# How to use:
run: cmake . && make
# Example code to set up opencv gstream for any camera(BGR img conversion):
VideoCapture cap("nvarguscamerasrc ! video/x-raw(memory:NVMM), width=(int)3264, height=(int)2464,format=(string)NV12, framerate=(fraction)21/1 ! nvvidconv ! video/x-raw, format=(string)BGRx ! videoconvert ! appsink");
# Enable all cpu cores
sudo nvpmodel -m 0
