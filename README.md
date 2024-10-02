# Optimal Pseudo Counts for Transcription Factor Binding Sites

## Overview
This project investigates the optimal pseudo counts for transcription factor binding sites using a Python implementation based on the findings from the paper [“Title of the Paper”](https://pubmed.ncbi.nlm.nih.gov/19106141/). The aim is to enhance the representation of binding sites by evaluating how pseudo counts impact the artificial datasets derived from the JASPAR database.

## Table of Contents
- [Methodology](#methodology)
- [Results](#results)
- [Conclusion](#conclusion)

## Methodology
1. **Data Preparation:**
   - Utilized the JASPAR dataset to create an artificial dataset, maintaining the same distribution.
   - Introduced various pseudo counts (from 0.01 to 10, around 61 different numbers) to analyze their impact on the binding site matrices.

2. **Distance Metrics:**
   - Employed cosine similarity, Manhattan distance, and total variation distance to compare the original dataset with the artificial one.

3. **Functionality Testing:**
   - Generated sequences and scored them based on both the actual and artificial datasets.
   - Compared scores using the aforementioned distance metrics to evaluate how well the artificial dataset represented the actual dataset.

## Results
- **Optimal Pseudo Counts:**
  - For datasets of size around 30 with low entropy, the optimal pseudo count ranged from 0.8 to 1.2.
  - In larger datasets (size 50), optimal pseudo counts were around 5.
  - For smaller datasets (size 10), lower pseudo counts (e.g., 0.01) resulted in significant negative effects, while larger sizes showed less sensitivity.
  - High entropy datasets required larger pseudo counts, around 6, to maintain functionality.

## Conclusion
The project demonstrates that the choice of pseudo counts significantly influences the performance of artificial datasets in representing actual transcription factor binding sites. The findings suggest a general guideline for selecting pseudo counts based on dataset size and entropy.
