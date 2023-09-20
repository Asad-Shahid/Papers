### Overall Idea

- Learn a policy to through and catch objects using MAPPO with each hand being one agent.
- Domain randomization to randomize friction, inertia, contact force center of mass, etc.
- 
### Novel Contribution
- Despite the thrower being able to throw towards a pre-defined destination in simulation, the policy would not transfer well due to a substantial dynamics gap.
- To deal with the above issue, a 3-stage training procedure is proposed:
    - Train a base policy to tackle the task, with the catcher observing the pre-defined throwing goal.
    - Freeze the base policy and train a goal estimator through supervised learning, using the rollout trajectory of the base policy as training data.
    - Replace the pre-defined throwing goal in the catcher’s observation with an estimated goal and fine-tune both the base policy and the goal estimator in an end-to-end fashion.
- To learn the goal estimator, they use the object's position history to predict the 3D position of the goal. (unclear how it is trained) 
