# End-2-End-Driving
This  repository contain End-to-end autonomous driving project using the F1TENTH Gym environment. Trains and evaluates reinforcement learning agents (PPO, DQN, DDPG) for lap completion on simulated tracks. Built with PyTorch, NumPy, and Matplotlib, focusing on stable, closed-loop performance and consistent navigation.

================================================================================
F1TENTH PPO TRAINING PROJECT - SETUP INSTRUCTIONS
================================================================================

PROJECT: End-to-End Autonomous Driving Agent using PPO
DATE CREATED: [19/09/2025]
PYTHON VERSION: 3.10.18


================================================================================
QUICK START GUIDE
================================================================================

1. Extract End-2-End Driving.zip 

2. ENVIRONMENT SETUP
   - Install Anaconda/Miniconda if not already installed
   - Open Anaconda Prompt (Windows) or Terminal (Mac/Linux)
   - Create environment: conda create -n rl_env python=3.10.18
   - Activate environment: conda activate rl_env

3. INSTALL DEPENDENCIES
   - Navigate to project folder: cd path/to/project/src
   - Install packages: pip install -r requirements_minimal.txt
   - Install packages: pip install -r requirements_clean.txt
   - Install packages: pip install -r requirements_new.txt
   - Install F1Tenth gym: pip install git+https://github.com/f1tenth/f1tenth_gym.git@main

4. RUN TRAINING
   - Ensure environment is active: conda activate rl_env
   - Navigate to src folder: cd path/to/project/src
   - Start training: python ppo.py

================================================================================
FILE CHECKLIST
================================================================================

Required files in src/ directory:
[ ] ppo.py
[ ] custom_f1tenth_env.py
[ ] reward_functions.py
[ ] requirements_minimal.txt
[ ] requirements_clean.txt

Optional files:
[ ] lem_seminar_f1tenth_env/ (module directory)
[ ] environment.yml (for conda environment export)

================================================================================
TRAINING CONFIGURATION
================================================================================

Default settings in train_ppo.py:
- Training steps: 10,000,000
- WandB tracking: Disabled
- Video recording: Disabled
- Model saving: Enabled

To modify settings, edit the configuration section at the top of train_ppo.py

================================================================================
MONITORING
================================================================================

View training progress with TensorBoard:
1. In a new terminal: tensorboard --logdir runs
2. Open browser: http://localhost:6006

================================================================================
TROUBLESHOOTING
================================================================================

Issue: ModuleNotFoundError for f1tenth_gym
Fix: pip install git+https://github.com/f1tenth/f1tenth_gym.git@main

Issue: CUDA/GPU not available
Fix: Script auto-detects and uses CPU if needed

Issue: Import error for custom modules
Fix: Ensure running from src/ directory

Issue: Memory problems
Fix: Reduce num_steps or disable video recording

================================================================================
NOTES
================================================================================

- Training takes approximately 2-4 hours for 1M steps (varies by hardware)
- Models are saved in runs/ directory
- Evaluation videos saved in eval_videos/ directory
- For questions, check the README.md file

================================================================================

https://github.com/user-attachments/assets/d1431065-e454-469d-956c-c391bf6d3039

