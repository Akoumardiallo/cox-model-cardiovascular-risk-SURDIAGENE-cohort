
# cox-model-cardiovascular-risk-SURDIAGENE-cohort

## Description

This project presents a **survival analysis** examining cardiovascular mortality risk factors in patients with type 2 diabetes, using data from the **SURDIAGENE prospective cohort** (Poitiers University Hospital, France).

The main objective was to identify independent predictors of cardiovascular death, adjusting for diabetes duration, in a real-world clinical population followed over nearly 9 years.

## Dataset

- **Cohort**: SURDIAGENE (SUivi du Risque cardiovasculaire et renal dans le DIAbète de type 2 GENEtique)
- **Sample**: 1,193 patients with complete data (out of 1,409 included)
- **Follow-up**: Median 8.96 years (max: 13.87 years)
- **Outcome**: Cardiovascular death (n = 280, 23.5%)

## Methods

- Descriptive statistics stratified by cardiovascular death status
- Kaplan-Meier survival curves with log-rank test (overall and by sex)
- Univariate Cox proportional hazards models (selection threshold: p < 0.20)
- Multivariate Cox model with forced variables (age, sex, diabetes duration) and backward stepwise selection by AIC
- Proportional hazards assumption verified via Schoenfeld residuals and log(-log) plots
- Collinearity assessed via Pearson correlation matrix and Variance Inflation Factors (VIF)
- Sex interaction analysis with stratified models

## Key Results

Nine independent predictors were identified: age (HR=1.05), female sex (HR=0.75, protective), diabetes duration (HR=1.01), heart rate (HR=1.02), history of TIA (HR=1.52), coronary artery disease (HR=1.61), urinary sodium (HR=0.99), pro-adrenomedullin (HR=2.13), and proBNP (HR=2.59).

A significant sex × diabetes duration interaction was found (p=0.031): diabetes duration was an independent risk factor in women (HR=1.03, p=0.004) but not in men (p=0.77).

## Tools

`R 4.5.2` · `survival` · `survminer` · `MASS (stepAIC)` · `car (VIF)` · `ggplot2`

## Author

**Alpha Oumar Karim Diallo** — Master 2 MPCE Biostatistics, Nantes University / University of Rennes
