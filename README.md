# Numerical Approximations of Solutions to the N-Body Problem

## Overview

This repository provides a complete framework for constructing and implementing a mathematical model in Python to simulate the trajectories of an **N-body gravitational system**.

The **N-body problem** is a classical problem in physics and applied mathematics that seeks to predict the motion of a system of celestial bodies interacting through gravitational forces. While the **two-body problem** admits an exact analytical solution (e.g., Keplerian orbits), systems with three or more bodies generally **do not have closed-form solutions**. Instead, their behavior is often:

- Highly nonlinear  
- Sensitive to initial conditions  
- Chaotic over long time scales  

As a result, numerical methods are essential for approximating solutions.

---

## Objectives

This project aims to:

- Model gravitational interactions between \( N \) bodies using Newtonian mechanics  
- Implement numerical integration methods to approximate trajectories  
- Visualize system evolution over time  
- Provide a flexible and extensible framework for experimentation  

---

## Mathematical Formulation
Each body in the system follows Newton’s law of gravitation and Newton’s second law:

### Gravitational Force
$$\mathbf{F}_{ij} = G \frac{m_i m_j}{\|\mathbf{r}_j - \mathbf{r}_i\|^3} (\mathbf{r}_j - \mathbf{r}_i)$$

### Equation of Motion
$$m_i \frac{d^2 \mathbf{r}_i}{dt^2} = \sum_{j \ne i} \mathbf{F}_{ij}$$

This leads to a system of **coupled second-order differential equations**, which we rewrite as a first-order system for numerical integration.

---

## Numerical Methods

The repository supports (or is designed to support) multiple integration techniques:

- **Euler Method** (baseline, less accurate)
- **Runge-Kutta Methods (RK4)** (higher accuracy, commonly used)
- **Symplectic Integrators** (better energy conservation for long simulations)
- (Optional extension) **Adaptive step-size methods**

Each method trades off:

| Method | Accuracy | Stability | Performance |
|------|--------|----------|------------|
| Euler | Low | Poor | Fast |
| RK4 | High | Good | Moderate |
| Symplectic | Moderate | Excellent (long-term) | Moderate |

---

## Features

- Modular architecture for simulation components  
- Configurable number of bodies and initial conditions  
- Support for different numerical solvers  
- 2D and/or 3D trajectory visualization  
- Energy tracking and diagnostics  
- Extensible for advanced physics models  

---

## Project Structure


n-body/
│── main.py # Entry point for simulations
│── integrators/ # Numerical solvers (Euler, RK4, etc.)
│── models/ # Physics and system definitions
│── utils/ # Helper functions
│── visualization/ # Plotting and animation tools
│── data/ # Saved simulation data (optional)
│── README.md


---

## Installation

Clone the repository:

```bash
git clone https://github.com/troyc03/n-body.git
cd n-body
```

# Numerical Approximations of Solutions to the N-Body Problem

## Overview

This repository provides a complete framework for constructing and implementing a mathematical model in Python to simulate the trajectories of an **N-body gravitational system**.

The **N-body problem** is a classical problem in physics and applied mathematics that seeks to predict the motion of a system of celestial bodies interacting through gravitational forces. While the **two-body problem** admits an exact analytical solution (e.g., Keplerian orbits), systems with three or more bodies generally **do not have closed-form solutions**. Instead, their behavior is often:

- Highly nonlinear  
- Sensitive to initial conditions  
- Chaotic over long time scales  

As a result, numerical methods are essential for approximating solutions.

---

## Objectives

This project aims to:

- Model gravitational interactions between \( N \) bodies using Newtonian mechanics  
- Implement numerical integration methods to approximate trajectories  
- Visualize system evolution over time  
- Provide a flexible and extensible framework for experimentation  

---

## Mathematical Formulation

Each body in the system follows Newton’s law of gravitation and Newton’s second law:

### Gravitational Force

\[
\mathbf{F}_{ij} = G \frac{m_i m_j}{\|\mathbf{r}_j - \mathbf{r}_i\|^3} (\mathbf{r}_j - \mathbf{r}_i)
\]

### Equation of Motion

\[
m_i \frac{d^2 \mathbf{r}_i}{dt^2} = \sum_{j \ne i} \mathbf{F}_{ij}
\]

This leads to a system of **coupled second-order differential equations**, which we rewrite as a first-order system for numerical integration.

---

## Numerical Methods

The repository supports (or is designed to support) multiple integration techniques:

- **Euler Method** (baseline, less accurate)
- **Runge-Kutta Methods (RK4)** (higher accuracy, commonly used)
- **Symplectic Integrators** (better energy conservation for long simulations)
- (Optional extension) **Adaptive step-size methods**

Each method trades off:

| Method | Accuracy | Stability | Performance |
|------|--------|----------|------------|
| Euler | Low | Poor | Fast |
| RK4 | High | Good | Moderate |
| Symplectic | Moderate | Excellent (long-term) | Moderate |

---

## Features

- Modular architecture for simulation components  
- Configurable number of bodies and initial conditions  
- Support for different numerical solvers  
- 2D and/or 3D trajectory visualization  
- Energy tracking and diagnostics  
- Extensible for advanced physics models  

---

## Project Structure


n-body/
│── main.py # Entry point for simulations
│── integrators/ # Numerical solvers (Euler, RK4, etc.)
│── models/ # Physics and system definitions
│── utils/ # Helper functions
│── visualization/ # Plotting and animation tools
│── data/ # Saved simulation data (optional)
│── README.md


---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/n-body.git
cd n-body
