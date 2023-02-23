# Hand Gesture Controlled UAV (Simulation)

The repository simulates a quadcopter UAV with hand gesture control using mediapipe. 

# Installation 

1. [Ardupilot and MAV Proxy ](https://github.com/2ashishmohan/-Hand-Gesture-Controlled-UAV-Ardupilot-ROS-Dronekit-/blob/main/Ardupilot%20and%20MAVProxy.md) 

ArduPilot is an open-source autopilot software suite designed to control unmanned aerial vehicles (UAVs). It is compatible with a wide range of hardware platforms and features a rich set of features for autonomous flight, including GPS-based navigation, waypoint following, and advanced control algorithms. ArduPilot is highly customizable, allowing users to modify the code to suit their specific needs.

MAVProxy (MAVLink Proxy) is a lightweight communication tool for drones that allows for real-time monitoring and control of UAVs. It acts as a bridge between the ground control station (GCS) and the UAV, forwarding MAVLink messages between the two. MAVProxy can be used to control UAVs directly from the command line or via a GUI, and supports a range of GCSs and UAV platforms.

Together, ArduPilot and MAVProxy form a powerful combination for autonomous drone operation. ArduPilot provides the underlying autopilot functionality, while MAVProxy allows for real-time monitoring and control of the UAV. This combination allows users to execute complex autonomous flight missions while retaining full control over the drone in case manual intervention is required.

2. [ Gazebo and Ardupilot Plugin](https://github.com/2ashishmohan/-Hand-Gesture-Controlled-UAV-Ardupilot-ROS-Dronekit-/blob/main/Gazebo%20and%20ArduPilot%20Plugin.md)

3. [ Dronekit - Python](https://github.com/2ashishmohan/-Hand-Gesture-Controlled-UAV-Ardupilot-ROS-Dronekit-/blob/main/Dronekit-Python.md)

DroneKit is an open-source software development kit (SDK) that enables developers to create drone applications using Python programming language. The SDK is built on top of the MAVLink protocol, which is a lightweight messaging protocol designed for communication between unmanned vehicles and ground control stations.

DroneKit provides a high-level API for controlling and monitoring drones, including features such as vehicle control, mission planning, telemetry monitoring, and data logging. It can be used with a wide range of popular drone platforms, including DJI, 3DR, and Pixhawk.

4. [ Google Mediapipe ](https://google.github.io/mediapipe/getting_started/install.html#installing-on-debian-and-ubuntu)

MediaPipe is a popular open-source framework developed by Google that provides a set of cross-platform, customizable, and scalable building blocks for the development of computer vision and machine learning applications. It includes a variety of pre-built algorithms and models for tasks such as face detection, pose estimation, hand tracking, object detection, and segmentation, among others.

Mediapipe Hand Tracking is a computer vision-based module that detects and tracks the hand movements in real-time using a deep learning neural network model. Developed by Google's Mediapipe team, this module is widely used in various applications like virtual reality, gesture recognition, sign language translation, robotics, and more. The hand landmarks detected by the module include the fingertip, the base of the finger, and the joints in between. These landmarks are used to estimate the hand pose and track its movements over time. The module also provides additional features like hand segmentation, handedness classification, and tracking stability metrics.

![Hand Landmark ](HandLandmarks.png) 


# Running the Simulation

Open a terminal go to ardupilot repository and launch the ardupilot instance by running

```
sim_vehicle.py -v ArduCopter -f gazebo-iris --console
``` 

In another, second terminal run Gazebo

```
gazebo --verbose ~/ardupilot_gazebo/worlds/iris_arducopter_runway.world
```

And on the third terminal, run the Hand gesture control python script

```
python3 HandTrackingDemo.py
```







