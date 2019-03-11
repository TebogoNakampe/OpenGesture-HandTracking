# OpenGesture 0.0.1v
Platform | Build Status |
-------- | ------------ |
Qt5 | [![Build status](https://ci.appveyor.com/api/projects/status/swutsp1bjcc56q64/branch/master?svg=true)](https://ci.appveyor.com/project/ddiakopoulos/hand-tracking-samples/branch/master)

<p align="center">
  <img width="460" height="300" src="https://raw.githubusercontent.com/TebogoNakampe/OpenGesture/master/assets/OpenGesture.png">
</p>
     
## Audience

The code in this repository is authored for computer-vision and machine-learning students and researchers interested in developing hand gesture applications using Intel® RealSense™ D400 depth cameras. 

This project provides C++ code to demonstrate Hand Gestures via depth data from Intel® RealSense™ depth cameras.

The software provided here works with the currently available Intel® RealSense™ D400 depth cameras supported by librealsense2. OpenGesture is experimental code and not an official Intel® product.

## OpenGesture

* [RealSense OpenGesture](https://github.com/TebogoNakampe/OpenGesture/blob/master/src/main.cpp) - This is the reference implementation using OpenCV and RealSense D400 series


# OpenGesture Hardware and Software

XRDrive is an inference-based application supercharged with power-efficient Intel® processors and Intel® Processor Graphics on a laptop.

1. ZenBook UX430
2. Intel Core i7 8th Gen
3. 16 GB DDR4 RAM
4. 512 SSD Storage
5. Intel RealSense D435
6. Ubuntu 16.04 LTS
7. IntelOpenVINO Toolkit
8. Realsense SDK 2
9. OpenCV
10. Qt5

## Environment Setup
* Install [OpenVINO™ Toolkit](https://software.intel.com/en-us/openvino-toolkit) ([guide](https://software.intel.com/en-us/articles/OpenVINO-Install-Linux))<br>
    	**Note**: Please use  *root privileges* to run the installer when installing the core components.
* Install OpenCL Driver for GPU
	```bash
	cd /opt/intel/computer_vision_sdk/install_dependencies
	sudo ./install_NEO_OCL_driver.sh
	```
* Install Intel® RealSense™ SDK 2.0 [(tag v2.14.1)](https://github.com/IntelRealSense/librealsense/tree/v2.14.1)<br>
	* [Install from source code](https://github.com/IntelRealSense/librealsense/blob/v2.14.1/doc/installation.md)(Recommended)<br>
	* [Install from package](https://github.com/IntelRealSense/librealsense/blob/v2.14.1/doc/distribution_linux.md)<br>
* [Build OpenCV from Source](https://docs.opencv.org/trunk/d7/d9f/tutorial_linux_install.html):Please use git checkout 3.4 to use version 3.4
* [Install Qt5 for Ubuntu](https://wiki.qt.io/Install_Qt_5_on_Ubuntu)


Note that the inference engine backend i used by default since OpenCV 3.4.2 (OpenVINO 2018.R2) when OpenCV is built with the Inference engine support, so the call above is not necessary. Also, the Inference engine backend is the only available option (also enabled by default) when the loaded model is represented in OpenVINO™ Model Optimizer format.
       ```


# 1. Research previous and current work on Hand Gestures

* Xinghao Chen: awesome-hand-pose-estimation,
* 3DiVi: Nuitrack 3D Gestures,
* Eyesight Embedded Computer Vision
* Carnegie Mellon University OpenPose: webcam
* Microsoft hololens: 3D sensor
* Microsoft hand tracking: 3D sensor
* Leap Motion: 3D sensor
* Mano Motion: smartphone camera
* PilotBit Mobile Hand Tracking: 3D sensor

## 2. Defining hand gestures.
Horns Sign                 |  Peace Sign
:-------------------------:|:-------------------------:
![](https://raw.githubusercontent.com/TebogoNakampe/OpenGesture/master/assets/a4g.png)  |  ![](https://raw.githubusercontent.com/TebogoNakampe/OpenGesture/master/assets/peace.png)

