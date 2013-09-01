Barrett Model
=============

This repository contains Barrett WAM & BHand-280 CAD and modular URDFs with inertial properties.

### Conventions

* `PREFIX/base_yaw_joint`

### Examples

To create a 7-DOF WAM with a Barrett Hand:

```xml
<xacro:wam_7dof prefix="wam_left" parent_link="bench_link" xyz="0.02 0.46 1" rpy="${PI} ${-PI/2} 0"/>
<xacro:bhand prefix="wam_left" parent_link="wam_left/wrist_palm_link" xyz="0 0 0.06" rpy="0 0 0"/>
```
