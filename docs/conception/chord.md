---
title: Audio-Based Analysis for Complex Jazz Chord Recognition
layout: default
section: conception
date: 2026-05-05
nav_order: 1
lead: This project focuses on audio-based analysis for recognizing complex jazz chords, including slash chords and tension chords.
updated: 2026-05-05
---

# Proposal: Audio-Based Analysis for Complex Jazz Chord Recognition

## 1. Background

In recent years, research in Music Information Retrieval (MIR) has made significant progress in tasks such as automatic transcription and chord recognition. However, most existing approaches primarily focus on relatively simple harmonic structures, such as triads and seventh chords. Recognition of more complex harmonic structures—such as tension chords and slash chords commonly used in jazz—remains a challenging problem.

For example, chords like Gm/C (a slash chord) or C7(#9, b13) (a tension chord) involve complex relationships between bass notes and upper harmonic structures. These characteristics make them difficult to identify not only for computational systems but also for human listeners.

From a personal perspective, I possess a strong sense of pitch, allowing me to identify tuning differences at the Hz level. I am also able to recognize common chords used in pop music with relative ease. However, I often struggle to accurately identify complex jazz chords such as slash chords and tension chords, where separating bass notes and harmonic structures becomes significantly more difficult. This experience motivated my interest in developing computational approaches to assist in complex chord recognition.

## 2. Objective

The objective of this study is to develop an audio-based analysis method for recognizing complex jazz chords, with a particular focus on:

- Slash chords (e.g., Gm/C)

- Tension chords (e.g., C7(#9, b13))

The goal is to design a system capable of estimating both bass notes and chord structures, and to improve recognition accuracy compared to conventional methods.

## 3. Methodology

### 3.1 Feature Extraction

Audio signals will be processed to extract chroma features, which represent the distribution of energy across the 12 pitch classes. Additionally, low-frequency analysis will be used to estimate bass notes, which is critical for identifying slash chords.

### 3.2 Chord Estimation Model

A two-stage approach will be adopted:

1. Bass note estimation  

2. Chord structure classification  

Machine learning models such as logistic regression, support vector machines, or neural networks will be used for classification tasks.

### 3.3 Tension Detection

Tension notes (e.g., b9, #11, 13) will be treated as extensions of basic chord structures. Their presence will be inferred from patterns in chroma features and additional spectral characteristics. Special attention will be given to distinguishing subtle pitch differences.

## 4. Dataset

The study will utilize the following datasets:

- MIDI datasets with annotated chord labels  

- Self-recorded audio data (e.g., piano recordings)

MIDI data will provide accurate ground truth labels, while recorded audio will allow evaluation in realistic conditions.


## 5. Expected Outcomes

This study is expected to improve the recognition of complex jazz chords that are difficult to identify using existing methods. The proposed system may also serve as a tool to assist musicians in ear training and transcription tasks.

## 6. Future Work

Future extensions may include:

- Handling polyphonic audio with multiple instruments  

- Real-time chord recognition  

- Integration of harmonic progression analysis (e.g., key modulation)

## 7. Required Python Libraries

To implement the proposed system, the following Python libraries will be utilized:

- **librosa**  
  A core library for audio signal processing and feature extraction. It will be used to compute spectrograms, chroma features, and other relevant audio representations.

- **numpy**  
  A fundamental package for numerical computation, used for handling arrays and mathematical operations on audio data.

- **pandas**  
  Used for organizing and managing structured data, such as chord labels and time-aligned annotations.

- **scikit-learn**  
  Provides machine learning algorithms (e.g., logistic regression, SVM) for baseline chord classification tasks.

- **PyTorch (or TensorFlow)**  
  Deep learning frameworks used to implement more advanced models, such as neural networks for chord recognition.

- **matplotlib / seaborn**  
  Visualization libraries used to plot spectrograms, chroma features, and evaluation results.

- **music21**  
  A toolkit for symbolic music analysis. It can be used to handle MIDI data, analyze chord structures, and assist in mapping between notes and chord labels.

- **scipy**  
  Used for signal processing tasks such as filtering and frequency analysis.

These libraries collectively support audio processing, feature extraction, machine learning, and data visualization, forming the technical foundation of the proposed system.