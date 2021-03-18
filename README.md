# cabin_auv_simulation
Simulation environment, with gazebo&ros, for the project [cabin_auv_ws](https://github.com/cabinx/cabin_auv_ws), a simple demo for rov/auv underwater object tracking based on ros.
![image](https://github.com/cabinx/cabin_auv_simulation/blob/main/media/test_image.png)
A test video can be found in the media folder.

Attention:

the simulation rely on the [uuv_simulator](https://github.com/uuvsimulator/uuv_simulator).

[darknet_ros](https://github.com/leggedrobotics/darknet_ros) is also needed for tracking.

Install:
```
mkdir -p catkin_ws/src
cd catkin_ws/src
git clone https://github.com/uuvsimulator/uuv_simulator.git
git clone https://github.com/cabinx/cabin_auv_simulation.git
cd ..
catkin_make
```

Test:
1. roslaunch bluerov2h_gazebo bluerov2h_origin.launch
2. roslaunch cabin_controllers gazebo_sim.launch
3. start your darknet_ros application
4. rosrun rqt_reconfigure rqt_reconfigre
5. tuning the parameter, turn on the tracking_switch in the rqt_reconfigre panel

The robot can also be controlled by a joystick with the package cabin_teleop.
