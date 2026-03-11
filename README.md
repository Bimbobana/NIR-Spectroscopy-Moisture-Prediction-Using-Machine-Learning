# NIR Spectroscopy Moisture Prediction

Machine learning project for predicting wood moisture content using Near-Infrared (NIR) spectroscopy data.

This project demonstrates a practical data science workflow including:

- Exploratory Data Analysis (EDA)
- Spectral data investigation
- Feature correlation analysis
- Dimensionality reduction
- Machine learning modeling

---

## Table of Contents

- Project Overview
- Dataset
- Repository Structure
- Exploratory Data Analysis
- Example Visualization
- Mean Spectrum
- Spectral Correlation With Moisture
- PCA Spectral Clusters
- Water Absorption Bands
- Model Results
- Prediction Performance
- Key Findings
- Future Work
- Technologies Used
- Author

---

## Project Overview

Near-Infrared (NIR) spectroscopy allows rapid and non-destructive measurement of material properties. In forestry and wood processing, it can be used to estimate moisture content from spectral signals.

In this project, spectral measurements from wood samples are analyzed to determine whether machine learning models can accurately predict moisture content.

Key challenges in the dataset include:

- High-dimensional spectral data (1555 wavelengths)
- Strong correlation between neighboring wavelengths
- Differences between wood species

---

## Dataset

The dataset contains NIR spectral measurements and corresponding moisture values.

| Feature | Description |
|------|------|
| Samples | 1322 wood samples |
| Spectral features | 1555 wavelengths |
| Wavenumber range | ~10000 – 4000 cm⁻¹ |
| Wood species | 13 |
| Target variable | Moisture Content |

Each row represents a wood sample, while each spectral column represents reflectance at a specific wavenumber.

---

## Repository Structure

NIR-Spectroscopy-Moisture-Prediction
│
├── data
│   └── raw dataset files
│
├── notebooks
│   └── 01_EDA.ipynb
│
├── docs
│   ├── eda_en.md
│   ├── eda_ja.md
│   ├── moisture_by_species.png
│   ├── mean_spectrum.png
│   ├── moisture_correlation_heatmap.png
│   ├── pca_spectral_clusters.png
│   └── prediction_results.png
│
├── src
│   └── future modeling code
│
└── README.md

---

## Exploratory Data Analysis

Exploratory analysis was conducted to understand the structure of the dataset and identify patterns in the spectral measurements.

The analysis focused on:

- Distribution of moisture values across samples
- Differences in moisture between wood species
- Correlation between spectral wavelengths and moisture content
- Redundancy among spectral features

Detailed EDA documentation is available in the project documentation folder:

- English: docs/eda_en.md  
- Japanese: docs/eda_ja.md

---

## Moisture Distribution by Species

The following box plot shows how moisture content varies across different wood species in the dataset.

Moisture Distribution by Species

The visualization highlights differences in moisture ranges and variability between species, suggesting that species may influence moisture content and should be considered during modeling.

![Moisture Distribution](docs/moisture_by_species.png)

![Mean Spectrum](docs/mean_spectrum.png)

![Spectral Correlation](docs/moisture_correlation_heatmap.png)

![PCA Clusters](docs/pca_spectral_clusters.png)

![Prediction Results](docs/prediction_results.png)
