# Technology Diffusion in Genetically Engineered Crops

## A Panel Data Analysis of U.S. Corn Adoption

This project examines the adoption dynamics of genetically engineered (GE) crop technologies across U.S. states, focusing on the transition from single-trait technologies to stacked gene varieties using panel data econometric methods.

## Introduction

Genetically engineered (GE) crops have transformed modern agriculture through the introduction of traits such as herbicide tolerance (HT) and insect resistance (Bt). Over time, these single-trait technologies have been combined into stacked gene varieties, offering multiple benefits simultaneously.

This study investigates whether adoption patterns reflect a transition from single-trait to multi-trait technologies.

## Tools Used

- Python (pandas, numpy)
- matplotlib
- statsmodels
- linearmodels (PanelOLS)
  
## Data Processing
The dataset contains state-level panel data on GE crop adoption across multiple years (State × Year structure).

Key steps:

* Cleaned encoding issues (`latin1`)
* Converted data from long to wide format using pivot tables
* Standardized column names
* Handled missing values

## Exploratory Data Analysis
This pattern suggests a shift from early-stage adoption of single-trait technologies toward more advanced multi-trait (stacked) innovations.

<img width="578" height="457" alt="plt savefig outputs trend_plot" src="https://github.com/user-attachments/assets/665a6d1c-b974-4d64-b6b0-a33f279db125" />


The relationship between Bt and stacked adoption suggests a negative association, indicating substitution between technologies.

<img width="575" height="457" alt="plt savefig scatter_plot" src="https://github.com/user-attachments/assets/1f3ad748-a85c-458b-88f3-9e2be229e8a6" />

## Econometric Model

A fixed-effects panel regression was estimated to analyze the relationship between single-trait and stacked GE crop adoption:

Stacked_it = β1 HT_it + β2 Bt_it + α_i + γ_t + ε_it

Where:

* α_i represents state fixed effects
* γ_t represents time fixed effects
  
This specification controls for unobserved heterogeneity across states and common shocks over time.

## Key Results

| Variable | Coefficient | P-value | Interpretation                  |
| -------- | ----------- | ------- | ------------------------------- |
| HT       | -0.034      | 0.593   | Not statistically significant   |
| Bt       | -0.494      | 0.000   | Negative and highly significant |

* R-squared (within): **0.263**
* F-statistic: **46.94 (p < 0.01)**


## Interpretation

The results show that insect-resistant (Bt) adoption has a negative and statistically significant effect on stacked gene adoption. This indicates a substitution effect, where farmers transition from single-trait Bt varieties to more advanced stacked technologies.

In contrast, herbicide-tolerant (HT) adoption is not statistically significant, suggesting it does not play a major role in driving technological upgrading.

1% increase in Bt adoption is associated with a 0.49% decrease in stacked adoption, holding other factors constant.

## Conclusion

The findings provide strong evidence of technological upgrading in GE crop adoption. Farmers initially adopt single-trait technologies but gradually transition to stacked gene varieties that combine multiple traits. This pattern is consistent with technology diffusion theory in agricultural systems.

This pattern is consistent with technology diffusion and upgrading theory, where producers adopt increasingly sophisticated innovations over time.

## Author
Abiodun Ikeowo

![Python](https://img.shields.io/badge/Python-Data%20Analysis-blue)
