# MATH38161 Coursework - Gaussian Mixture Model Analysis

## Overview
This project is part of the MATH38161 coursework and focuses on clustering analysis of the **Old Faithful Geyser dataset** using **Gaussian Mixture Models (GMMs)**. The goal is to determine the optimal number of clusters using statistical model selection criteria such as **Bayesian Information Criterion (BIC)** and **Akaike Information Criterion (AIC)**.

## Dataset
The dataset comprises **299 observations** from the Old Faithful Geyser in Yellowstone National Park. It contains two key features:
1. **Waiting time** between eruptions.
2. **Eruption duration**.

## Methods Used
The analysis employs **Gaussian Mixture Models (GMMs)** with the `mclust` package in R:
1. **Data Preprocessing**: Standardizing the dataset.
2. **Model Fitting**: Applying GMMs with different cluster numbers.
3. **Model Selection**:
   - Evaluating **BIC and AIC** to determine the optimal cluster count.
   - Identifying the best model structure.
4. **Visualization**: Generating cluster plots to interpret results.

## Results
- The **BIC criterion** suggests an optimal cluster count of **4** with a **VVI (diagonal, varying volume and shape) model**.
- The **AIC criterion** suggests **8 clusters** with a **VEV (ellipsoidal, equal shape) model**.
- Visualizations confirm the clustering structure and the separation of data points.

## How to Run
1. **Install Dependencies**:
   ```r
   install.packages("mclust")
   library(mclust)
   ```
2. **Load Dataset**:
   ```r
   data(geyser, package = "MASS")
   ```
3. **Run Analysis**:
   ```r
   source("MATH38161_analysis.R")
   ```
4. **Interpret Results**: Check plots and model summaries to understand clustering patterns.

## Conclusion
The analysis demonstrates that **GMMs effectively cluster the geyser eruption data**, with the **VVI model** being the best fit based on BIC. However, AIC suggests a more complex model with additional clusters. The findings highlight the importance of model selection in unsupervised learning.

