# Design and Fabrication of Axial Flux BLDC Motor

An engineering project covering the complete electromagnetic design, CAD modeling, hardware fabrication, and experimental validation of a 6-slot, 8-pole Axial Flux Brushless DC (BLDC) Motor[cite: 2].

---

## 3D Interactive CAD Model
* **[View Interactive CAD Model on Onshape](https://cad.onshape.com/documents/a40cc31149d1d09e504c31ce/w/99b5a3a0bd8f971fb47aac6b/e/8211c1ee55ab4f770ae8887e?renderMode=0&uiState=6a9bdb5d4aa540bc693907ed)**[cite: 2]

---

## Technical & Electromagnetic Specifications

| Parameter | Specification / Dimension |
| :--- | :--- |
| **Topology** | 6-Slot, 8-Pole Axial Flux Permanent Magnet BLDC[cite: 2] |
| **Winding Configuration** | Star (Y) Connected, Single Layer[cite: 2] |
| **Turns per Slot** | 38 Turns[cite: 2] |
| **Wire Gauge** | 20 AWG Enamel Coated Copper Wire[cite: 2] |
| **Winding Factor** | 0.866[cite: 2] |
| **Phase Resistance** | 1 $\Omega$[cite: 2] |
| **Stator Outer Diameter** | 75 mm[cite: 2] |
| **Rotor Outer Diameter** | 75 mm[cite: 2] |
| **Slot Diameter** | 12 mm[cite: 2] |
| **Shaft Diameter** | 6.9 mm[cite: 2] |
| **Spool Dimensions** | Outer Diameter: 8 mm \| Inner Diameter: 6 mm[cite: 2] |
| **Bearing Diameter** | 17 mm[cite: 2] |
| **Structural Material** | 3D Printed PLA (Stator, Spools, Shaft, Rotor)[cite: 2] |

---

## Working Principle & Control Pipeline

1. **Power Delivery:** An 11.1V LiPo RC battery supplies DC power to the Electronic Speed Controller (ESC)[cite: 2].
2. **PWM Signal Generation:** An Arduino UNO generates Pulse Width Modulation (PWM) signals to command speed and direction to the ESC[cite: 2].
3. **Phase Conversion:** The SimonK 30A ESC converts DC power into 3-phase AC current delivered to the stator coils[cite: 2].
4. **Electromagnetic Interaction:** The stator produces a rotating magnetic field in the axial direction, driving the 8-pole permanent magnet rotor[cite: 2].
5. **Electronic Commutation:** Dynamic PWM regulation maintains continuous electronic commutation and variable speed control[cite: 2].

---

## Bill of Materials (BOM)

| Component | Specification |
| :--- | :--- |
| **Permanent Magnets** | Neodymium 15 x 2 mm Circular Magnets[cite: 2] |
| **Winding Wire** | 20 AWG Enamel Coated Copper Wire[cite: 2] |
| **3D Printed Structure** | PLA Stator Body, Spools, Shaft, Rotor[cite: 2] |
| **Speed Controller** | SimonK 30A Electronic Speed Controller (ESC)[cite: 2] |
| **Microcontroller** | Arduino UNO[cite: 2] |
| **Power Source** | 11.1V LiPo RC Battery[cite: 2] |

---

## Testing & Oscilloscope Results

* **Equipment Used:** Rigol DS1054Z Digital Oscilloscope[cite: 2].
* **Waveform Validation:** Confirmed a clean 3-phase sinusoidal back-EMF profile[cite: 2].
* **Phase Alignment:** Verified the expected 120-degree phase shift across all three phases during rotation[cite: 2].

---

## Engineering Challenges & Solutions

* **ESC Overheating:** Solved by transitioning from constant signal drive algorithms to smooth, incremental PWM speed regulation via Arduino[cite: 2].
* **Rotor Jerks & Synchronization:** Iteratively tested multiple pole arrangements (8 mm magnets at 10-pole, 4-pole, and 8-pole) before optimizing to **15 mm magnets in an 8-pole configuration**, significantly enhancing magnetic flux distribution and operational stability[cite: 2].

---

## Repository Structure

```text
├── CAD/                  # 3D STL/STEP design files exported from Onshape
├── Code/                 # Arduino C/C++ scripts for PWM motor control
├── Docs/                 # Datasheets, schematics, and project presentation
├── Media/                # Photos and oscilloscope back-EMF test captures
└── README.md             # Project documentation
