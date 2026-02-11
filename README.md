# R Shiny App for Pharmacometrics

This repository contains a Shiny-based pharmacometrics prototype that reproduces core Monolix/Simulx workflows using open-source R packages only.

## 🎯 Purpose

The goal of this project is to demonstrate:
- Nonlinear mixed-effects PK modeling
- Simulation-based diagnostics
- Reproducible, open-source alternatives to proprietary tools

## 🔁 Monolix → R Mapping

| Monolix / Simulx | R Equivalent |
|------------------|--------------|
| Structural model | Closed-form PK equations |
| Random effects | `random = ~ 1 | id` |
| Simulx | Monte Carlo simulation in R |
| VPC | Quantile-based ggplot |
| AUC | `pracma::trapz()` |

## 📐 Model

- One-compartment oral PK model
- First-order absorption
- Log-normal inter-individual variability
- 
## 📂 Input Data

Required columns: id,time,conc,dose

## 🧪 Outputs

- Parameter estimates
- Observed vs predicted plots
- Visual Predictive Check
- Simulated concentration–time profiles
- Individual AUC summaries

## 🚀 Run the App

```r
shiny::runApp("app.R")
