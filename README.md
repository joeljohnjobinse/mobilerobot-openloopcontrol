# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:
Import robot module and camera module from robomaster package
<br/>

Step2:
Import the time module
<br/>

Step3:
Initialize the robot using ep_robot.initialize
<br/>

Step4:
Start video streaming
<br/>

Step5:
Enter the directions in coordinates and the distance it should travel depending on the path it is supposed to follow
<br/>

Step6:
Enter the color code the LED's of the robot should display at each stop
<br/>

Step7:
Once the final point is reached, use time.sleep to put the robot to sleep
<br/>

Step8:
Use ep.robot.close to shut the robot down
<br/>

## Program
```python
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

    ep_chassis.move(x=0.5, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=15, xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0, y=2.2, z=0, xy_speed=0.9).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=128,effect="on")

    ep_chassis.move(x=0, y=0, z=175).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=90,b=128,effect="on")

    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=127,effect="on")

    ep_chassis.move(x=0, y=0, z=35).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=1.4, z=0, xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=128,b=128,effect="on")

    ep_chassis.move(x=0, y=0, z=-55).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=255,effect="on")

    ep_chassis.move(x=1.2, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=128,effect="on")

    ep_chassis.move(x=0.4, y=0, z=-60, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=128,effect="on")

    ep_chassis.move(x=0.7, y=0, z=450 , xy_speed=2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=0 , xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=35,g=5,b=45,effect="on")

    ep_chassis.move(x=-0.6, y=0, z=-20 , xy_speed=0.95).wait_for_completed()
    ep_led.set_led(comp = "all",r=35,g=5,b=45,effect="on")

    ep_chassis.move(x=-2.7, y=0, z=0 , xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=180 , xy_speed=0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")



    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

![mobilerobotics](https://github.com/joeljohnjobinse/mobilerobot-openloopcontrol/assets/138955488/7da2f9c2-271c-4916-8896-b8427a2dd5fd)



<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)]((https://youtu.be/dmMFeZLrbQk?si=sMExSaGjsemkW66h))

<br/>
<br/>
<br/>
<br/>

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
