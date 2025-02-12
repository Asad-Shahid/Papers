### Overall Idea

- Use off-policy RL (DDPGfd) and online corrections to benchmark insertion tasks (NIST assembly).
- Test policies under different set of input modalities 
   - proprioception
   - proprioception and wrist force/torque
   - proprioception, wrist force/torque and images
   - wrist force/torque and images
- Experiments: mainly NIST insertion, also adds a dynamic insertion in to a moving target and key in lock.
- Experiments: Test on a different nominal position of the target, rotated 45 degrees

### Contribution
- Large-scale evaluation of RL on industrial insertion task.
- Few modifications to original DDPGfD:
    - remove the independent Gaussian noise added to the actor network.
    - The replay buffer retains all experience data and all transitions are weighted equally (no prioritization), actions from the human operator are regarded as the agent’s own.
    - Task and action space curriculum to gradually increase the difficulty level of learning.
    - Initially action space is quite small, but is grown exponentially (up to a maximum) as the agent policy becomes more reliable.
    - On-policy correction to override the agent’s actions if it is not performing well.
