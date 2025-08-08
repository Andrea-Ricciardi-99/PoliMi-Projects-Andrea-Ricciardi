# Project Structure

This repository contains all the Simulink files used during the project, organized into **Real System** and **Simulation** sections.

---

## 📂 Real System

This folder contains the Simulink files uploaded directly to the drone.  
They are organized by controller type, and each controller folder includes:

- **`init_control.m`** — Run this before starting Simulink.
- **`controller_HW.slx`** — Controller without filtering.
- **`controller_HW_EKF.slx`** — Controller with EKF-based filtering.

---

## 📂 Simulation

This folder contains Simulink files for system simulation, grouped by controller type.  
Each controller folder includes:

- **`init_control.m`** — Run this before starting Simulink.
- **`controller_no_noise.slx`** — Ideal (noiseless) feedback.
- **`controller_with_noise_control.slx`** — Simulated noise (with estimated characteristics) using a custom quadcopter model for controller design.
- **`controller_with_noise_realistic.slx`** — Similar to above, but uses the **Px4** library model for more realistic system behavior.  
  - Used for validating the controller’s real-world performance.

---

## 📂 Noise (within Simulation)

This subfolder contains MATLAB and Simulink files for:
- Extracting noise information from real-world data collected during experiments.
- Designing the **EKF** (Extended Kalman Filter).  
  *(Note: Not used for controller tuning.)*

---

### 🛠 Usage Tips
- Always run the `init_control.m` script before launching the corresponding Simulink model.
- Choose the correct controller and simulation environment based on whether you’re testing in hardware or simulation.
