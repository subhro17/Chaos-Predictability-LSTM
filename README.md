# Chaos-Predictability-LSTM
This repository contains a deep learning framework designed to model and predict the chaotic motion of a Double Pendulum. By leveraging Long Short-Term Memory (LSTM) networks, we create a high-speed neural surrogate capable of approximating the complex, non-linear dynamics derived from Lagrangian Mechanics.

Traditional numerical solvers (like Runge-Kutta 4th Order) are computationally expensive for real-time applications. This project explores the feasibility of using AI to "internalize" physical laws, providing a 50x speedup in inference while maintaining physical stability.
# Key Features
1. Physics-Grounded Data: Synthetic data generated via Euler-Lagrange equations and integrated using an RK4 scheme.
2. Recursive Forecasting: An LSTM architecture trained to perform multi-step-ahead predictions, effectively mapping the system's temporal evolution.
3. Chaos Analysis: Investigation of the Predictability Horizon and the Butterfly Effect (Sensitivity to Initial Conditions).
4. Fractal Stability Mapping: A global analysis of the Phase Space complexity, identifying basins of stability vs. chaotic regimes.
# Results
1. Temporal Prediction vs. Physical TruthThe model tracks the secondary pendulum link ($\theta_2$) with high fidelity ($R^2 > 0.98$) before reaching the Lyapunov Time threshold (~3.5s), where phase drift naturally occurs.
2. Phase Space TopologyEven after the temporal prediction diverges, the model remains Topologically Stable. The LSTM traces the correct Chaotic Attractor, proving it has learned the energy constraints of the system.
# Tech Stack
Language: Python 3.12 \\
Deep Learning: PyTorch
Numerical Computing: NumPy, SciPy
Visualizations: Matplotlib (with LaTeX formatting)
Hardware: Optimized for NVIDIA GeForce RTX 3050 (CUDA)

# How to Use
1. Clone the Repo: https://github.com/subhro17/Chaos-Predictability-LSTM
2. Install Dependencies: pip install torch numpy  scipy matplotlib pandas scikit-learn
3. Run the Analysis: Open analysis.ipynb to visualize the trajectories and the fractal stability map.
