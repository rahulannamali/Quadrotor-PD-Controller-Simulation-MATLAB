# Quadrotor PD Controller Simulation – MATLAB

## 📌 Project Description

This project demonstrates the implementation of a Proportional-Derivative (PD) controller to control the vertical (z-axis) motion of a 1D quadrotor in MATLAB. The controller was developed as part of an academic exercise to understand basic flight dynamics and closed-loop control.

Using a custom simulation built on MATLAB’s `ode45` solver, the quadrotor is commanded to either hover or follow a step input, showcasing how classical control theory can be applied to aerial systems.

## 🚁 Features

- Simulates vertical flight of a quadrotor in 1D (z-axis)
- Implements a PD control law:  
  `u = m * (z̈_des + Kp * e + Kv * ė + g)`
- Visualizes flight trajectory using MATLAB plots
- Includes performance-tuned gain values for:
  - **Hover stabilization**
  - **1-meter step input response**

## 📂 File Structure

- `controller.m` – Core PD control logic (user-implemented)
- `height_control.m` – Physics simulation with `ode45`
- `runsim.m` – Main script to run simulation scenarios
- `fixed_set_point.m` – Defines desired altitude for testing
- `utils/` – Contains helper functions for state updates and visualization

## ▶️ How to Use

1. Clone or download this repository.
2. Open MATLAB and set the working directory to the project folder.
3. Run `runsim.m` to start the simulation.
4. Adjust `Kp` and `Kv` in `controller.m` to observe different system behaviors.

## 📊 Demonstration Goals

- Achieve smooth hover at z = 0 m with no oscillation.
- Reach 1 m altitude with:
  - **Rise time < 1 second**
  - **Overshoot < 5%**

These tuning goals reflect a stable, responsive system appropriate for vertical flight control.

## 📷 Sample Output

_Add screenshots or `.gif` of the simulation results here if available_

## 🛠 Skills Highlighted

- Classical control system design (PD tuning)
- MATLAB scripting and simulation
- Dynamic modeling using differential equations
- Visualization and performance analysis

## 📌 Notes

This is a standalone academic demonstration of vertical flight control. While simplified to 1D motion, the logic and control techniques scale up to full 3D UAV systems with proper modeling and sensor integration.

---

