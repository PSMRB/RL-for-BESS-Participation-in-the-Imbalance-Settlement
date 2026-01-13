# RL-for-BESS-Participation-in-the-Imbalance-Settlement

This repository gathers codes for the control of a Battery Energy Storage System (BESS) in the Imbalance Settlement (IS) using Reinforcement Learning (RL). In particular, a TD3 agent is used to control on a quarter-hour basis a 20MW/MWh BESS participating exclusively to the IS (no bidding on any market).
 
The TD3_agent_git.py file is the main script that can be run to train and test a TD3 agent based on Belgian IS data also provided in this repository. All useful functions and classes are in the file Classes_TD3_git.py. The requirements are in the requirements.txt file.
 
This script is one of the original building block that was used for the paper : C. Rasic, P. Favaro, Y. Wang and J. -F. Toubeau, "Safe Reinforcement Learning for Battery Energy Storage Participation in the Imbalance Settlement," in IEEE Transactions on Energy Markets, Policy and Regulation, doi: 10.1109/TEMPR.2025.3639758.

The above-cited paper introduces a fast and Safe Reinforcement Learning (RL) framework that unifies data-driven market learning with physics-based feasibility guarantees. Instead of relying on arbitrary approximations of market dynamics, a deep neural actor–critic captures the strategic behaviors in the IS directly from data, in a fully end-to-end manner. Safety is enforced by a differentiable projection layer that maps every action onto the convex BESS feasible set, ensuring hard constraint satisfaction during both training and
deployment. By separating the learning of unknown economics from the enforcement of known BESS physics within a single trainable pipeline, the proposed safe agent achieves millisecond-scale runtime and structurally safe policies. The framework leverages off-policy RL to reuse past experiences and expert-guided trajectories, accelerating convergence and avoiding short-sighted strategies. On real Belgian IS market data, our approach delivers higher profits than both RL and model-based baselines, with faster and more stable convergence among RL methods.

The actual codes of the paper, including Safe Projetion mechanisms, are expected to be added in the future in this repository. For any earlier interest regarding the codes of the paper, please contact Cyril Rasic (cyril.rasic@umons.ac.be).
