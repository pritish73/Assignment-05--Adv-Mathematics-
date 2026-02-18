# Assignment-05--Adv-Mathematics
# Learning Probability Density Functions using Roll-Number-Parameterized Non-Linear Model

A Python-based statistical analysis project that learns probability density function parameters from transformed air quality data using maximum likelihood estimation and Gaussian modeling.

---

## Student Information

**Name:** Pritish Dutta  
**Roll Number:** 102303473  
   
---

## Overview

This project applies a **roll-number-parameterized non-linear transformation** to Nitrogen Dioxide (NO₂) measurements and estimates the parameters of a Gaussian-like probability density function.

The notebook demonstrates how mathematical transformations combined with statistical methods can model real-world environmental data distributions.

---

## Objectives

- Apply a **non-linear transformation** to NO₂ concentration values  
- Estimate distribution parameters (**μ, σ, λ, c**) using sample statistics  
- Fit a **Gaussian probability density function**  
- Visualize empirical vs theoretical distributions  

---

## Dataset

**Source:** India Air Quality Dataset (Kaggle)  
**Feature Used:** NO₂ (Nitrogen Dioxide) concentration levels  

The dataset contains real-world pollution measurements, making it ideal for statistical modeling and probability analysis.

---

## Methodology

### Step 1: Parameterized Non-Linear Transformation
-  z = Tr(x) = x + ar · sin(br · x)

Where:
- `ar = 0.05 × (r mod 7)`
- `br = 0.3 × (r mod 5 + 1)`
- `r` = University Roll Number (**102317200**)

**Calculated Parameters:**

- **ar = 0.30**  
- **br = 0.30**

---

### Step 2: Probability Density Function

The transformed data is modeled using:
 - p̂(z) = c × e^(-λ(z-μ)²)

Where:
- **μ (mu):** Mean of transformed data  
- **σ (sigma):** Standard deviation  
- **λ (lambda):** Precision parameter = 1/(2σ²)  
- **c:** Normalization constant = 1/(σ√(2π))  

Parameters are computed directly from the dataset using NumPy.

---

### Step 3: Visualization

The notebook generates:
- Histogram of transformed data  
- Overlaid Gaussian probability density curve  
- Visual comparison between empirical and theoretical distributions  

This helps validate how well the fitted model represents the data.

---

## Technologies Used

- **Python**
- **NumPy** — numerical computations  
- **Pandas** — data manipulation  
- **Matplotlib** — visualization  
- **Jupyter Notebook / Kaggle**

---

## Results

- Successful transformation of raw NO₂ data  
- Accurate parameter estimation using statistical formulas  
- Gaussian distribution closely fits the transformed dataset  
- Visual validation confirms strong alignment  

---

##  Mathematical Foundation

Gaussian probability density function:
 - p̂(z) = (1 / (σ√(2π))) × e^(-(z-μ)² / (2σ²))
 
Reparameterized as:
 - p̂(z) = c × e^(-λ(z-μ)²)

Where:
- `λ = 1/(2σ²)`  
- `c = 1/(σ√(2π))`

---

## Key Insights
- The non-linear transformation slightly alters the original pollution data distribution  
- The transformed dataset approximately follows a normal distribution  
- Demonstrates the effectiveness of statistical modeling on environmental datasets  

---

## How to Run

```bash
# Clone the repository
git clone https://github.com/<your-username>/<repo-name>.git

# Install dependencies
pip install pandas numpy matplotlib

# Launch notebook
jupyter notebook


