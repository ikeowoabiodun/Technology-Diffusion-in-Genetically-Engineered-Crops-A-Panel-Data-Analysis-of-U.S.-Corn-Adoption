# Technology Diffusion and Adoption Dynamics in Genetically Engineered Crops: A Panel Data Analysis of U.S. Corn

## Problem Statement

Understanding how agricultural technologies diffuse over time is critical for improving productivity, sustainability, and innovation adoption in agribusiness systems. While genetically engineered (GE) crops have been widely adopted, less is known about the transition dynamics between different generations of technology, particularly the shift from single-trait to multi-trait (stacked) varieties.

This study investigates whether observed adoption patterns reflect technological upgrading behavior among farmers, using panel data econometric methods.

## Research Objective

To analyze the adoption dynamics of genetically engineered crop technologies and examine whether farmers transition from single-trait technologies (herbicide tolerance and insect resistance) to more advanced stacked gene varieties.


## Data Description

The dataset consists of state-level panel data on GE crop adoption in the United States, structured as:

- Cross-sectional units: U.S. states
- Time dimension: Multiple years

## Variables:

- Herbicide-tolerant (HT) adoption
- Insect-resistant (Bt) adoption
- Stacked gene adoption

This structure enables analysis of both cross-state variation and temporal dynamics.

  
## Methodology

This study applies a panel data econometric framework to capture both time and cross-sectional effects.

## Data Processing
- Cleaning encoding inconsistencies (latin1)
- Reshaping dataset (long to wide format)
- Standardizing variable names
- Handling missing values


## Exploratory Data Analysis
This pattern suggests a shift from early-stage adoption of single-trait technologies toward more advanced multi-trait (stacked) innovations.

<img width="578" height="457" alt="plt savefig outputs trend_plot" src="https://github.com/user-attachments/assets/665a6d1c-b974-4d64-b6b0-a33f279db125" />


The relationship between Bt and stacked adoption suggests a negative association, indicating substitution between technologies.

<img width="575" height="457" alt="plt savefig scatter_plot" src="https://github.com/user-attachments/assets/1f3ad748-a85c-458b-88f3-9e2be229e8a6" />


The visual evidence suggests a gradual shift from single-trait adoption toward stacked gene technologies.

## Econometric Model

The fixed-effects panel regression model is specified as:

\[
Stacked_{it} = \beta_1 HT_{it} + \beta_2 Bt_{it} + \alpha_i + \gamma_t + \varepsilon_{it}
\]

Where:

- $\alpha_i$ = State-specific fixed effects  
- $\gamma_t$ = Time-specific fixed effects  
- $\varepsilon_{it}$ = Error term

This specification controls for unobserved heterogeneity across states and common shocks over time.

## Key Results

| Variable | Coefficient | P-value | Interpretation                  |
| -------- | ----------- | ------- | ------------------------------- |
| HT       | -0.034      | 0.593   | Not statistically significant   |
| Bt       | -0.494      | 0.000   | Negative and highly significant |

* R-squared (within): **0.263**
* F-statistic: **46.94 (p < 0.01)**


## Interpretation of Findings
- Bt adoption has a negative and statistically significant relationship with stacked gene adoption, indicating a substitution effect.
- This suggests that farmers transition from single-trait Bt varieties to more advanced stacked technologies over time.
- Herbicide-tolerant (HT) adoption does not significantly influence this transition, indicating differing roles of individual technologies in the adoption process.

Overall, the findings provide empirical evidence of technology upgrading behavior in agricultural systems.

## Economic and Agribusiness Relevance

This study contributes to understanding:

- Technology diffusion in agriculture
- Farmer decision-making and adoption behavior
- Innovation upgrading in agribusiness systems

The analytical framework is applicable to developing-country contexts, including:

- Adoption of improved seed technologies
- Transition to climate-smart agriculture
- Scaling agricultural innovations

## Tools and Technologies
- Python (pandas, numpy)
- Visualization: matplotlib
- Econometrics: statsmodels, linearmodels (PanelOLS)

## Key Contribution

This project demonstrates the application of panel data econometrics to analyze real-world agricultural problems, highlighting the ability to:

- Handle longitudinal data
- Apply fixed-effects models
- Generate policy-relevant insights

## Author
Abiodun Ikeowo
MBA (Agribusiness)
Data Analyst (Python, SQL/SQLite, STATA)

![Python](https://img.shields.io/badge/Python-Data%20Analysis-blue)
