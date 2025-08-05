# Robot-Arm-Torque

This document provides a motor selection for a 3-joint horizontal robotic arm carrying a 2 kg payload.


## System Overview

* **Payload:** 2 kg
* **Total arm length:** 0.4 m
* **Joints:** 3 
* **Arm configuration:** Horizontal
* **Gearing:** Yes (5:1 gear reduction assumed)


## Step 1: Raw Torque Calculation (Before Gears)

Each arm segment ≈ 0.133 m.

| Joint | Load | Distance from Joint | Torque (N·m) |
| ----- | ---- | ------------------- | ------------ |
| first | 2 kg | 0.133 m             | 2.61 N·m     |
| second| 2 kg | 0.266 m             | 5.22 N·m     |
| third | 2 kg | 0.4 m               | 7.83 N·m     |

---

## Step 2: Adjusted Torque (After 5:1 Gear Reduction)

| Joint | Raw Torque | With Gearbox (÷5) |
| ----- | ---------- | ----------------- |
| third | 7.83 N·m   | 1.57 N·m          |
| second| 5.22 N·m   | 1.04 N·m          |
| first | 2.61 N·m   | 0.52 N·m          |



> External gearboxes are strongly recommended for torque alignment.
