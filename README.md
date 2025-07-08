# BMS-Simulation-EV  
Simulation-based Battery Management System for 48V, 30Ah LFP battery using MATLAB/Simulink  

---

## 🎯 Objective  
To simulate a basic Battery Management System (BMS) for a **48 V, 30 Ah LiFePO₄ battery pack** used in electric two-wheelers, incorporating **voltage/current monitoring**, **temperature fault protection**, and **SOC estimation** using MATLAB Simulink.

---

## ⚙️ Features Implemented

### 1. Battery Modeling
- Simulated 48 V battery using **DC Voltage Source**
- Internal resistance: `0.05 Ω`
- Load resistor: `5 Ω`

### 2. Voltage and Current Monitoring
- Connected **voltage and current sensors** to **scopes**
- Real-time signal visualization of battery behavior

### 3. Over-Temperature Fault Logic
- Temperature input simulated using a **Step block** (30°C → 70°C at t = 2s)  
- Fault triggers when **T > 60°C**
- **Display block** shows binary fault output (0 → 1)

### 4. SOC Estimation (Coulomb Counting)
- SOC formula: `SOC = 100 - ∫ I(t) / (30 × 3600)`  
- SOC displayed on screen using a **Display block**

---

## 🛠 Tools Used
- MATLAB **R2025a**  
- Simulink  
- Simscape Electrical

---

## 📊 Simulation Results
- **Voltage (Scope_V):** Stable at ~45 V  
- **Current (Scope_I):** ~9.5 A  
- **Fault Display:** Switches to 1 at 2s (T > 60°C)  
- **SOC Display:** Gradually decreases from 100%

---

## 📘 Learning Outcome
Demonstrated a working understanding of **BMS architecture** — including sensing, fault logic, and energy tracking — using **industry-standard simulation tools**.

---

> 🚀 *This project serves as a simulation prototype. Future work may include real-time embedded BMS implementation using TI BQ76952 IC and STM32F103 MCU.*
