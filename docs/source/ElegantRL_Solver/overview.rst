Overview
=============

One sentence summary: ElegantRL_Solver is a high-performance RL Solver.

We aim to find high-quality optimum, or even (nearly) global optimum, for nonconvex/nonlinear optimizations (continuous variables) and combinatorial optimizations (discrete variables). We provide pretrained neural networks to perform real-time inference for nonconvex optimization problems, including combinatorial optimization problems.

This project is built on [ElegantRL](https://github.com/AI4Finance-Foundation/ElegantRL) and OpenAI Gym.

The following two key technologies are under active development:
  - Massively parallel simuations of gym-environments on GPU, using thousands of CUDA cores and tensor cores.
  - Podracer scheduling on a GPU cloud, e.g., DGX-2 SuperPod.

Key references:
  - Mazyavkina, Nina, et al. "Reinforcement learning for combinatorial optimization: A survey." Computers & Operations Research 134 (2021): 105400.

  - Bengio, Yoshua, Andrea Lodi, and Antoine Prouvost. "Machine learning for combinatorial optimization: a methodological tour d’horizon." European Journal of Operational Research 290.2 (2021): 405-421.

  - Makoviychuk, Viktor, et al. "Isaac Gym: High performance GPU based physics simulation for robot learning." Thirty-fifth Conference on Neural Information Processing Systems Datasets and Benchmarks Track (Round 2). 2021.

  - Nair, Vinod, et al. "Solving mixed integer programs using neural networks." arXiv preprint arXiv:2012.13349 (2020).

Environments: 
  - MIMO Beamforming in 5G/6G.
  - Classical NP-Hard problems.
  - Classical Simulation of Quantum Circuits.
  - Compressive Sensing.
  - Portfolio Management.
  - OR-Gym.

File Structure:
```
-RLSolver
-├── optimal
-|   ├──branch-and-bound.py
-|   └──cutting_plane.py
-├── helloworld
-|   ├──milp
-|   ├──tsp
-|   └──graph_maxcut
-└── rlsolver (main folder)
-    ├── envs
-    |   (nonconvex optimizations)
-    |   ├── learn2optimize
-    |   └── mimo_beamforming
-    |   (combinatorial optimizations)
-    |   ├── portfolio_management
-    |   ├── quantum_circuits
-    |   ├── vehicle_routing
-    |   ├── virtual_machine_placement
-    |   └── chip_design
-    |── rlsolver_learn2optimize
-    |── rlsolver_mimo_beamforming
-    |── rlsolver_portfolio_management
-    |── rlsolver_quantum_circuits
-    └── utils
```


**ElegantRL_Solver features high-performance and stability:**

**High-performance**: it can find high-quality optimum, or even (nearly) global optimum.

**Stable**: it leverages computing resource to implement the Hamiltonian-term as an add-on regularization to DRL algorithms. Such an add-on H-term utilizes computing power (can be computed in parallel on GPU) to search for the "minimum-energy state", corresponding to the stable state of a system.


  


