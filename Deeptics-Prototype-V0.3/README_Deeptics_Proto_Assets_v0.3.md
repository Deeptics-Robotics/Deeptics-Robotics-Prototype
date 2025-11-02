# Deeptics Proto Asset Catalog (v0.3)

**Updated**: 2025-10-07

This release integrates the **Legged Series** (humanoids, quadrupeds, hexapod, salamander) as Deeptics‑original assets, with enriched fields: **DoF, payload, default sensors, controller presets**.

## Asset Schema
```json
{
  "asset_code": "DXQ-GHOST",
  "public_name": "Quadruped-Ghost",
  "class": "legged",
  "subtype": "quadruped-minimal",
  "status": "proto",
  "orig_views": 180,
  "deeptics_views": 0,
  "description": "Minimalist quadruped for controller prototyping and unit tests.",
  "dof": 8,
  "payload_kg": 1.5,
  "sensor_default": ["SM-IMU"],
  "controller_presets": ["gait_walk","gait_trot"]
}
```

## Asset Index
| Code | Name | Class | DoF | Payload (kg) | Default Sensors | Controllers |
|---|---|---|---:|---:|---|---|
| DXF-INSPECT | QuadRotor-Inspect | aerial | 6 | 1.5 | SM-IMU, SM-Stereo, SM-RGBD | LQR_attitude, waypoint_P, VIO_loops |
| DXF-MICRO | MicroQuad | aerial | 6 | 0.03 | SM-IMU, SM-Stereo, SM-RGBD | LQR_attitude, waypoint_P, VIO_loops |
| DXH-COMPACT | Humanoid-Compact | humanoid | 20 | 0.5 | SM-RGBD, SM-IMU, SM-Stereo | gait_walk, push_recovery, whole_body_QP |
| DXH-COMPACTP | Humanoid-CompactPlus | humanoid | 20 | 0.7 | SM-RGBD, SM-IMU, SM-Stereo | gait_walk, push_recovery |
| DXH-DRWN | Humanoid-Darwin | humanoid | 16 | 0.5 | SM-IMU, SM-RGBD | gait_walk |
| DXH-DRWNH2 | Humanoid-DarwinH2 | humanoid | 16 | 0.5 | SM-IMU, SM-RGBD | gait_walk, push_recovery |
| DXH-K2HV | Humanoid-K2HV | humanoid | 18 | 0.8 | SM-IMU, SM-RGBD | gait_walk, push_recovery |
| DXH-K3HV | Humanoid-K3HV | humanoid | 18 | 0.8 | SM-IMU, SM-RGBD | gait_walk, push_recovery |
| DXH-MINI2 | Humanoid-Mini2 | humanoid | 16 | 0.5 | SM-RGBD, SM-IMU, SM-Stereo | gait_walk, push_recovery, whole_body_QP |
| DXH-MINI2H2 | Humanoid-Mini2Hinge2 | humanoid | 16 | 0.5 | SM-IMU | gait_walk |
| DXH-MINI3 | Humanoid-Mini3 | humanoid | 16 | 0.5 | SM-RGBD, SM-IMU, SM-Stereo | gait_walk, push_recovery, whole_body_QP |
| DXH-POWER | Humanoid-Power | humanoid | 28 | 10.0 | SM-RGBD, SM-IMU, SM-Stereo, SM-LiDAR-3D | gait_walk, push_recovery, whole_body_QP, jump_control |
| DXH-RSCH2 | Humanoid-Research2 | humanoid | 20 | 1.0 | SM-RGBD, SM-IMU, SM-Stereo | gait_walk, whole_body_QP |
| DXH-SCOUT | Humanoid-Scout | humanoid | 12 | 0.3 | SM-IMU | gait_walk |
| DXL-HEX6M | Hexapod-Mantis | legged | 18 | 3.0 | SM-IMU, SM-RGBD | tripod_gait, wave_gait |
| DXL-SALA | Salamander | legged | 12 | 1.0 | SM-IMU | body_cpg, limb_cpg |
| DXQ-AGILE | Quadruped-Agile | legged | 12 | 6.0 | SM-RGBD, SM-IMU, SM-LiDAR-3D | gait_trot, gait_walk, whole_body_QP |
| DXQ-EDU | Quadruped-Edu | legged | 8 | 1.5 | SM-IMU, SM-RGBD | gait_walk |
| DXQ-GHOST | Quadruped-Ghost | legged | 8 | 1.5 | SM-IMU | gait_walk, gait_trot |
| DXQ-PET | Quadruped-Pet | legged | 8 | 2.0 | SM-IMU, SM-RGBD | gait_walk, gait_trot |
| DXA-10E | CollabArm-10e | manipulator | 6 | 10.0 | SM-RGBD, SM-IMU, SM-FT, SM-Tactile | joint_space_PD, task_space_impedance, RRT_connect, IK_solvers |
| DXA-3E | CollabArm-3e | manipulator | 6 | 3.0 | SM-RGBD, SM-IMU, SM-FT, SM-Tactile | joint_space_PD, task_space_impedance, RRT_connect, IK_solvers |
| DXA-5E | CollabArm-5e | manipulator | 6 | 5.0 | SM-RGBD, SM-IMU, SM-FT, SM-Tactile | joint_space_PD, task_space_impedance, RRT_connect, IK_solvers |
| DXA-DESK | DeskArm-N | manipulator | 6 | 1.0 | SM-RGBD, SM-IMU, SM-FT, SM-Tactile | joint_space_PD, task_space_impedance, RRT_connect, IK_solvers |
| DXA-IND4600 | IndustArm-4600 | manipulator | 6 | 60.0 | SM-RGBD, SM-IMU, SM-FT, SM-Tactile | joint_space_PD, task_space_impedance, RRT_connect, IK_solvers |
| DXA-P7 | CollabArm-P7 | manipulator | 7 | 7.0 | SM-RGBD, SM-IMU, SM-FT, SM-Tactile | joint_space_PD, task_space_impedance, RRT_connect, IK_solvers |
| DXM-OMNIARM | OmniBase+Arm | mobile_manipulator | 10 | 3.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | DWA_planner, A*_global, joint_space_PD |
| DXM-TORSO | Tiago-Class | mobile_manipulator | 10 | 3.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | DWA_planner, A*_global, joint_space_PD |
| DXW-K4 | MicroRover-K4 | wheeled | 2 | 4.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
| DXW-MICRO | MicroRover-μ | wheeled | 2 | 1.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
| DXW-MINI | MiniRover-TB | wheeled | 2 | 4.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
| DXW-P3AT | Rover-P3AT | wheeled | 2 | 8.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
| DXW-P3DX | Rover-P3DX | wheeled | 2 | 4.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
| DXW-SCOUT | ScoutRover | wheeled | 2 | 4.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
| DXW-SCOUTXL | ScoutRover-XL | wheeled | 2 | 15.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
