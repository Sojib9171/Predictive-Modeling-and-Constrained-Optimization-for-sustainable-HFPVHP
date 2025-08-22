# Outflow forecasting with LSTM with Constraint Validation for sustainable Hybrid Floating Photovoltaic-Hydropower (HFPVHP) systems


## Overview
This repository contains the implementation of a **research project** that integrates **machine learning** and **constraint solving** for sustainable water and energy management.  
The project focuses on combining **LSTM neural networks** for short-term outflow forecasting with **RealPaver constraint solving** to validate predictions against physical and operational limits.

---

## Research Objectives
- Forecast short-term **reservoir outflows** using LSTM models trained on historical hydrological data.  
- Guarantee that forecasts are **physically feasible** by validating them with RealPaver constraint solving.  
- Provide a **hybrid workflow** for reservoir release scheduling under climate and demand uncertainty.  
- Lay the foundation for future integration of **Hybrid Floating Photovoltaic-Hydropower (HFPVHP) systems** into reservoir management.

---

## Methodology
1. **Data Preprocessing**  
   - Historical reservoir data (storage, inflow, outflow, evaporation).  
   - Sliding-window sequences created for time-series learning.  

2. **LSTM Forecasting**  
   - Implemented in **TensorFlow/Keras**.  
   - Trained on **30-day windows** to predict **10-day reservoir outflows**.  

3. **Constraint Validation with RealPaver**  
   - Converts predictions into `.rp` files including:  
     - Initial storage  
     - Daily change constants  
     - Predicted releases (R1–R10)  
     - Storage capacity limits  
     - Mass balance equations  
   - RealPaver ensures forecasts respect **physical and operational constraints**.  

4. **Hybrid Workflow**  
   - LSTM = predictive accuracy.  
   - RealPaver = feasibility assurance.  
   - Together = actionable release schedules for dam managers.  

---

## Key Results
- LSTM produced accurate **outflow forecasts**.  
- RealPaver validated schedules, contracting wide intervals into **feasible, near-exact values**.  
- Demonstrates a **scalable decision-support tool** for water-energy management.  

---

## Ongoing/Future Work
- **Integration of Hybrid Floating Photovoltaic-Hydropower (HFPVHP) Systems**  
  Expanding the framework to optimize **joint water release and renewable energy production**, balancing solar variability with hydropower stability.  


- **Uncertainty Quantification**  
  Incorporating probabilistic inflow, evaporation, and price scenarios for more robust decision-making.  
