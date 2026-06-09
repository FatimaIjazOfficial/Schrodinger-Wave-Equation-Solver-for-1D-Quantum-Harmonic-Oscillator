# Schrödinger Wave Equation Solver (1D Quantum Harmonic Oscillator)
In this project we have discussed the Schrodinger Wave Equation which includes its time dependency and time independency for 1D Quantum Harmonic Oscillator through different numerical techniques for 1D Harmonic Oscillator . These numerical techniques include, Shooting method , Crank Nicolson and Compare it using Python Jupyter.

## Overview

This project numerically explores the solutions of the Schrödinger equation for the harmonic oscillator using two methods: **Shooting Method** and **Crank–Nicolson Method**. The simulations include:

1. Classical harmonic oscillator potential and energy.
2. Quantum stationary states and probabilities.
3. Time evolution of wave packets.

The code is implemented in Python using **NumPy**, **Matplotlib**, and **SciPy**.

---

## Equations Implemented

**Time-Independent Schrödinger Equation:**

`-(hbar^2 / (2*m)) * d^2(psi)/dx^2 + V(x) * psi(x) = E * psi(x)`

with harmonic potential:

`V(x) = (1/2) * m * omega^2 * x^2`

**Time-Dependent Schrödinger Equation:**

`i * hbar * d(psi)/dt = H * psi`

**Crank–Nicolson update (finite difference):**

`(I + i*H*dt/(2*hbar)) * psi(t+dt) = (I - i*H*dt/(2*hbar)) * psi(t)`

**Shooting method finite-difference approximation:**

`d^2(psi)/dx^2 ≈ (psi[i+1] - 2*psi[i] + psi[i-1]) / dx^2`

---

## Features

1. **Classical Harmonic Oscillator (CHO):**

   * Plots classical potential `V(x) = 1/2 k x^2`
   * Shows total energy and classical turning points ±A

2. **Quantum Harmonic Oscillator (QHO):**

   * Computes first 4 stationary energy levels `E_n = hbar*omega*(n+1/2)`
   * Plots corresponding normalized wavefunctions `psi_n(x)` and probabilities `|psi_n(x)|^2`

3. **Shooting Method:**

   * Finds energy eigenvalues and eigenfunctions using finite-difference approach
   * Produces normalized wavefunctions and probability densities

4. **Crank–Nicolson Method:**

   * Computes stationary states by diagonalizing the Hamiltonian matrix
   * Evolves arbitrary initial wave packets in time with unconditionally stable updates
   * Visualizes quantum dynamics: oscillations, spreading, interference

---

## Python Dependencies

* numpy
* matplotlib
* scipy

Install via pip if needed:

```bash
pip install numpy matplotlib scipy
```

---

## Usage

1. Run each Python script section to generate plots for classical and quantum oscillators.
2. Adjust parameters like mass `m`, frequency `omega`, spatial range `x_min`, `x_max`, or time steps `num_time_steps` for different simulations.
3. Observe:

   * Classical vs. quantum energy levels
   * Wavefunctions and probability densities
   * Time evolution of Gaussian wave packets

---

## Results

* Classical potential and turning points clearly illustrate energy conservation.
* Quantum stationary states show discrete energy levels and spatial probability distributions.
* Shooting method provides insight into eigenvalue problems.
* Crank–Nicolson allows full time evolution and demonstrates dynamic quantum behavior.

---

## References
1. Griffiths, D. J., *Introduction to Quantum Mechanics*, 2nd Edition
2. Press, W. H., et al., *Numerical Recipes in C/Python*, 3rd Edition
3. SciPy and Matplotlib official documentation
