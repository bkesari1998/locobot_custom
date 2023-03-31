# locobot_custom
ROS Noetic package for locobot control

## Launch files
### locobot_gazebo.launch
Launches the gazebo simulation of the locobot in the two room environment

### locobot_teleop.launch
Launches teleop control of the locobot similar to turtlebot's teleop.

## URDF
To make a URDF compatable with ROS, follow the following tutorial: 
http://classic.gazebosim.org/tutorials?tut=ros_urdf&cat=connect_ros

In summary:
Required

 * An <inertia> element within each <link> element must be properly specified and configured.

Optional

 * Add a <gazebo> element for every <link>
     * Convert visual colors to Gazebo format
     * Convert stl files to dae files for better textures
     * Add sensor plugins
 * Add a <gazebo> element for every <joint>
     * Set proper damping dynamics
     * Add actuator control plugins
 * Add a <gazebo> element for the <robot> element
 * Add a <link name="world"/> link if the robot should be rigidly attached to the world/base_link
