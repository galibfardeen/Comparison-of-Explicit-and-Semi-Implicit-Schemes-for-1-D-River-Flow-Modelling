# Comparison-of-Explicit-and-Semi-Implicit-Schemes-for-1-D-River-Flow-Modelling
This project compares **1D Python-based** and **2D Delft3D** hydrodynamic models to simulate changes in **water level** and **velocity** over time for the **Halda River**, Bangladesh. Both models use field data to assess wave propagation using explicit and semi-implicit numerical schemes. Boundary conditions are read from real or synthetic hydrographs, and stability is maintained through CFL-based time stepping. The work demonstrates how different numerical formulations influence wave propagation and flow behavior in river systems.


---

## Overview

- **Study area:** Halda River (Panchapukuria → Enayethat, ~45.8 km)  
- **Tools:** Python (1D), Delft3D (2D)  
- **Period:** Jan 2021 – Dec 2022  
- **Goal:** Examine temporal flow behavior using simplified 1D–2D modelling approaches.

---

## Methodology

- **Data Sources:** BWDB (discharge, stage, cross-sections), Copernicus GLO-30 DEM, Google Earth Pro (bridge data)  
- **1D Model:**  
  - Explicit and semi-implicit finite-difference schemes  
  - Assumed depth = 5 m, width = 50 m, celerity = 7 m/s  
  - Semi-implicit scheme showed smoother and more stable results.  
- **2D Model:**  
  - Built from HEC-RAS-derived bathymetry  
  - Used same boundary data  
  - Results inconsistent due to setup and boundary mismatches.

---

## Results Summary

| Model | Scheme | Performance | Remarks |
|--------|---------|-------------|----------|
| 1D Python | Explicit | Poor | Unstable oscillations |
| 1D Python | Semi-Implicit | Better | Stable propagation |
| 2D Delft3D | Shallow-Water | Incomplete | Needs calibration |

---

## Limitations

- Limited cross-section data  
- Simplified river geometry and constant wave celerity  
- Missing short-interval tidal data  
- Incomplete 2D boundary setup  

---

## References

Data from **BWDB** and **Copernicus GLO-30 DEM**.  
Based on the same dataset as the term paper *“Hydrodynamic Assessment of Tidal-Induced Backwater and Bridge-Induced Velocity Effects on the Halda River Using HEC-RAS.”*

