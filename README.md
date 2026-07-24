

# Comparative Analysis of PI and Hybrid Adaptive PI Controllers for PMSM Field Oriented Control  (MATLAB/Simulink)

## Overview

This project implements **Field Oriented Control (FOC)** for a Permanent Magnet Synchronous Motor (PMSM) using a **Adaptive PI Logic Controller** and compares its performance with a conventional **PI Controller**.

The goal is to improve transient response and reduce overshoot in PMSM speed control.

---

##  Objective

- Design a PMSM Field Oriented Control system.
- Implement a conventional PI speed controller.
- Develop a Hybrid Adaptive PI speed controller.
- Compare controller performance under identical operating conditions.

---

##  System Architecture

* Clarke & Park Transformations (abc → dq)
* dq-axis current control
* Speed control loop using:

  * PI Controller
  * Fuzzy Logic Controller (.fis)
* PWM generation and inverter model
* PMSM motor model with feedback

---

##  Results

###  Speed Response(Fuzzy-PI Controller)

<img width="952" height="972" alt="Speed_vs_time_Adaptive_PI" src="https://github.com/user-attachments/assets/a5bc18e4-9f01-47cf-8721-c6167801a57c" />


###  Adaptive PI vs PI Comparison

<img width="1600" height="856" alt="Speed_vs_time_of _PI_vs_Adaptive_PI" src="https://github.com/user-attachments/assets/7062a521-55fd-4a71-a487-b2c75820bcee" />
Speed_vs_time_of _PI_vs_Adaptive_PI.jpg

---

##  Performance Comparison

| Parameter     | PI Controller | Fuzzy Controller |
| ------------- | ------------- | ---------------- |
| Rise Time     |  0.1284 sec   |    0.5158 sec    |
| Settling Time |  1.0569 sec   |    0.9572 sec    |
| Overshoot     |  25.78 %      |    0.33 %        |

---

##  Observations

- Hybrid Adaptive PI controller significantly reduces overshoot compared to the conventional PI controller.
- Improved transient response with smoother speed regulation.
- Better steady-state stability under changing operating conditions.
- Adaptive gain adjustment improves controller robustness for nonlinear motor dynamics.

---

##  Tools Used

* MATLAB
* Simulink
* Fuzzy Logic Toolbox

---

##  Project Files

* `Hybrid_PI_Fuzzy.slx` → Main Simulink model
* `Fuzzy_control_PID.fis` → Fuzzy logic design
* `Speed_vs_time_of _PI_vs_Adaptive_PI.jpg` → Comparison plot
* `Speed_vs_time_Adaptive_PI.png` → Speed response

---

##  How to Run

1. Open MATLAB
2. Open `Hybrid_PI_Fuzzy.slx`
3. You can change Reference speed which is done by changing the constant Value in the subsystem in Bottom right(in .slx file).
4. Make Sure you have then in the Files(in Workspace).
5. Load `Fuzzy_control_PID.fis`
6. Run the simulation

---

