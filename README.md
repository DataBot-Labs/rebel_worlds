# Rebel Worlds

## Running this world directly in Gazebo without a ROS application

To open this world in Gazebo, change the directory to your ROS workspace root folder and run:

If using Gazebo Garden or later:

```bash
export GZ_SIM_RESOURCE_PATH=`pwd`/models
gz sim worlds/datafloor.sdf
```

or if using Ignition Fortress or earlier:

```bash
export GZ_SIM_RESOURCE_PATH=`pwd`/models
ign gazebo worlds/datafloor.sdf
```

## Running this world directly using ROS without a simulated robot

To launch this base Gazebo world without a robot, clone this repository and run the following commands

```bash
# build for ROS2
rosdep install --from-paths . --ignore-src -r -y
colcon build

# run in ROS2
source install/setup.sh
ros2 launch rebel_worlds rebel_worlds.launch.py
```
