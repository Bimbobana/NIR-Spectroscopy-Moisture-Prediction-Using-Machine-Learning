# Exploratory Data Analysis (EDA)

## Dataset Overview

This dataset contains Near-Infrared (NIR) spectroscopy measurements used to predict the moisture content of wood samples.

**Dataset structure**

- Samples: **1322**
- Spectral features: **1555 wavelengths**
- Wood species: **13**
- Target variable: **Moisture Content**

Each row represents a wood sample and each spectral column corresponds to a wavelength measurement between approximately **10000 and 4000 cm⁻¹**.

---

## Moisture Distribution

Moisture values span a very large range.

| Statistic | Value |
|---|---|
| Minimum | ~0.84 |
| Maximum | ~298.58 |
| Median | ~29 |

This indicates the dataset contains both extremely dry and very wet samples.

---

## Species Influence

Moisture distributions vary significantly by species.

Examples:

| Species | Mean Moisture |
|---|---|
| 3 | ~15 |
| 12 | ~31 |
| 1 | ~78 |
| 15 | ~88 |

This suggests that **species information is an important predictive feature**.

---

## Spectral Correlation with Moisture

Correlation analysis between spectral wavelengths and moisture revealed strong relationships.

Observed correlation range:

0.65 – 0.75

The strongest correlations appear in the **higher wavenumber region (~10000–6000 cm⁻¹)**.

---

## Spectral Feature Redundancy

Neighboring wavelengths are extremely correlated.

Example correlations:

0.9999  
0.9998  
0.9997  

This is expected because NIR spectra form **smooth continuous curves**.

Implication:

- Many wavelengths contain redundant information
- Dimensionality reduction techniques may be useful

---

## Data Quality

Missing value check:

0 missing values

The dataset is clean and ready for modeling.

---

## Key Insights

1. NIR spectra contain a strong signal for moisture prediction.
2. Spectral features are highly correlated with each other.
3. Moisture distribution varies significantly by species.
4. The dataset contains no missing values.

---

## Modeling Implications

Because of the high dimensionality and strong spectral correlation, suitable models include:

- Partial Least Squares Regression (PLS)
- PCA + Regression
- Ridge Regression
- Other regularized models

These approaches work well for high-dimensional spectroscopy data.
