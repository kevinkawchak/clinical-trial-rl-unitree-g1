# Clinical Trial Drug Infusion Room - RL Training Package

## Videos: [Three Trainings Final (50/3000/1500 Iterations)](https://drive.google.com/drive/folders/1ET0zCNUudv9y7x6STLMtyAVoHfFIV6Ij?usp=sharing)

<picture>
  <img src="assets/GitHub28Jan26.jpg" alt="Main">
</picture>

## Session Information
- **Session ID**: 20260122_185241
- **Date**: 2026-01-22 18:59:53
- **Framework**: mjlab (MuJoCo-Warp)
- **Hardware**: NVIDIA L4, H100, T4
- **1500 Iterations**: Fine-Tuned Execution

## Package Contents

```
clinical_trial_outputs/
├── checkpoints/          # PyTorch model checkpoints (.pt)
├── onnx/                 # ONNX models for deployment
├── tensorboard/          # TensorBoard log files
├── charts/               # Visualization outputs
│   ├── training_analysis.png
│   └── interactive_dashboard.html
├── configs/              # Training configurations
├── training_logs/        # Raw training output logs
├── logs/                 # Additional logs
└── sim2real_deployment_guide.json
```

## Trained Policies

| Policy | Context | ONNX File | Recommended Use |
|--------|---------|-----------|----------------|
| Careful Navigation | IV equipment navigation | careful_navigation_policy.onnx | Obstacle-rich areas |
| Patient Approach | Approaching patient beds | patient_approach_policy.onnx | Near patients |
| Equipment Transport / Dynamic Environment | Carrying infusion pumps | equipment_transport_policy.onnx | Transporting equipment |

## Quick Start

### Sim-to-Sim Evaluation (Mac/Linux)
```bash
# Clone mjlab
git clone https://github.com/mujocolab/mjlab.git
cd mjlab && uv sync

# Run evaluation
uv run play Mjlab-Velocity-Flat-Unitree-G1 \
    --checkpoint /path/to/checkpoints_3000/careful_navigation_model_2999.pt \
    --num-envs 6

# View at http://localhost:8080
```

### Sim-to-Real Deployment
See `sim2real_deployment_guide.json` for complete instructions.

### TensorBoard Visualization
```bash
tensorboard --logdir ./tensorboard
```

## License
Apache 2.0

[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.18343597-blue)](https://doi.org/10.5281/zenodo.18343597)
