# Transport Accessibility and Robbery in London

**Spatial analysis and predictive modelling of London robbery rates using public transport accessibility and station proximity.**

[View the 13-page research briefing (PDF)](./Robbery_Research_Brief.pdf)

## Research question

Do public transport accessibility and proximity to rail-based stations improve the prediction of robbery rates across London LSOAs?

## Project overview

This individual MSc project compared baseline neighbourhood models with transport-extended models across **4,988 London LSOAs**, using 2023 crime, population, deprivation and transport data.

The baseline specification included deprivation, population density and the share of residents aged 16–24. The extended specification added:

- mean PTAL Accessibility Index;
- straight-line distance to the nearest TfL rail-based station.

Three model families were compared: **Linear Regression, Random Forest and XGBoost**.

## Key findings

- Adding transport indicators improved prediction across all three model families.
- Under borough-grouped cross-validation, the mean XGBoost \(R^2\) increased from **0.135 to 0.421**, while RMSE decreased from **0.716 to 0.584**.
- Mean PTAL Accessibility Index had the highest permutation importance among the included predictors.
- Station proximity contributed less predictive information than the broader PTAL accessibility measure.
- These results are predictive associations and should not be interpreted as causal effects.

## Methods

1. Integrated and checked multi-source spatial data.
2. Screened candidate crime outcomes and tested sensitivity to central-London extremes.
3. Calculated LSOA centroid-to-station distances using projected geometry.
4. Compared baseline and transport-extended model specifications.
5. Tuned and interpreted the final XGBoost model.
6. Assessed spatial sensitivity through residual mapping and borough-grouped cross-validation.

## Data sources

- Metropolitan Police Service crime counts;
- 2023 small-area population and age estimates;
- English Indices of Deprivation;
- TfL public transport accessibility and rail-station locations;
- London LSOA boundaries.

## Tools and techniques

- Python, pandas and GeoPandas;
- scikit-learn and XGBoost;
- spatial data integration and coverage checks;
- regression and machine-learning model comparison;
- permutation importance and partial dependence;
- residual mapping and geographically grouped validation;
- technical reporting and data visualisation.

## Limitations

Resident population does not capture commuters, visitors or commercial activity. LSOA averages and centroid-based distances simplify real journeys and station environments. Borough-grouped validation tests geographical sensitivity but does not eliminate all spatial dependence.

## Repository contents

- [`Robbery_Research_Brief.pdf`](./Robbery_Research_Brief.pdf) — visual research briefing with findings, maps, model evaluation and technical appendices.

## Author

**Hanyun Hu**  
MSc Urban Spatial Science, University College London  
[LinkedIn](https://www.linkedin.com/in/hanyun-hu-4a45b23a9/)
