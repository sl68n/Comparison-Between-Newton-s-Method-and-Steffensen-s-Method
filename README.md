# Comparison Between Newton’s Method and Steffensen’s Method

![Course](https://img.shields.io/badge/Course-CPCS%20212-blue)
![MATLAB](https://img.shields.io/badge/MATLAB-R2023a+-orange)
![Convergence](https://img.shields.io/badge/Convergence-Quadratic-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

A numerical analysis project that implements and compares two powerful root-finding algorithms:

- Newton’s Method  
- Steffensen’s Method  

Both methods are analyzed theoretically and implemented in MATLAB with graphical visualization and iteration tracking.

---

## Project Overview

This project demonstrates how iterative numerical methods approximate roots of nonlinear equations.

We implemented both methods in MATLAB, analyzed their convergence behavior, and compared:

- Convergence speed
- Computational cost
- Sensitivity to initial guesses
- Practical performance

---

## Newton’s Method

Newton’s Method is a derivative-based root-finding technique.

### Iteration Formula:

x(n+1) = x(n) - f(x(n)) / f'(x(n))

### Requirements:
- Function must be continuous
- Derivative must exist
- Initial guess close to root
- f'(x) ≠ 0

### Advantages:
- Quadratic convergence
- Fast when derivative is known

### Disadvantages:
- Requires derivative
- Can fail if derivative = 0
- Sensitive to initial guess
- Possible cycling behavior

---

## Steffensen’s Method

Steffensen’s Method is a derivative-free root-finding algorithm with quadratic convergence.

### Iteration Formula:

x(n+1) = x(n) - [f(x(n))²] / (f(x(n) + f(x(n))) - f(x(n)))

### Advantages:
- Does NOT require derivative
- Quadratic convergence
- Useful when derivative is complex or unavailable

### Disadvantages:
- Requires two function evaluations per iteration
- Higher computational cost
- Sensitive to initial guess
- Can also suffer from cycling

---

## Example Used

Newton’s Method Example:
f(x) = x² − 5  
Initial guess: x₀ = 2  
Root found ≈ 2.236067978

Steffensen’s Method Example:
f(x) = x² − 7  
Initial guess: x₀ = 2.5  
Exact root = √7 ≈ 2.645751311  
Method converges with high precision.

---

## MATLAB Implementation

### Newton’s Method Script

- Inputs:
  - Function handle
  - Derivative handle
  - Initial guess
- Outputs:
  - Root approximation
  - Iteration table
  - Convergence plot

### Steffensen’s Method Script

- Inputs:
  - Function handle
  - Initial guess
- Outputs:
  - Root approximation
  - Iteration table
  - Convergence plot

Both scripts:
- Use tolerance = 1e-10
- Maximum 100 iterations
- Display formatted iteration tables
- Plot the function and final root

---

## Feature Comparison

| Feature | Newton’s Method | Steffensen’s Method |
|----------|-----------------|--------------------|
| Convergence Rate | Quadratic | Quadratic |
| Requires Derivative | Yes | No |
| Function Calls per Iteration | 1 function + 1 derivative | 2 function evaluations |
| Computation Cost | Lower (if derivative known) | Slightly higher |
| Sensitive to Initial Guess | High | High |
| Susceptible to Cycles | Yes | Yes |
| Best Use Case | Derivative Available | Derivative Unknown |

---

## Conclusion

Both Newton’s and Steffensen’s methods demonstrated rapid quadratic convergence when the initial guess was close to the true root.

- Newton’s Method is computationally efficient when the derivative is available.
- Steffensen’s Method provides a strong alternative when derivatives are difficult or impossible to compute.

The choice between them depends on derivative availability and computational considerations.

---

## Author

Sultan Yasir Alasami  
Computer Science Student  
King Abdulaziz University
