# Design and Fabrication of Axial Flux BLDC Motor

An engineering project covering the complete electromagnetic design, CAD modeling, hardware fabrication, and experimental validation of a 6-slot, 8-pole Axial Flux Brushless DC (BLDC) Motor.

---

## 3D Interactive CAD Model
* **[View Interactive CAD Model on Onshape](https://cad.onshape.com/documents/a40cc31149d1d09e504c31ce/w/99b5a3a0bd8f971fb47aac6b/e/8211c1ee55ab4f770ae8887e?renderMode=0&uiState=6a9bdb5d4aa540bc693907ed)**

---

## Technical & Electromagnetic Specifications

| Parameter | Specification / Dimension |
| :--- | :--- |
| **Topology** | 6-Slot, 8-Pole Axial Flux Permanent Magnet BLDC |
| **Winding Configuration** | Star (Y) Connected, Single Layer |
| **Turns per Slot** | 38 Turns |
| **Wire Gauge** | 20 AWG Enamel Coated Copper Wire |
| **Winding Factor** | 0.866 |
| **Phase Resistance** | 1 Ohm |
| **Stator Outer Diameter** | 75 mm |
| **Rotor Outer Diameter** | 75 mm |
| **Slot Diameter** | 12 mm |
| **Shaft Diameter** | 6.9 mm |
| **Spool Dimensions** | Outer Diameter: 8 mm \| Inner Diameter: 6 mm |
| **Bearing Diameter** | 17 mm |
| **Structural Material** | 3D Printed PLA (Stator, Spools, Shaft, Rotor) |

---

## Working Principle & Control Pipeline

1. **Power Delivery:** An 11.1V LiPo RC battery supplies DC power to the Electronic Speed Controller (ESC).
2. **PWM Signal Generation:** An Arduino UNO generates Pulse Width Modulation (PWM) signals to command speed and direction to the ESC.
3. **Phase Conversion:** The SimonK 30A ESC converts DC power into 3-phase AC current delivered to the stator coils.
4. **Electromagnetic Interaction:** The stator produces a rotating magnetic field in the axial direction, driving the 8-pole permanent magnet rotor.
5. **Electronic Commutation:** Dynamic PWM regulation maintains continuous electronic commutation and variable speed control.

---

## Bill of Materials (BOM)

| Component | Specification |
| :--- | :--- |
| **Permanent Magnets** | Neodymium 15 x 2 mm Circular Magnets |
| **Winding Wire** | 20 AWG Enamel Coated Copper Wire |
| **3D Printed Structure** | PLA Stator Body, Spools, Shaft, Rotor |
| **Speed Controller** | SimonK 30A Electronic Speed Controller (ESC) |
| **Microcontroller** | Arduino UNO |
| **Power Source** | 11.1V LiPo RC Battery |

---

## Testing & Oscilloscope Results

* **Equipment Used:** Rigol DS1054Z Digital Oscilloscope.
* **Waveform Validation:** Confirmed a clean 3-phase sinusoidal back-EMF profile.
* **Phase Alignment:** Verified the expected 120-degree phase shift across all three phases during rotation.

---

## Engineering Challenges & Solutions

* **ESC Overheating:** Solved by transitioning from constant signal drive algorithms to smooth, incremental PWM speed regulation via Arduino.
* **Rotor Jerks & Synchronization:** Iteratively tested multiple pole arrangements (8 mm magnets at 10-pole, 4-pole, and 8-pole) before optimizing to **15 mm magnets in an 8-pole configuration**, significantly enhancing magnetic flux distribution and operational stability.

---

