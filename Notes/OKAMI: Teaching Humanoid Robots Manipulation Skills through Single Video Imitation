### Overall Idea

- generates a “reference plan” by extracting both object and human motion information from the video.
- humanoid motion is generated through object-aware retargeting to map the extracted human body and hand movements onto the humanoid robot.

### Models/Tools used 
- GPT-4V: Identifies task-relevant objects via prompts on sampled video frames.
- Grounded-SAM: Segments and localizes identified objects in the initial frame.
- Cutie: Provides tracking of object positions throughout the video.
- SLAHMR (modified with SMPL-H): Reconstructs the full-body and hand motion trajectories from the video.

### Limitations
- focuses on upper-body manipulation within tabletop scenarios and does not include lower-body or locomotion behaviors.
- retargeting process can struggle with significant variations in object shapes.
