# RIGI Policy Analysis: Causal Inference project

## Overview

This project evaluates the impact of the Milei administration's RIGI policy on firm-level stock returns using a Difference-in-Differences (DiD) model.

## Research Question

Did the implementation of RIGI generate a significant positive effect on the daily returns of Argentine energy companies relative to similar energy firms in Latin America?

## Empirical Design

The analysis uses a Difference-in-Differences regression with the following model: 

**Daily_Return ~ treated + post + treated_post**

* **treated**: identifies firms expected to benefit more directly from the policy
* **post**: indicates dates after RIGI was applied in Argentina
* **treated_post**: captures the DiD treatment effect

Additionally, this project:
* compares standard error specifications (non-robust vs. clustered)
* implements a placebo test using a random and false event date

## Regression results

* The estimated treatment effect is positive for firms in the treatment group, following the RIGI policy
* Statistical significance depends on the choice of standard error specification
* A placebo test yields no significant effect, supporting the timing-based interpretation
* Results are sensitive to modeling assumptions and should be interpreted cautiously

## Interpretation

The positive interaction coefficient suggests that treated firms experienced higher returns after the policy relative to controls. However, inference is not fully robust: the result is statistically significant under clustered standard errors but not under non-robust errors. Given the panel structure, clustering is appropriate, but the small number of firms limits the reliability of clustered inference.

## Limitations

* The analysis includes only six firms, which limits the reliability of clustered standard errors
* Results are sensitive to the choice of standard error specification
* Argentine firms experienced increased returns around the time of Javier Milei’s election, which may partially confound the estimated policy effect
* While the placebo test supports the timing of the effect, it does not fully establish causality
* The limited sample and time horizon may affect generalizability

## Files

* `rigi_policy_did_analysis.ipynb`: complete notebook with data preparation, regression analysis, placebo testing, and interpretation

## Skills

* Python (pandas, statsmodels)
* Data cleaning
* Causal inference
* Difference-in-Differences
* Regression analysis
* Robustness checks (placebo testing, alternative standard errors)
* Data visualization

## Author

Santiago Osorio
