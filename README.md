Barrett Model
=============

This repository contains Barrett WAM & BHand-280 CAD and modular URDFs with inertial properties.

### Joint Naming Conventions

* macro: `wam_7dof`
    * macro: `wam`
        * `PREFIX/base_yaw_joint`
        * `PREFIX/shoulder_yaw_joint`
        * `PREFIX/shoulder_pitch_joint`
        * `PREFIX/elbow_pitch_joint`
    * macro: `wam_wrist`
        * `PREFIX/wrist_yaw_joint`
        * `PREFIX/wrist_pitch_joint`
        * `PREFIX/palm_yaw_joint`

* macro: `bhand`
  * `PREFIX/finger_1/prox_joint`
  * `PREFIX/finger_1/med_joint`
  * `PREFIX/finger_1/dist_joint`
  * `PREFIX/finger_2/prox_joint`
  * `PREFIX/finger_2/med_joint`
  * `PREFIX/finger_2/dist_joint`
  * `PREFIX/finger_3/med_joint`
  * `PREFIX/finger_3/dist_joint`

### Examples

To create a 7-DOF WAM with a Barrett Hand:

```xml
<xacro:wam_7dof 
  prefix="wam_left" 
  parent_link="bench_link" 
  xyz="0.02 0.46 1" rpy="${PI} ${-PI/2} 0"/>
<xacro:bhand 
  prefix="wam_left/bhand" 
  parent_link="wam_left/wrist_palm_link" 
  xyz="0 0 0.06" rpy="0 0 0"/>
```
