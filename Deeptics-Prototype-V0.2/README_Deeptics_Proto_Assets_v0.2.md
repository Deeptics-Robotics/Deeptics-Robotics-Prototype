# Deeptics Proto Asset Catalog (v0.2)

**Updated**: 2025-10-07

This catalog lists the **21 prototype assets** used across the Deeptics robotics-simulation + PoSml stack.
All entries are normalized to Deeptics-native codes and schemas for reproducibility and partner integration.

## What’s inside
- **Robots**: wheeled, legged, humanoids, aerial, and mobile manipulators
- **Sensors**: default blocks standardized across assets (RGB-D, IMU, LiDAR, FT, Tactile, Stereo)
- **Controllers**: curated presets for motion, planning, and estimation
- **PoSml packaging**: manifests + signed artifacts for verifiable simulation output

## Metadata schema
```json
{
  "asset_code": "DXQ-AGILE",
  "public_name": "Quadruped-Agile",
  "class": "legged",
  "subtype": "quadruped",
  "status": "proto",
  "orig_views": 1172,
  "deeptics_views": 0,
  "description": "Agile quad for foothold planning and uneven-terrain traversal.",
  "dof": 12,
  "payload_kg": 6.0,
  "sensor_default": ["SM-RGBD","SM-IMU","SM-LiDAR-3D"],
  "controller_presets": ["gait_trot","gait_walk","whole_body_QP"],
  "interfaces": {
    "control": ["CTRL-Locomotion"],
    "sensors": ["SM-RGBD", "SM-IMU"],
    "telemetry": ["metrics.json","run.log"]
  },
  "posml": {
    "package": "v0.1",
    "manifest": "DXQ-AGILE.manifest.json",
    "metrics": ["task_success_rate","energy_proxy","latency_ms"]
  },
  "safety": {"limits": true, "workspace_guard": true, "failsafe_halt": true},
  "compatibility": ["DX-Sim R0.1"]
}
```

## Asset index
| Code | Name | Class | DoF | Payload (kg) | Default Sensors | Controller Presets |
|---|---|---|---:|---:|---|---|
| DXW-MICRO | MicroRover-μ | wheeled | 2 | 1.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
| DXW-SCOUT | ScoutRover | wheeled | 2 | 4.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
| DXM-OMNIARM | OmniBase+Arm | mobile_manipulator | 10 | 3.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | DWA_planner, A*_global, joint_space_PD |
| DXH-COMPACT | Humanoid-Compact | humanoid | 20 | 0.5 | SM-RGBD, SM-IMU, SM-Stereo | gait_walk, push_recovery, whole_body_QP |
| DXA-5E | CollabArm-5e | manipulator | 6 | 5.0 | SM-RGBD, SM-IMU, SM-FT, SM-Tactile | joint_space_PD, task_space_impedance, RRT_connect, IK_solvers |
| DXF-INSPECT | QuadRotor-Inspect | aerial | 6 | 1.5 | SM-IMU, SM-Stereo, SM-RGBD | LQR_attitude, waypoint_P, VIO_loops |
| DXW-MINI | MiniRover-TB | wheeled | 2 | 4.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
| DXA-10E | CollabArm-10e | manipulator | 6 | 10.0 | SM-RGBD, SM-IMU, SM-FT, SM-Tactile | joint_space_PD, task_space_impedance, RRT_connect, IK_solvers |
| DXF-MICRO | MicroQuad | aerial | 6 | 0.03 | SM-IMU, SM-Stereo, SM-RGBD | LQR_attitude, waypoint_P, VIO_loops |
| DXQ-AGILE | Quadruped-Agile | legged | 12 | 6.0 | SM-RGBD, SM-IMU, SM-LiDAR-3D | gait_trot, gait_walk, whole_body_QP |
| DXW-P3DX | Rover-P3DX | wheeled | 2 | 4.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
| DXW-K4 | MicroRover-K4 | wheeled | 2 | 1.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
| DXA-IND4600 | IndustArm-4600 | manipulator | 6 | 60.0 | SM-RGBD, SM-IMU, SM-FT, SM-Tactile | joint_space_PD, task_space_impedance, RRT_connect, IK_solvers |
| DXH-MINI3 | Humanoid-Mini3 | humanoid | 16 | 0.5 | SM-RGBD, SM-IMU, SM-Stereo | gait_walk, push_recovery, whole_body_QP |
| DXH-MINI2 | Humanoid-Mini2 | humanoid | 16 | 0.5 | SM-RGBD, SM-IMU, SM-Stereo | gait_walk, push_recovery, whole_body_QP |
| DXM-TORSO | Tiago‑Class | mobile_manipulator | 10 | 3.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | DWA_planner, A*_global, joint_space_PD |
| DXW-P3AT | Rover-P3AT | wheeled | 2 | 4.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
| DXA-DESK | DeskArm‑N | manipulator | 6 | 1.0 | SM-RGBD, SM-IMU, SM-FT, SM-Tactile | joint_space_PD, task_space_impedance, RRT_connect, IK_solvers |
| DXW-SCOUTXL | ScoutRover‑XL | wheeled | 2 | 15.0 | SM-RGBD, SM-IMU, SM-LiDAR-2D | EKF_fusion, DWA_planner, A*_global |
| DXA-P7 | CollabArm‑P7 | manipulator | 7 | 7.0 | SM-RGBD, SM-IMU, SM-FT, SM-Tactile | joint_space_PD, task_space_impedance, RRT_connect, IK_solvers |
| DXA-3E | CollabArm‑3e | manipulator | 6 | 3.0 | SM-RGBD, SM-IMU, SM-FT, SM-Tactile | joint_space_PD, task_space_impedance, RRT_connect, IK_solvers |


## Using assets with PoSml
1. Select an asset by `asset_code`.

2. Create a run manifest (see `posml.manifest`) and pin seeds/noise for determinism.

3. Execute the run and produce signed artifacts (`run.log`, `metrics.json`).

4. Attach telemetry + safety bounds to the report for audit.


## Contact
partners@deeptics.ai
