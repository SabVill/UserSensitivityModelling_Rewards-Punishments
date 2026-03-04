# RL & MAB for Reward–Punishment Sensitivity Modeling and Incentives Adaptation

This repository contains the implementation and simulation framework used to study how **Reinforcement Learning (RL)** and **Multi-Armed Bandit (MAB)** approaches can infer user sensitivity to rewards and punishments and adapt incentive strategies accordingly.

## 📂 Repository Structure

- `ModelsLearning_RL_MAB_Rand.ipynb`  
  Main notebook containing the full simulation pipeline, including:
  - user behavior simulation
  - reward–punishment configuration
  - learning algorithms (RL, MAB, Random baseline)
  - evaluation and visualization of results

- Generated files (created when running the notebook):
  - step trends across simulation days
  - performance comparisons between models
  - intermediate data outputs (if enabled)

## ⚙️ Overview

The framework simulates a behavior change scenario in which:
- Each user is assigned a **daily step goal**, predicted from historical data.
- At each time step, an algorithm selects a **reward–punishment configuration (r, p)**.
- The user’s behavior (daily steps) is generated based on:
  - the selected incentives
  - the user’s latent sensitivity to rewards and punishments

The system then observes whether the goal is achieved (success/failure) and updates its internal model accordingly.

## 🤖 Implemented Models

- **Reinforcement Learning (Q-learning)**  
  Learns optimal incentive strategies through reward-based updates over time.

- **Multi-Armed Bandit (MAB)**  
  Balances exploration and exploitation to identify effective incentive configurations.

- **Random Baseline**  
  Selects reward–punishment pairs randomly, used as a non-adaptive benchmark.

## 🎯 Objective

The goal is to evaluate whether learning-based approaches can:
1. Infer user sensitivity to rewards and punishments from behavior alone  
2. Adapt incentive strategies over time  
3. Improve behavioral outcomes compared to non-adaptive approaches  

## ▶️ How to Run

1. Open the notebook:

ModelsLearning_RL_MAB_Rand.ipynb

2. Run all cells sequentially.
3. Outputs (plots and metrics) will be generated automatically.

## 📊 Outputs

The notebook produces:
- learning curves of selected (r, p) configurations  
- evolution of user step counts over time  
- comparison between RL, MAB, and Random baseline  
- evidence of adaptation to different user sensitivity profiles  

## 🔍 Notes

- The environment is **fully simulated**, allowing controlled evaluation of learning behavior.
- User sensitivity is **not explicitly modeled or provided** to the algorithms; it is inferred implicitly from interaction outcomes.
- The framework is designed to be **extensible** to other behavior change domains.

## 📌 Future Extensions

- Integration with real-world behavioral data  
- Extension to additional latent user traits  
- Deployment in adaptive intervention systems  
