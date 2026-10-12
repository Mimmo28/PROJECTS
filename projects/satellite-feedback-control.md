# 🚀 Satellite Feedback Control & Orbit Simulation
> **Architecture:** Dynamic Systems Modeling & Closed-Loop Control | **Tech Stack:** MATLAB, Simulink, SISO Tool | **Status:** Completed (Academic / University of Palermo, Team Project - 2024)

## 📋 Project Overview
A control engineering and simulation project focused on the attitude and orbital dynamics of an artificial satellite. Developed in 2024 as a collaborative team project at the **University of Palermo**, the objective was to mathematically model nonlinear system dynamics, analyze system stability, and design a high-precision feedback controller validated through both linear and nonlinear simulations.

---

## 🏗️ Engineering & Modeling Workflow

### 1. Mathematical Modeling & Linearization
- Derived equations of motion and rotational kinematics governing satellite attitude dynamics.
- Formulated state-space representations and transfer functions around target operating points.
- Analyzed open-loop poles/zeros, controllability, observability, and inherent stability margins (gain and phase margins).

### 2. Feedback Controller Design & Synthesis
- Utilized MATLAB's **SISO Tool** and root-locus techniques to synthesize compensators meeting stringent settling time, overshoot, and steady-state error criteria.
- Implemented loop-shaping and frequency-domain compensator tuning to ensure robustness against orbital disturbance torques (aerodynamic drag, solar radiation pressure, gravitational gradients).

### 3. Simulation & Validation in Simulink
- Designed nonlinear block models in **Simulink** incorporating actuator saturation and sensor noise characteristics.
- Benchmarked closed-loop linear responses against full nonlinear dynamic simulations to confirm tracking accuracy and disturbance rejection.

---

## 📈 Key Outcomes
- Successfully stabilized satellite attitude dynamics with minimal overshoot and fast convergence.
- Validated controller robustness under simulated parametric uncertainties and external orbital disturbances.

---

> **Developer:** Domenico Filippo Innamorato  
> **Team Project:** University of Palermo (BSc Computer Engineering, 2024)
