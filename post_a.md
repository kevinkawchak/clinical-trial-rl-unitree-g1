
## [LinkedIn 22Jan26 Post](https://www.linkedin.com/posts/kevin-kawchak-38b52a4a_stage-i-gemini-3-pro-api-macos-terminal-activity-7420244455678599168-Meoj)

Stage I: Gemini 3 Pro API MacOS terminal instructions + MuJoCo 
Clinical trial simulations. Videos: https://lnkd.in/gFwE_eFY
Goal: 1 Walking treatment nurse is to inject patient who has a red bandage, 1 Standing clinical research nurse checks documents, 1 Patient dressed in a business suit sitting in an infusion chair
Outcome: Mujoco Infusion Room 1 = 2 nurses and patient in black attire with red bandage. Treatment nurse in blue falls down as patient looks at the treatment nurse
Outcome: Mujoco Infusion Room 2a = 2 nurses and patient in black attire with red bandage. Patient is ejected from seat as treatment nurse sways arm with injector in hand. 2b = Treatment nurse eventually slides over to infusion chair with syringe still in hand, but with patient laying on the floor. No training was performed in this stage.

Pros: 
1) Appropriate medical context
Cons:
1) Low quality human movements
2) Low quality human representations

Stage II: Opus 4.5 Extended MacOS terminal instructions to Multi-Unitree G1 agent tracking simulations (Pre-Trained, Shown)
Goal: Recreate mjlab + Isaac Lab + MuJoCo-Warp using aMacBook M3 Max 48GB System. Videos: https://lnkd.in/gSXHnmFe
Outcome: 6 simulated G1 robots performing highly co-ordinated actions and dance moves. Green mesh “kinematic ghost” on one robot shows exactly what the character should be doing at that specific moment in time

Simulation Evidence:
1) Command is running a simulator + policy loop, not a media player: cd ~/robotics/mjlab && source .venv/bin/activate; uv run demo --num-envs 6
2) Logs show physics stepping, RL-style observations/actions, rewards, termination, and domain randomization: Environment step-size; Live policy inference + actuator control: ActionManager with joint_pos

Stage III: Train on Oncology Clinical Trial Nurse Context from Stage II 
Goal: Refine the following policies associated with clinical trial nurse locomotion. Videos: https://lnkd.in/gyZTtpi2 
Outcome: Limitations in L4 Colab GPU training compute and time yielded sporadic behavior at 50 iterations for each of the three policies.
a) Policy: Careful Navigation for IV equipment navigation regarding obstacle-rich areas
b) Policy: Patient Approach for approaching patient beds for use near patients
c) Policy: Equipment Transport for carrying infusion pumps

UPDATE: January 22nd, 2026 Improved RL Trainings at 3000 iterations on H100. Videos: https://lnkd.in/gSEUpXsf. Updated Notebook on GitHub
a) Stable walking: episode length reaches ~1000 steps
b) Later rewards jump at iteration ~1200–2000 
c) Highest reward: Patient Approach: ~45.80
d) Careful Navigation & Patient Approach illustrate subtle movements, but Equipment Transport lacked utility

Future Research: Optimize sim-to-real protocols for use in real robots. 

References:
Kevin Kawchak. (2026). kevinkawchak/clinical-trial-rl-unitree-g1: v0.1 (v0.1). Zenodo. https://lnkd.in/gDDHsnVs
Mujocolab. "mjlab." GitHub, n.d., https://lnkd.in/gGAmhRnW

- Post by Kevin Kawchak
