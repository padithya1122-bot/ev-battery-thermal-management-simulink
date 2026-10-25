# EV Battery Thermal Management & R-1234yf Refrigeration Cycle (MATLAB / Simulink)

This repository contains MATLAB / Simscape simulation models developed during the internship at **NoonRay Energy Pvt. Ltd. (IIT Madras Industrial Park, Chennai)**[cite: 5]. It focuses on EV battery thermal management (comparing conduction vs. convection) and a closed-loop vapor-compression refrigeration cycle using refrigerant R-1234yf[cite: 5].

---

## 📌 Project Overview
Effective thermal management is critical for EV battery safety, performance, and longevity[cite: 7]. This project investigates:
1. **Transient thermal behavior** of a lumped battery thermal mass under direct convection versus cold-plate conduction[cite: 5, 7].
2. **Closed-loop vapor-compression refrigeration** using R-1234yf, validated via Pressure-Enthalpy (P-H) diagram analysis[cite: 5, 7].

---

## 🔋 Part I: Battery Thermal Management (Conduction vs. Convection)
Two physical network models were simulated in MATLAB Simscape assuming a constant **1 kW heat generation** from a 300 kg battery[cite: 5, 7]:

* **Convective Model:** Direct heat loss from battery surface to ambient air ($T_{amb} = 313.15\text{ K}$)[cite: 5, 7].
  * *Finding:* Temperature rise is inversely proportional to the convective heat transfer coefficient ($h$)[cite: 7]. Lower $h$ values ($5\text{ W/m}^2\cdot\text{K}$) result in significant temperature escalation ($308\text{ K} \to 320\text{ K}$)[cite: 5, 7].
* **Conductive Model (Cold Plate):** Heat conducted from the battery through a solid layer into a liquid-cooled cold plate ($293.15\text{ K}$)[cite: 5, 7].
  * *Finding:* Cold-plate conduction provides rapid thermal stabilization, dropping the battery temperature quickly and maintaining it close to the cold plate temperature ($\approx 293\text{ K}$)[cite: 5, 7]. Thinner conductive layers offer lower thermal resistance for quicker initial response[cite: 5, 7].

---

## ❄️ Part II: R-1234yf Vapour-Compression Refrigeration Cycle
A closed-loop multi-component refrigeration model was implemented to simulate full-system thermodynamic behavior:
* **Evaporator Tube:** Low-pressure refrigerant absorbs heat from the load and undergoes phase change[cite: 5, 7].
* **Positive Displacement Compressor:** Increases refrigerant pressure and enthalpy via mechanical work input[cite: 5, 7].
* **Condenser (2-Pass + Manifolds):** Multi-stage heat rejection to surroundings[cite: 5, 7].
* **P-H Validation:** Real-time state sensors feed data into a P-H diagram generator, successfully capturing all four thermodynamic phases (Evaporation, Compression, Condensation, and Throttling via flow restrictions)[cite: 5, 7].

---

## 📂 Repository Contents
* `Internship_Report_Perugu_Venkata_Aditya.docx`: Comprehensive report detailing model architectures, parameter sweeps, and analytical derivations[cite: 5].
* `Internship_Presentation_Perugu_Venkata_Aditya.pptx`: Slide deck summarizing the thermal study and Simulink schematic layout[cite: 6].
