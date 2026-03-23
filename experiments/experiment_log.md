# Experiment Log

## Baseline
Model: PLSRegression  
Score: 20.85  
Notes: Raw spectra without preprocessing performed best.

## Experiment 02
Model: PLS + StandardScaler  
Score: 27.58  
Notes: Scaling degraded performance.

## Experiment 03
Model: Savitzky–Golay derivative + species feature  
Score: 32.57  
Notes: Derivative preprocessing worsened predictions.

## Experiment 04

Model: ElasticNet  
Score: **17.65**

Pipeline:
Raw spectra → StandardScaler → ElasticNet

Observation:

ElasticNet significantly improved performance compared to PLS.

PLS baseline score: 20.85  
ElasticNet score: 17.65

ElasticNet likely benefits from sparse feature selection in high-dimensional spectral data (~1555 wavelengths).

Next step:

Wavelength selection to remove redundant spectral bands.
