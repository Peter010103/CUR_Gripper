# CUR_Gripper
Cambridge University Robotics > Robocup Rescue > GripperV4

- URDF file produced using https://github.com/yanshil/Fusion2PyBullet
- Visualisation graphs produced using https://github.com/yanshil/Joint2Graphviz

The Fusion scripts from the above links are in the scripts folder for convenience.

# Hardware Overview
- 6 x ROBOTIS AX-12A actuators used for Gripper, Roll & Yaw Axis & Pitch Axis(?)
- 3D printed in PETG (STL files in [assets](catkin_ws/src/gripperv4/assets))

Follows a common 4-bar linkage (parallelogram) mechanism for gripping action. The wrist axes are designed to be able to rotate a full 360 degrees (must ensure long enough wires are used !)

<p align="center">
  <img src="assets/preview.png" width="500">
</p>

# URDF Layout
<p align="center">
  <img src="assets/urdf.png" width="400">
</p>

To conform with the URDF format, some components were removed to make the tree 'open-loop' in RViz. Dependent joints between the servo arm (link1) and the finger (link3) were added ([dependent_joints.yaml])(catkin_ws/src/gripperv4/config/dependent_joints.yaml) instead to mimic the motion of the parallelogram mechanism.

# RViz Simulation
<p align="center">
  <img src="assets/RViz.png" width="600">
</p>
