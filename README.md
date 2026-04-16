# Reinforcement Learning-Based Smart Health Coach

## Project Overview
This project involves the design and implementation of an AI-driven health coach that uses **Reinforcement Learning (RL)** to provide personalized fat-reduction and lifestyle optimization strategies. Unlike static models, this agent learns through interaction with a simulated environment to maximize long-term health outcomes for users.

## Core Methodology
The project follows a systematic Reinforcement Learning pipeline designed to transform static health data into a dynamic, goal-oriented decision-making agent.

### 1. Problem Formulation: Markov Decision Process (MDP)
To enable agent learning, the environment is modeled as an **MDP**, defined by the mathematical tuple $(S, A, R, \gamma)$:
* **State Space ($S$):** Multidimensional vectors representing the user's current health status. Key features include BMI, caloric intake (FAVC), physical activity frequency, and age (sourced from the Kaggle Obesity Dataset).
* **Action Space ($A$):** Discrete interventions recommended by the coach, such as "Increase Physical Activity," "Reduce Caloric Intake," or "Maintain Routine."
* **Reward Function ($R$):** A custom-engineered scalar feedback loop:
    * **Goal Reward:** $+10$ for reaching a healthy BMI range ($18.5 - 24.9$).
    * **Progress Bonus:** $+1$ for incremental BMI reduction.
    * **Penalty:** $-5$ for actions leading to weight gain or stagnant health metrics.

### 2. Comparative Model Architecture
The methodology centers on benchmarking four distinct Reinforcement Learning architectures to identify the most stable and effective "Coach":
1.  **PPO (Proximal Policy Optimization):** An on-policy Actor-Critic method that uses a clipped surrogate objective to ensure stable and reliable policy updates.
2.  **SAC (Soft Actor-Critic):** An off-policy algorithm that maximizes **entropy**, encouraging the agent to explore a wider variety of health strategies.
3.  **DQN (Deep Q-Network):** A value-based approach using experience replay to estimate optimal action-values.
4.  **A2C (Advantage Actor-Critic):** A synchronous framework that utilizes an "Advantage" estimate to reduce variance during training.

### 3. Implementation Pipeline
1.  **Environment Engineering:** Developed a custom **Gymnasium** (OpenAI Gym) environment to simulate physiological responses to lifestyle changes.
2.  **Training:** Models were trained over **50,000+ timesteps** using the Stable Baselines3 library.
3.  **Evaluation:** Performance was measured by tracking the **Cumulative Reward** and **Convergence Rate** to ensure the recommendations were both safe and effective.

## Technical Stack
- **Languages:** Python
- **Algorithms Evaluated:** PPO (Proximal Policy Optimization), SAC (Soft Actor-Critic), DQN (Deep Q-Network), and A2C (Advantage Actor-Critic).
- **Libraries:** Stable Baselines3, OpenAI Gym/Gymnasium, Pandas, NumPy.
- **Environment:** Custom-built simulation environment for user lifestyle modeling.

## Key Findings
- **Algorithm Performance:** Proximal Policy Optimization (**PPO**) demonstrated the most stable convergence and best generalization across various user profiles.
- **Outcome:** The agent successfully optimized action sequences to lead a "simulated user" from an 'Obese' classification to a 'Normal' weight range within the training episodes.

## 🔗 Live Implementation

https://github.com/user-attachments/assets/4eea73f3-5cb8-44de-8a49-b592bf76010f



