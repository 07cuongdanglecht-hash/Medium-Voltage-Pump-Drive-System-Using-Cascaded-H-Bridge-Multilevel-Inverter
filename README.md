# Medium-Voltage Cascaded H-Bridge Multilevel Inverter (13-Level CHB-MLI) & FOC Control System

## 📌 Project Overview
This project presents the design, modeling, and simulation of a **13-Level Cascaded H-Bridge Multilevel Inverter (CHB-MLI)** drive system for high-power medium-voltage (6kV, 2.85MW) induction motors. 

The main focus of this work includes:
1. **Grid-Synchronous Soft Starting Method:** Eliminating inrush current and mechanical torque transients during grid connection.
2. **Field Oriented Control (FOC):** High-performance vector control for dynamic speed and torque regulation.
3. **Fault-Tolerant Operation (Neutral Point Shift):** Maintaining balanced line-to-line voltages and maximizing available output power under cell failure scenarios.

---

## 🔑 Key Features & Technical Highlights
* **Power Electronics Topology:**
  * 36-pulse diode rectifier fed by a phase-shifting phase-zigzag transformer to achieve low input current Total Harmonic Distortion ($THD \approx 1.01\%$).
  * 13-Level CHB-MLI (6 H-bridge power cells per phase) using Phase-Disposition Sinusoidal PWM (IPD-PWM).
* **Control Strategies:**
  * **SRF-PLL & Amplitude/Phase Synchronization:** Real-time tracking of grid voltage parameters for seamless transfer from inverter to grid.
  * **Rotor Flux-Oriented Control (RFOC):** Decoupled control of flux ($i_{sd}$) and torque ($i_{sq}$) components.
* **Fault-Tolerant Control:**
  * Integrated **Neutral Point Shift (NPS)** algorithm adding zero-sequence voltage ($V^{(0)}$) to maintain balanced line voltages when power cells are bypassed due to faults.

---

## 📊 Key Simulation Results (MATLAB/Simulink)
* **Normal Condition:** Output current $THD < 0.25\%$ with fast torque and speed dynamic response.
* **Grid Connection:** Smooth grid transfer without current spikes or mechanical shocks.
* **Fault Management (2 Cells Fault on Phase A):**
  * *Standard Bypass Method:* Line voltage drops to 6010V, speed drops to 805 RPM.
  * *Neutral Point Shift Method:* Line voltage recovers to 7761V (83.2% capacity), speed maintained at 930 RPM.

---

## 🛠 Tools & Environment
* **Software:** MATLAB / Simulink
* **Toolboxes Used:** Control System Toolbox, Simscape Electrical

---

## 📂 Repository Structure
