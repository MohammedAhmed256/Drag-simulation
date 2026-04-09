# Drag-simulation
This project models projectile motion under quadratic air resistance by numerically solving coupled non-linear differential equations. The simulation investigates how drag affects trajectory, range, and optimal launch conditions under varying physical parameters.

The project extends beyond basic modelling by incorporating:

Multiple numerical integration schemes (Euler and Runge-Kutta 4th order)
Altitude-dependent drag effects
Convergence analysis of numerical methods
Optimisation of launch angle for maximum range


Physical Model:
The motion is governed by newtons 2nd law with a quadratic drag force,
m*(dv/dt) = -mg - kv
where m is the mass, v is the velocity, and g is gravitational accelleration. please note this is usually written with vectors.
The extended model uses height dependent drag, k(y) = k_0 * exp(-y/H) where H is the characteristic height.
due to the non linearaity of the drag term, analytical solutions are not generally available.

Numerical methods:
Two integration schemes are implemented
Euler Method, a first-order method, computationally simple with lower accuracy and stability
Runge-Kutta (RK4), a fourth-order method that is significantly higher accuracy (Used as the primary solver in this project)
A convergence study is performed to compare the accuracy of both methods as the timestep (Δt) decreases

Key Features
-Simulation of 2D projectile motion with quadratic drag
-Comparison of Euler and RK4 integration methods
-Convergence analysis using log-log error scaling
-Parameter sweeps (e.g. varying mass)
-Altitude-dependent drag modelling
-Optimisation of launch angle using numerical minimisation

Results & Insights:
-The simulations demonstrate several key physical behaviours such as drag reducing range and breaks trajectory symmetry, producing steeper descent paths. Higher mass reduces the relative effect of drag, increasing range. Altitude-dependent drag increases range due to reduced air resistance at higher altitudes
-RK4 significantly outperforms Euler, exhibiting faster convergence and improved stability
-Optimal launch angle is less than 45° under drag, due to energy loss during flight

Example Outputs:

Trajectory comparisons (RK4 vs Euler)
Parameter sweeps (e.g. varying mass)
Drag model comparisons
Convergence plots (log-log error scaling)
Optimal launch angle calculations

Technologies used:
-Python
-NumPy
-SciPy
-Matplotlib

















