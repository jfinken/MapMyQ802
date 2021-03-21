# MapMyQ802
SLAM with RTAB-Map in ROS1-noetic

### Install

RTAB-Map is released as binaries in the ROS distribution.

```bash
sudo aptitude install ros-noetic-rtabmap-ros
```
### Launch

```bash

# Launches gazebo, rviz and spawns the robot
roslaunch map_my_q802 world.launch 
```

```bash
# the teleop node
rosrun teleop_twist_keyboard teleop_twist_keyboard.py 
```

```bash
# the rtab mapping node
roslaunch map_my_q802 mapping.launch 
```

### Database Analysis
[rtabmap-databaseViewer](https://github.com/introlab/rtabmap/wiki/Tools#database-viewer)
is a great tool for exploring your database when you are done generating it. It is isolated
from ROS and allows for complete analysis of your mapping session.
- Constraints View
- Graph View
- Occupancy Grid

```base
# for example
rtabmap-databaseViewer ../MapMyQ802/map_my_q802/map/rtabmap.db
```
