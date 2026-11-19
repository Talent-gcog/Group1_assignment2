# HASTS206 Assignment 2 — District Clustering Analysis

## Project Overview

This project applies K-means clustering to classify 24 districts based on demographic characteristics, migration patterns and piped-water access. The analysis aims to identify districts with similar characteristics and demonstrate the application of unsupervised machine learning in demographic analysis and planning.

## Objectives

- Classify 24 districts into meaningful clusters.
- Examine demographic structure, migration and piped-water access.
- Determine an appropriate number of clusters.
- Evaluate cluster quality and stability.
- Interpret the resulting district profiles for practical planning.

## Data and Features

The analysis uses district-level demographic and socioeconomic indicators derived from the supplied assignment datasets.

The four clustering features are:

- **Under-15 population (%):** Proportion of the district population younger than 15 years.
- **Age-65-plus population (%):** Proportion of the population aged 65 years and above.
- **Net migration rate:** Net migration per 1,000 population.
- **Piped-water access (%):** Proportion of the population with piped-water access.

## Methodology

The analysis follows these steps:

1. Data loading and inspection.
2. Feature engineering and data merging.
3. Missing-value assessment and median imputation.
4. Outlier assessment using boxplots.
5. Feature standardisation using StandardScaler.
6. K-means clustering using multiple values of k.
7. Cluster evaluation using the Elbow Method and Silhouette Analysis.
8. Cluster interpretation using centroids and visualisation.
9. Stability assessment using an alternative random seed and imputation method.

## Model Selection

The Elbow Method and Silhouette Analysis were used to evaluate cluster solutions.

The selected model was **K-means with k = 3**, which achieved a mean silhouette score of **0.8168**.

## Cluster Results

### Cluster 0 — Older-population districts

- Mean under-15 population: 9.49%
- Mean age-65-plus population: 27.89%
- Mean net migration rate: -1.53 per 1,000
- Mean piped-water access: 53.79%

### Cluster 1 — Migration-attracting districts

- Mean under-15 population: 12.90%
- Mean age-65-plus population: 12.56%
- Mean net migration rate: 12.01 per 1,000
- Mean piped-water access: 75.97%

### Cluster 2 — Younger-population districts

- Mean under-15 population: 28.97%
- Mean age-65-plus population: 14.59%
- Mean net migration rate: -2.77 per 1,000
- Mean piped-water access: 38.75%

## Stability Assessment

The model was tested using an alternative random seed and an alternative missing-value imputation approach.

Both tests achieved an Adjusted Rand Index (ARI) of **1.0000** against the original cluster assignments, indicating unchanged district memberships under the two tested variations.

## Practical Application

The clusters may support evidence-based planning, resource allocation and comparison of districts with similar demographic characteristics.

For example, younger-population districts with comparatively lower piped-water access may warrant further investigation when planning water infrastructure and child-related services.

## Limitations

The clustering analysis uses only four indicators. Other factors such as education, income, employment, healthcare access and urbanisation are not included.

The clusters are exploratory groupings and should not be interpreted as definitive classifications of districts.

## Tools and Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Project Files

- `clustering_analysis.ipynb` — Complete analysis and code.
- `clustering_analysis.html` — Exported notebook.
- `data/` — Supplied datasets.

---

**HASTS206 — Assignment 2, Section 4: District Clustering Analysis**
