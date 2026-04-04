# Technology Diffusion in Genetically Engineered Crops  
## A Panel Data Analysis of U.S. Corn Adoption

This project examines the adoption dynamics of genetically engineered (GE) crop technologies across U.S. states, focusing on the transition from single-trait technologies to stacked gene varieties using panel data econometric methods.

## Introduction
## Data Loading
## Data Cleaning
## Exploratory Data Analysis
The trend shows a steady increase in stacked gene adoption, indicating progressive technological upgrading over time.
We estimate a fixed-effects panel model to control for unobserved state-level heterogeneity and time-specific effects.
## Econometric Model

A fixed-effects panel regression was estimated to analyze the relationship between single-trait and stacked GE crop adoption:

Stacked_it = β1 HT_it + β2 Bt_it + α_i + γ_t + ε_it

Where:
- α_i represents state fixed effects  
- γ_t represents time fixed effects  
## Results
## 📊 Key Results

| Variable | Coefficient | P-value | Interpretation |
|--------|------------|--------|----------------|
| HT     | -0.034     | 0.593  | Not statistically significant |
| Bt     | -0.494     | 0.000  | Negative and highly significant |

- R-squared (within): **0.263**
- F-statistic: **46.94 (p < 0.01)**

## Interpretation

The results show that insect-resistant (Bt) adoption has a negative and statistically significant effect on stacked gene adoption. This indicates a substitution effect, where farmers transition from single-trait Bt varieties to more advanced stacked technologies.

In contrast, herbicide-tolerant (HT) adoption is not statistically significant, suggesting it does not play a major role in driving technological upgrading.

Overall, the findings provide evidence of technology diffusion and upgrading in agricultural production systems.

> A 1% increase in Bt adoption is associated with a 0.49% decrease in stacked adoption, holding other factors constant.
## Conclusion


