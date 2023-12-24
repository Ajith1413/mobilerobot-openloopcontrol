# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

# Step1:
 Use from robomaster import robot.

# Step2:
 Choose the x,y,z - axis movement distance(meters). 


# Step3:
 Give ep_chassis.move to move straight.


# Step4:
 Give time.sleep() for a break.

# Step5:
 Give ep_chassis.drive_speed to have a circular movement.

## Program
```python
    ## Write your code here

 #Developed by: AJITH KUMAR A
 #Register Number: 23002150   

from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0.4, y=0, z=75, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=192,g=192,b=192,ef…



    
    ep_robot.close()
```

## MobileRobot Movement Image:

![image](https://github.com/Ajith1413/mobilerobot-openloopcontrol/assets/139842524/d123e101-421f-433e-ae9b-33876df855d0)


## MobileRobot Movement Video:

https://youtube.com/shorts/DN7oSsqC-tU?feature=shared

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
