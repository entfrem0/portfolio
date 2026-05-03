
title: Data Analysis - Computer Fluid Dynamics
layout: default
section: report
date: 2026-02-05
nav_order: 1
lead: 
updated: 2026-02-05



# Computational Fluid Dynamics Analysis

## Overview
This project analyzes a fluid dynamics dataset to understand the relationship between pressure, velocity, and acceleration.  
The main focus is on predicting the y-direction acceleration (dv/dt) using both statistical analysis and machine learning methods.



## Report (Full Version)

<div class="pdf-container">
  <iframe 
    src="https://drive.google.com/file/d/1qxphbqVtqhZ9bo3nbUPzfJ-pbJczeT-R/preview"
    allow="autoplay">
  </iframe>
</div>



## Background

The analysis is based on the Navier–Stokes equations, which describe fluid motion.  
Key variables include:

- **Dependent variables**: velocity (u, v), pressure (p)  
- **Independent variables**: spatial coordinates (x, y), time (t), and derivatives  

The dataset consists of **10,000 samples**, including both laminar and turbulent flows. 



## Objectives

- Understand physical relationships in fluid flow  
- Analyze pressure–velocity–acceleration interactions  
- Build predictive models for dv/dt  
- Compare performance across different flow regimes  



## Exploratory Data Analysis

### Key Observations

- Pressure differences influence acceleration  
- Higher velocity tends to correspond to lower pressure (Bernoulli principle)  
- Turbulent flow shows higher variability compared to laminar flow 

### Visualization

- Pressure vs acceleration  
- Velocity vs pressure  
- Velocity vs acceleration  
- Velocity field (u–v plane)



## Statistical Analysis

Descriptive statistics revealed:

- Large variability in pressure and acceleration  
- Clear structural differences between laminar and turbulent flows 
Hypothesis testing (ANCOVA) showed:

- Interaction between pressure and flow type is significant  
- Pressure gradient contributes to acceleration behavior  



## Machine Learning Approach

### Models Used

- K-Nearest Neighbors Regression (KNR)  
- Support Vector Regression (SVR)

### Features

- t, u, v, p, dudt  

### Target

- dvdt  



## Results

### Baseline Performance

- R² ≈ 0.088  
- Moderate predictive accuracy  

### Key Findings

- Models perform better in **laminar flow**  
- Prediction errors increase in **turbulent flow**  
- SVR provides more stable predictions



## Improvements

- Cross-validation (Repeated K-Fold)  
- PCA for dimensionality reduction  

These improved the **stability** of model performance, even if average accuracy remained similar.



## Discussion

This project highlights the importance of:

- Combining **physics-based understanding** with data-driven methods  
- Evaluating models carefully using cross-validation  
- Considering flow regimes when modeling complex systems  



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