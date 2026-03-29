
# FOC of PMSM using Fuzzy Logic Controller (MATLAB/Simulink)

## Overview

This project implements **Field Oriented Control (FOC)** for a Permanent Magnet Synchronous Motor (PMSM) using a **Fuzzy Logic Controller** and compares its performance with a conventional **PI Controller**.

The goal is to improve transient response and reduce overshoot in PMSM speed control.

---

##  Objective

* Replace traditional PI control with fuzzy logic Controller
* Improve system stability and robustness
* Analyze performance using simulation metrics

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

### 🔹 Speed Response

![Speed Response](speed_plot.png)

### 🔹 PI vs Fuzzy Comparison

![Comparison](pi_vs_fuzzy.png)

---

##  Performance Comparison

| Parameter     | PI Controller | Fuzzy Controller |
| ------------- | ------------- | ---------------- |
| Rise Time     | (add value)   | (add value)      |
| Settling Time | (add value)   | (add value)      |
| Overshoot     | (add value)   | (add value)      |

---

##  Observations

* Fuzzy controller significantly **reduces overshoot**
* Faster and smoother settling compared to PI controller
* Better handling of system non-linearity
* Improved overall stability

---

##  Tools Used

* MATLAB
* Simulink
* Fuzzy Logic Toolbox

---

##  Project Files

* `foc_fuzzy.slx` → Main Simulink model
* `fuzzy_controller.fis` → Fuzzy logic design
* `pi_vs_fuzzy.png` → Comparison plot
* `speed_plot.png` → Speed response

---

##  How to Run

1. Open MATLAB
2. Open `foc_fuzzy.slx`
3. Load `fuzzy_controller.fis`
4. Run the simulation

---

