### Overall Idea and Contribution
- A two-stage procedure to first learn a discovery and then deployment policy.
- Learns policies from supine (face up) to prone (face down) poses.
- Apparently 2 policies (1 for rolling over, 2 for standing up)

### Detailed Bits
- Stage 1 discover a motion trajectory without being limited by smoothness in motion or speed / torque limits.
- In Stage 2, deployment policy tracks the discovered trajectory (8x slowed down) using tracking rewards (under control regularization for sim2real).
- From stage 1 to 2, a learning curriculum is employed that progresses from easier to harder settings (simpler mesh, fixed pose, etc.).
- State is 74 dim proprioceptive info (DOF's pos, vel, robot's base angular vel, roll, pitch, prev actions)
- Actions are 23 dim PD targets.
- Sim frequency 1000 Hz, PD control 50 Hz
- Extensive evaluation w/o stage 2, full URDF, posture randomization, and single-shot.
