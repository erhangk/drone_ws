# Installation

Clone the repo:

```
git clone https://github.com/gtu-ros/drone_ws.git
```

or

```
git clone https://<oauth-key-goes-here>@github.com/gtu-ros/drone_ws.git
```

Initialize the drone workspace:

```
cd ~/drone_ws
catkin init
```

Build workspace

```
cd ~/drone_ws
catkin build
```

Add setup.bash to your .bashrc

```
echo "source ~/drone_ws/devel/setup.bash" >> ~/.bashrc
```

Update global variables

```
source ~/.bashrc
```

You can read ROS_Guides folder ROS Noetic guides.

This repo was clonned from https://github.com/erhangk/ROS_Guides.git

### Installing gazebo tools

Gazebosim link:

http://models.gazebosim.org/

Gazebo camera plugin guides:

https://classic.gazebosim.org/tutorials?tut=ros_gzplugins

https://answers.ros.org/question/210695/adding-a-camera-to-a-model-in-gazebo-beginner/

### Running Simulation

```
roslaunch ardupilot_gazebo iris_with_roscam.launch
```

Check if camera topics are being published:

```
rostopic list
```

You should see something like this:

```
erhangk@erhan-Acer:~$ rostopic list
/clock
/gazebo/link_states
/gazebo/model_states
/gazebo/parameter_descriptions
/gazebo/parameter_updates
/gazebo/performance_metrics
/gazebo/set_link_state
/gazebo/set_model_state
/roscam/cam/camera_info
/roscam/cam/image_raw
/roscam/cam/image_raw/compressed
/roscam/cam/image_raw/compressed/parameter_descriptions
/roscam/cam/image_raw/compressed/parameter_updates
/roscam/cam/image_raw/compressedDepth
/roscam/cam/image_raw/compressedDepth/parameter_descriptions
/roscam/cam/image_raw/compressedDepth/parameter_updates
/roscam/cam/image_raw/theora
/roscam/cam/image_raw/theora/parameter_descriptions
/roscam/cam/image_raw/theora/parameter_updates
/roscam/cam/parameter_descriptions
/roscam/cam/parameter_updates
/rosout
/rosout_agg
```
