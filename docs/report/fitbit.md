---
title: Fitbit Data Analysis (Heart Rate and Steps)
layout: default
section: report
date: 2026-05-03
nav_order: 1
lead: This report presents an analysis of daily activity patterns and physiological rhythms using step count and heart rate data collected from Fitbit devices.
updated: 2026-05-03
---


#  Fitbit Data Analysis (March 2026)

## Overview

This report presents an analysis of daily activity patterns and physiological rhythms using step count and heart rate data collected from Fitbit devices.

The analysis includes:

- Daily step trends  
- Activity patterns by weekday and time of day  
- Relationship between steps and heart rate  
- Regression modeling  
- Fourier analysis (FFT) for periodic structure  

The results show that heart rate is influenced not only by physical activity but also by strong circadian rhythms.

##  Key Highlights

- Daily steps ranged from ~4,000 to 18,000 steps, showing high variability  
- Clear circadian patterns in heart rate were observed  
- A positive correlation exists between steps and heart rate, though with large variance  
- Fourier analysis revealed dominant 24-hour and 12-hour cycles  
- Heart rate dynamics can be modeled using both activity (steps) and time-based periodic features

These findings suggest that heart rate variability is primarily driven by both behavioral patterns and biological rhythms.

##  Full Report

You can view the complete report below:

<div class="pdf-container">
  <iframe 
    src="https://drive.google.com/file/d/1kof8JXsR_sNdP4p97nsgGhNhjoWkmBDi/preview" 
    width="100%" 
    height="100%">
  </iframe>
</div>

##  Technical Approach

The analysis was conducted using:

- Python (pandas, numpy, matplotlib)
- Scikit-learn (Linear Regression)
- Time series analysis techniques
- Fourier Transform (FFT)

Key modeling approach:

$$
\mathrm{BPM}(t) = a \cdot \mathrm{steps}(t) + b \sin\left(\frac{2\pi t}{24}\right) + c \cos\left(\frac{2\pi t}{24}\right)
$$

This allows simultaneous modeling of:

- Physical activity (steps)  
- Biological rhythms (time periodicity)  

## Insights

- Heart rate is not purely random but follows a structured periodic pattern
- Activity alone cannot fully explain heart rate variation  
- Combining regression + Fourier analysis provides deeper understanding  
- The data exhibits a clear multi-scale temporal structure

## Future Work

- Incorporating higher-order Fourier components  
- Noise filtering and signal smoothing  
- Integration with sleep and HRV data  
- Building predictive time-series models  
