# Reinforcement Learning-Based Smart Health Coach

## Project Overview
This project involves the design and implementation of an AI-driven health coach that uses **Reinforcement Learning (RL)** to provide personalized fat-reduction and lifestyle optimization strategies. Unlike static models, this agent learns through interaction with a simulated environment to maximize long-term health outcomes for users.

## Core Methodology
The system is modeled as a **Markov Decision Process (MDP)** consisting of:
- **State Space:** User data including BMI, caloric intake, physical activity levels, and metabolic factors (based on the Kaggle Obesity Dataset).
- **Action Space:** Personalized interventions such as dietary adjustments and exercise intensity recommendations.
- **Reward Function:** Designed to incentivize sustainable weight loss while penalizing extreme/unhealthy calorie deficits.

## Technical Stack
- **Languages:** Python
- **Algorithms Evaluated:** PPO (Proximal Policy Optimization), SAC (Soft Actor-Critic), DQN (Deep Q-Network), and A2C (Advantage Actor-Critic).
- **Libraries:** Stable Baselines3, OpenAI Gym/Gymnasium, Pandas, NumPy.
- **Environment:** Custom-built simulation environment for user lifestyle modeling.

## Key Findings
- **Algorithm Performance:** Proximal Policy Optimization (**PPO**) demonstrated the most stable convergence and best generalization across various user profiles.
- **Outcome:** The agent successfully optimized action sequences to lead a "simulated user" from an 'Obese' classification to a 'Normal' weight range within the training episodes.

## 🔗 Live Implementation
https://github.com/user-attachments/assets/0b351d7d-0c0c-42dd-a071-84a89a8c10bc

