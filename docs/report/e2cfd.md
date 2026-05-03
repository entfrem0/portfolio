---
title: Data Analysis - Computer Fluid Dynamics
layout: default
section: report
date: 2026-02-05
nav_order: 1
lead: This project analyzes a fluid dynamics dataset to understand the relationship between pressure, velocity, and acceleration.
updated: 2026-02-05
---

> This page was automatically translated into English using ChatGPT.

# Computational Fluid Dynamics Analysis

## Overview
This project analyzes a fluid dynamics dataset to understand the relationship between pressure, velocity, and acceleration.  
The main focus is on predicting the y-direction acceleration (dv/dt) using both statistical analysis and machine learning methods.



## Report (Full Version)

<div class="pdf-container">
  <iframe 
    src="https://drive.google.com/file/d/18VwY0Zy07vOVMtP7KoV-1zsF6cOz-3VI/preview"
    allow="autoplay">
  </iframe>
</div>


## Background

This analysis is based on the Navier–Stokes equations, which describe fluid motion:

$$
\frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u} \cdot \nabla)\mathbf{u}
= -\frac{1}{\rho} \nabla p + \nu \nabla^2 \mathbf{u}
$$

where:

- $$\mathbf{u} = (u, v)$$: velocity field  
- $$p$$: pressure  
- $$\rho$$: density  
- $$\nu$$: kinematic viscosity  

Key variables include:

- **Dependent variables**: velocity $$(u, v)$$, pressure $$(p)$$  
- **Independent variables**: spatial coordinates $$(x, y)$$, time $$(t)$$  

The dataset consists of **10,000 samples**, including both laminar and turbulent flow regimes.



## Objectives

- Understand physical relationships in fluid flow  
- Analyze pressure–velocity–acceleration interactions  
- Build predictive models for:

$$
\frac{dv}{dt}
$$

- Compare model performance across different flow regimes  



## Exploratory Data Analysis

### Key Observations

- Pressure gradients influence acceleration:

$$
\frac{dv}{dt} \propto -\frac{\partial p}{\partial y}
$$

- Higher velocity tends to correspond to lower pressure (Bernoulli principle):

$$
p + \frac{1}{2} \rho u^2 = \text{constant}
$$

- Turbulent flow exhibits higher variability compared to laminar flow  

### Visualization

- Pressure vs acceleration  
- Velocity vs pressure  
- Velocity vs acceleration  
- Velocity field $$(u, v)$$ plane  



## Statistical Analysis

Descriptive statistics revealed:

- Large variability in pressure and acceleration  
- Clear structural differences between laminar and turbulent flows  

Hypothesis testing (ANCOVA) showed:

- Interaction between pressure and flow type is statistically significant  
- Pressure gradients contribute to acceleration behavior  



## Machine Learning Approach

### Models

- K-Nearest Neighbors Regression (KNR)  
- Support Vector Regression (SVR)

### Features

$$
t, \; u, \; v, \; p, \; \frac{du}{dt}
$$

### Target

$$
\frac{dv}{dt}
$$



## Results

### Baseline Performance

- $R^2 \approx 0.088$
- Moderate predictive accuracy  

### Key Findings

- Models perform better in **laminar flow**  
- Prediction errors increase in **turbulent flow**  
- SVR provides more stable predictions  



## Improvements

- Cross-validation (Repeated K-Fold)  
- Principal Component Analysis (PCA)  

These methods improved the **stability** of model performance, even though the average accuracy remained similar.



## Discussion

This project highlights the importance of:

- Combining **physics-based modeling** with data-driven approaches  
- Evaluating models carefully using cross-validation  
- Accounting for different flow regimes in complex systems  



## Conclusion

- Pressure plays a key role in fluid acceleration  
- Machine learning can approximate fluid behavior, but with limitations  
- Turbulence introduces significant complexity  
- Robust validation is essential for reliable modeling  



## Tech Stack

- Python  
- Pandas / NumPy  
- Scikit-learn  
- Data Visualization  

## Links

- Github: [https://github.com/entfrem0/E2_dataanalysis](https://github.com/entfrem0/E2_dataanalysis)