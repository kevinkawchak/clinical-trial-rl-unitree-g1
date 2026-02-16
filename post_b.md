## [LinkedIn 28Jan26 Post](https://www.linkedin.com/posts/kevin-kawchak-38b52a4a_three-reinforcement-learning-rl-trainings-activity-7422523638391951360-Peu9)

Three reinforcement learning (RL) trainings based on Kevin Zakka’s mjlab/Isaac Lab API/MuJoCo framework have been completed (1, 2). This was accomplished primarily with Opus 4.5 Extended generating rounds of new RL Python notebooks that produced three sets of final “.pt” checkpoints.

Each simulated humanoid ran on the same policy as shown in the video, but at different states. The green arrow above humanoids is the commanded velocity, the light blue arrow is the current velocity, and the purple arrow is the goal direction. 

The 50 iteration notebook yielded sporadic movements in attempts to represent clinical trial careful navigation, equipment transport/dynamic environment, and patient approach. Increasing iterations to 3000 resulted in low overall motions which were not abled to accomplish trial tasks from all humanoids, with light blue velocity arrows being minimized. 

Further Opus prompts in the 1500 iteration training addressed locomotion issues with rational movements for each of the three clinical nurse cases.

Prompt Excerpt: “For instance, careful navigation may represent walking in a relatively straight line with avoidance of some obstacles; patient approach may be walking in a relatively straight line and then pausing; and dynamic environment might be walking with a larger array of movements that change based on conditions.“
a) Careful navigation OK, 0:13: Primarily linear movements with some direction changes
b) Equipment transport OK, 0:35: Diverse set of movements achieved across simulated humanoids
c) Patient approach OK, 0:57: Two humanoids approach each other, pause, and go in different directions

Next steps include using ONNX policies from the 1500 iteration, and training on real Unitree G1 robots. https://lnkd.in/gcBrk8ui (HD Video)

"Everything that moves will be autonomous." - Nvidia CEO Jensen Huang

References:
(1) https://lnkd.in/gcHbU9Sz (License: Apache 2.0)
(2) https://lnkd.in/gDDHsnVs (Apache 2.0)
