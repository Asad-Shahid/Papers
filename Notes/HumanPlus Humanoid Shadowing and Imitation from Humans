### Overall Idea and Contribution
- Learns to "shadow" humans using few demonstrations (behavior cloning).
- During shadowing, human operators teleoperate the robot while it extracts data (including RGB egocentric views)
- During teleoperation, they estimate human motion and retarget it to humanoid motion, passed as input to the low-level policy. 
- RL to create a robust, task-agnostic low-level controller that makes the robot match target poses.

### Detailed Bits
- Human motion is collected using RGB camera.
- Full body human motion is extracted using off-the shelf models (WHAM for body, HaMeR for hands). 
- The 3D poses are then retargeted to robot’s kinematic structure, even though the robot has fewer joints (fixed mapping of key joints).
- In simulation, they train a task-agnostic low-level control policy (the Humanoid Shadowing Transformer) using RL.
- The reward is designed to match retargeted poses while optimizing energy and minimizing slippage.
- RL policy is trained on a large human motion dataset and learns to produce joint-level commands to mimic the human’s motion.
- During “shadowing”, human operators control the robot using the RL policy, and this data is collected.
- This shadowing data is then used to do behavior cloning and train a higher-level skill policy.
- Humanoid Imitation Transformer is trained using behavior cloning to learn specific task skills from ~40 demonstrations. 
