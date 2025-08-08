# PoliMi Projects – Andrea Ricciardi

This repository contains a collection of academic and technical projects completed during my studies at Politecnico di Milano.  
They span topics from control systems and deep learning to structural analysis and IoT, and reflect both individual and team-based work.

---

## 📂 Quadcopter Project

**Purpose:**  
Design and implement control algorithms for stabilizing a quadcopter’s angular orientation.

**Key features:**
- Derived physical model of the drone and estimated dynamic parameters.
- Implemented PID, state-space, and feedback linearization controllers.
- Developed a neural network for motor voltage-to-thrust mapping.
- Simulation and real-time testing using MATLAB/Simulink.

---

## 📂 CNN-PlantDiagnosis

**Purpose:**  
Classify plant health (healthy/unhealthy) from RGB images using deep learning.

**Key features:**
- Backbone: **ConvNextXLarge** with SimSiam pretraining.
- Data cleaning: Outlier removal (“shrek” and “trolololo” images).
- Augmentation: Flips, rotations, translations, zooms, and random contrast.
- Notebooks for both **training** and **inference**.
- Scripts for dataset inspection (`plot.py`) and troll image detection (`labeling.py`).

---

## 📂 Time Series Forecasting NN

**Purpose:**  
Predict future time series values using a ResNet-inspired, attention-based deep learning model.

**Workflow:**
1. **Data Generation** – Used **TimeGAN** to produce synthetic sequences for underrepresented categories.
2. **Sample Processing** – Cleaned and filtered generated sequences to match real data.
3. **Model Training** – Auto-regressive forecasting with multihead attention and category encoding.

**Key results:**
- Significant accuracy improvement with GAN-based data augmentation.
- Modular architecture to integrate new data and control model complexity.

---

## 📂 FEM Project

**Purpose:**  
Perform dynamic finite element analysis of a railway bridge using the requirements from *Dynamics of Mechanical Systems*.

**Accomplishments (all requirements met):**
1. Defined FE model suitable for 0–24 Hz frequency range; plotted undeformed structure.
2. Computed natural frequencies and mode shapes; plotted up to 24 Hz.
3. Calculated damped natural frequencies and damping ratios.
4. Computed FRFs between input at point B and vertical acceleration at points A and B; plotted Bode diagrams.
5. Developed reduced modal-coordinate model (first three modes) and compared FRFs.
6. Computed FRF of bending moment at point C.
7. Simulated seismic excitation and computed displacement and acceleration at point A.
8. Proposed structural modification reducing FRF peak at point B by ≥30% without exceeding +5% total mass.

**Implementation:**  
- Developed and executed in `dmb_fem2/programma`.
- Includes `.inp` FE input files and MATLAB scripts for post-processing.

---

## 📂 CAM Project

**Purpose:**  
Design a manufacturing workflow from CAD modeling to process planning.

**Key features:**
- Geometry breakdown and process selection (milling, turning).
- Cost and constraint estimation.
- Tolerancing and manufacturability considerations.

---

## 📂 Lightweight publish-subscribe application protocol (IoT Project)

**Purpose:**  
Build a wireless telemetry network using **MQTT** and **TinyOS**.

**Key features:**
- Implemented low-level firmware stack for telemetry transmission.
- Managed memory and event-driven programming for constrained devices.
- Designed and tested MQTT message flow to a centralized broker.

---

## 📂 Temperature control in a four-rooms building

**Purpose:**  
Regulate temperature in a multi-room thermal model using **Linear Matrix Inequalities**.

**Key features:**
- Built state-space model of heat transfer.
- Designed and simulated LMI-based controllers.
- Integrated MATLAB LMI toolbox into control loop.
- Delivered technical presentation explaining controller design.
