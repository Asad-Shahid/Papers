### Overall Idea

- Fuse vision, sound and vision-based tactile data with a self-attention model and train through imitation learning 
- Self-attention model fuses the features (extracted by seperate networks) from 3 modalities using cross-modality, cross-time and both. 
- The robot control input is a task-dependent discrete action space. `x, y, z` or `x, theta` movements of end-effector
- IK solver to convert cartesian space displacement commands to joint space actions on real robot
- Cross entropy loss between ground truth action and predicted action is used for training


### Limitations
- Uses behavior cloning for learning an expert policy that requires demonstrations though they collect only 10 demonstrations
