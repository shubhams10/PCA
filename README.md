# PCA
# Principal Component Analysis on Interest Rate Data

## Overview
This project applies **Principal Component Analysis (PCA)** to interest rate data from the US Treasury yield curve. The aim is to reduce the dimensionality of multiple maturities into a few key factors that explain most of the movement in the data.

## Objective
- Understand how PCA works in reducing correlated variables into principal components.
- Apply **linear algebra techniques** like eigenvalues, eigenvectors, and covariance matrices.
- Identify how many components explain most of the variance in the yield curve.
- Interpret these components as level, slope, and curvature factors.

## Dataset
- **Data Type:** Interest rates for different maturities (1Y to 10Y)
- **Period:** 5 consecutive days (January 2024)
- **Data Input:** Hard-coded data for demonstration

## Methodology
1. **Data Preparation**
   - Used interest rate data across 10 maturities.
   - Standardized the data to mean = 0 and standard deviation = 1.

2. **PCA Computation**
   - Computed the covariance matrix of the standardized data.
   - Performed eigenvalue and eigenvector decomposition to extract principal components.
   - Calculated explained variance for each component.

3. **Interpretation**
   - **PC1 (Level):** Explains ~99.7% of the variance; represents parallel shifts in rates.
   - **PC2 (Slope):** Explains ~0.18%; represents steepening or flattening of the curve.
   - **PC3 (Curvature):** Explains negligible variance; represents humps or dips in mid-maturities.

## Use Case
PCA on yield curves is widely used in:
- **Fixed Income Analytics:** Simplifying yield curve modeling.
- **Risk Management:** Identifying major factors affecting interest rate movements.
- **Dimensionality Reduction:** Feeding fewer factors into forecasting or stress testing models.

## Results
- Most changes in the yield curve are captured by the first principal component (level).
- Slope and curvature contribute minimally in this small dataset, but are significant in larger real-world datasets.

