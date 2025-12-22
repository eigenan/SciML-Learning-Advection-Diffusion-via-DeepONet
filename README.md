# Learning an Advection-Diffusion System using DeepONet

This notebook demonstrates the use of a Deep Operator Network (DeepONet) to solve a 1D diffusion equation. The DeepONet is a neural network architecture designed to learn operators, which are mappings between function spaces. In this case, the DeepONet learns the operator that maps the initial condition of the diffusion equation to the solution at a later time.

We consider the 1D diffusion equation:

$$
\frac{\partial u}{\partial t} = \nu \frac{\partial^2 u}{\partial x^2}
$$

with the following conditions:

- **Domain:** $x \in [0, 1]$, $t \in [0, 1]$
- **Boundary Conditions:** $u(0, t) = u(1, t) = 0$
- **Initial Condition:** $u(x, 0) = g(x)$, where $g(x)$ is a Gaussian random field.

The goal is to learn the operator that maps the initial condition function $g(x)$ to the solution function $u(x, t)$ for $t > 0$.

<img width="559" height="413" alt="diff_onet_output" src="https://github.com/user-attachments/assets/e2d12887-cdf1-448e-81b2-fe61167144e1" />
