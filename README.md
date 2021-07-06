# E-DRONE DELIVERING SYSTEM

##Working Video Demonstration- [Click Here](https://youtu.be/giWqdSLqcoo)

## INTRODUCTION
Drones or Unmanned Aerial Vehicles (UAVs) come in two variants – fixed-wing and rotary drones. Rotary drones or multirotor drones consist of various configurations, and some common ones are the helicopter, four-rotor quadcopter, and six-rotor hex copter. Each rotor type has a specific usage and is useful for specific applications. The commonly used type of multirotor is the quadcopter (often shortened to quad). This is because it is a very mechanically, simple system. In quads, each motor spins in the opposite direction of the adjacent motor.

In order to maintain its 'pose' in-flight and stay stable, a quadcopter relies heavily on sensors that constantly monitor the quad's 'attitude.' These sensors provide feedback to the quad using which the flight controller makes corrections in the motor spin speed and thus adjusting and shifting the quad in flight so that it remains stable.

## Sensor Models Used

<strong>Inertial Measurement Unit (IMU):</strong> This sensor is a combination of an accelerometer,which measures linear acceleration (i.e., in X, Y & Z axis relative to the sensor) and agyroscope which measures angular velocity in three axes, roll, pitch, and yaw.Typically a magnetometer is also present, which by measuring the earth's magneticfield, serves to give a reference direction.

<strong>Barometer:</strong> Barometers are used to measure the air pressure and hence help flightcontrollers to predict the height of the quad from the ground. Barometers generallycome in handy when the quad is at large enough heights.

<strong>Ultrasonic Sensor:</strong>Ultrasonic sensors help give a precise height of the quad fromthe ground. Ultrasonic sensors are extremely useful when flying a quad within 50cmfrom the ground. Beyond that height, it is recommended to rely on the barometer forestimating the quad height with respect to the ground.

<strong>Time of Flight Sensor:</strong>It is a distance sensor that uses a laser to estimate thedistance.

<strong>GPS Reciever:</strong>Incorporating this on the UAV enables it to locate itself using theGlobal Positioning System and other satellite positioning systems.

## CONTROL SYSTEM
<p align="center">
  <img src="https://github.com/AbhisekOmkar/E-Drone/blob/main/Images/Map%20Control.jpg">  
</p>

## QR Detection using Python
There are various libraries by which you can scan a QR with a single line of code (just passing an image to these libraries). Example pyzbar is such a library that is used to detect QR codes.

## Detection of Launchpad using OpenCV
 Here is a short script to detect the landing marker and display it
 ```
 import cv2 
 from matplotlib import pyplot as plt 
 logo_cascade = cv2.CascadeClassifier('data/cascade.xml') 
 img = cv2.imread('test_1.png')  # Source image 
 gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY) 
 logo = logo_cascade.detectMultiScale(gray, scaleFactor=1.05) 
 for (x, y, w, h) in logo: 
    cv2.rectangle(img, (x, y), (x + w, y + h), (255, 255, 0), 2) 
 plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB)) 
 plt.show() 
```

## ROS Nodes for Drone Simulation
We have successfully complied ROS nodes for Drone Simulation. Here is the link for the same:<br>
[ROS Nodes Python Files](https://github.com/AbhisekOmkar/E-Drone/tree/main/Codes)
