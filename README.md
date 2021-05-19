# eurobench_simulated_pendulum
ROS node to simulate the effect of a pendulum mass hitting a robot from a certain angle.

Instructions:
-------------
- Installation: After cloned just run a ```catkin_make``` on your catkin environment.
- Usage: To execute the node jst run: ```rosrun eurobench_simulated_pendulum eurobench_simulated_pendulum_node```

How it Works:
-------------
The ```eurobench_simulated_pendulum``` open a service called ```/eurobench_simulated_pendulum_node/apply_body_force``` which accepts the service defined in [EuroBenchPendulum.srv](srv/EuroBenchPendulum.srv)  with: 
- the pendulum mass
- the pendulum length
- the angle w.r.t. the vertical
- the angle on the horizontal plane (if 0.0 the pendulum hits the robot on the x coordinates)
- the time of the impact

The node makes use of the service ```/gazebo/apply_body_wrench```.
