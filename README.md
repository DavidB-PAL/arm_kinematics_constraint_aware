### Forked ROS Package: arm_kinematics_constraint_aware

This is a fork of the ROS Fuerte Ubuntu package installation of arm_kinematics_constraint_aware, <br>
from the arm_navigation stack. <br>

The Trunk has other changes that haven't been released into Fuerte yet: <br>
https://code.ros.org/svn/wg-ros-pkg/stacks/kinematics/trunk/arm_kinematics_constraint_aware/

These fixes & modifications are for robots other than the PR2, but these changes have been tested to not break the simulated PR2 robot in ROS Fuerte Gazebo. <br>
-- David Butterworth
<br>

<br>
**Changelist:**

 - Fixed a segmentation fault. <br>
&nbsp;&nbsp;&nbsp;The fk_link_names and pose_stamped members of the response in getPositionFK aren't allocated before use. <br>
&nbsp;&nbsp;&nbsp;This fix originally reported: <br>
&nbsp;&nbsp;&nbsp;https://code.ros.org/trac/ros-pkg/ticket/5497 <br>
&nbsp;&nbsp;&nbsp;https://code.ros.org/trac/ros-pkg/ticket/5567

 - An enhancement, to restore the ability to use the FK (Forward Kinematics) routine from your kinematics plugin. <br>
&nbsp;&nbsp;&nbsp;FK is now handled by ROS TF, by default. <br>
&nbsp;&nbsp;&nbsp;When you launch the 'arm_constraint_kinematics_aware' node, you can specify an optional ROS Parameter 'use_plugin_fk=true'
&nbsp;&nbsp;&nbsp;Reported at: <br>
&nbsp;&nbsp;&nbsp;https://code.ros.org/trac/ros-pkg/ticket/5586


