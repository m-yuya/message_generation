# Message header file generation from .msg

This code based on ROS message_generation.

## Abstract

### Main file
- msg_gen.py: based on /ros_comm/clients/roscpp/rosbuild/scripts/msg_gen/py in https://github.com/ros/ros_comm.git

### Imported packages
[ROS: roslib](https://github.com/m-yuya/ros_packages)
- roslib: based on https://github.com/ros-infrastructure/rospkg.git
- rospkg: based on https://github.com/ros-infrastructure/rospkg.git
- catkin: based on https://github.com/ros/catkin.git
- catkin_pkg: based on  https://github.com/ros/catkin.git

## How to use

1. Set the path of imported packages such as:

[msg_gen.py]: around line 3:
``` python
sys.path.append(os.path.dirname(os.path.abspath(__file__)) + '/../../ros_packages')
```

2. Run module such as:

``` bash
# message header files (.h) are generated in generated_files directory
$ python msg_gen.py std_msgs/String.msg tutorials/user.msg
--- Generating message header file (.h) in ./msg_gen from .msg ---
--- $ python gen_msg.py [.msg path] [.msg path] ... ---

std_msgs/String.h
tutorials/user.h

---  Completed!! ---
```
