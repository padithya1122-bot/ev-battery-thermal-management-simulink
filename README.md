# EV Battery Thermal Management & R-1234yf Refrigeration Cycle (MATLAB / Simulink)

Hey there! This repository contains the MATLAB and Simscape simulation models I worked on during my internship at NoonRay Energy Pvt. Ltd. (IIT Madras Industrial Park, Chennai). 

It covers two main parts of thermal management: looking at how EV batteries heat up and cool down, and simulating a complete closed-loop refrigeration system.

---

### Project Overview

Battery thermal management is super important for keeping EV batteries safe and lasting a long time. In this project, I built and tested models in Simulink to see:
1. How heat moves out of a battery when using direct air cooling (convection) versus using a liquid cold plate (conduction).
2. How a standard vapor-compression refrigeration cycle works using R-1234yf refrigerant, checking the results on a Pressure-Enthalpy (P-H) diagram.

---

### Part 1: Battery Thermal Management (Convection vs. Conduction)

I modeled a 300 kg battery generating a constant 1 kW of heat under two different cooling methods:

* **Convective Cooling:** Heat goes straight from the battery surface into the surrounding air. 
  * *What I found:* The lower the convection coefficient (h), the higher the battery temperature rises (going from about 308 K up to 320 K with low airflow).
* **Conductive Cooling (Cold Plate):** Heat moves by conduction from the battery through a solid layer into a cold plate kept at a lower temperature.
  * *What I found:* Conduction cools the battery down much faster and keeps it stable close to the cold plate temperature (around 293 K). Thinner layers give a faster initial temperature drop.

---

### Part 2: R-1234yf Vapour-Compression Refrigeration Cycle

I also built a closed-loop refrigeration model to see how the refrigerant behaves through evaporation, compression, and condensation:
* **Evaporator Tube:** Low-pressure refrigerant absorbs heat from the load and turns into vapor.
* **Compressor:** Raises the pressure and enthalpy of the refrigerant using mechanical work.
* **Condenser:** Rejects the heat back out to the surroundings.
* **P-H Diagram Validation:** Sensors tracked the state points and plotted them on a P-H chart, confirming that the loop follows standard refrigeration theory smoothly without errors.

---

### Project Links & Resources
* [Presentation Slides](https://docs.google.com/presentation/d/1Z7y0GN761oVktsg2kIMHWrlEBNnztr6P/edit?usp=drive_link&ouid=110186731700141658012&rtpof=true&sd=true)
* [Detailed Internship Report Document 1](https://docs.google.com/document/d/1Nr2aCkfY1_TTS2E2FaihmTFem50EAWNk/edit?usp=drive_link&ouid=110186731700141658012&rtpof=true&sd=true)
* [Detailed Internship Report Document 2](https://docs.google.com/document/d/18M6gGqkUbdI7pCYNJdFg6OtwLGSj9mRh/edit?usp=drive_link&ouid=110186731700141658012&rtpof=true&sd=true)

### Files Included
* `Internship_Report_Perugu_Venkata_Aditya.docx`: The detailed final report with all equations, parameters, and graphs.
