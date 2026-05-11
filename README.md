# Monte Carlo Potts Model for Grain Growth Simulation

A GPU-accelerated Monte Carlo Potts Model for simulating curvature-driven grain growth, abnormal grain growth (AGG), and Zener pinning in polycrystalline materials.

---

## Overview

This project simulates microstructure evolution on a 2D lattice using the Monte Carlo Potts approach. Grain boundaries evolve through energy minimization using Metropolis updates, while pinned particles restrict boundary motion to model Zener pinning effects.

The framework is designed for fast large-scale simulations using CUDA-based parallelization.

---

## Features

- Monte Carlo Potts grain growth simulation
- Curvature-driven coarsening
- Abnormal grain growth (AGG)
- Zener pinning implementation
- Voronoi microstructure initialization
- CUDA GPU acceleration
- Grain statistics and visualization
- Checkerboard parallel updates

---

## Physical Model

Each lattice site stores a grain ID.

The simulation:
1. Randomly selects neighboring grain states
2. Computes local energy change
3. Accepts/rejects updates using the Metropolis criterion

Acceptance rule:

```math
P =
\begin{cases}
1, & \Delta E \le 0 \\
e^{-\Delta E/T}, & \Delta E > 0
\end{cases}
```

Pinned particles introduce local energy barriers that slow grain-boundary motion.

---

## Tech Stack

- Python
- NumPy
- CUDA / Numba
- Matplotlib

---

## Outputs

- Grain evolution snapshots
- Grain-size distribution
- Mean grain size vs time
- Grain count evolution
- Orientation maps

---

## Applications

- Computational materials science
- Grain-growth kinetics studies
- AGG research
- GPU-accelerated scientific computing
