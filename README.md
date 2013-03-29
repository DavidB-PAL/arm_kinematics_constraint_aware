### Forked ROS Package: arm_kinematics_constraint_aware

This is a fork of the ROS Fuerte Ubuntu package installation of arm_kinematics_constraint_aware, <br>
from the arm_navigation stack. <br>

Fuerte branch: <br>
https://kforge.ros.org/armnavigation/armnavigation/file/ebdb3ee14a58/

These fixes & modifications are for robots other than the PR2, but these changes have been tested to not break the simulated PR2 robot in ROS Fuerte Gazebo. <br>
-- David Butterworth
<br>

<br>
**Changelist:**

 - Fixed a segmentation fault. <br>
The fk_link_names and pose_stamped members of the response in getPositionFK aren't allocated before use. <br>
This fix originally reported: <br>
https://code.ros.org/trac/ros-pkg/ticket/5497 <br>
https://code.ros.org/trac/ros-pkg/ticket/5567

 - An enhancement, to restore the ability to use the FK (Forward Kinematics) routine from your kinematics plugin. <br>
Normally, FK is now handled by ROS TF, not your kinematics plugin!<br>
With this fix, you can launch the 'arm_constraint_kinematics_aware' node and specify an optional ROS Parameter 'use_plugin_fk=true'
Reported at: <br>
https://code.ros.org/trac/ros-pkg/ticket/5586


