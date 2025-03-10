# Comprehensive Biofilm Analysis

## Data Sources

Original Paper: Evolutionary and plastic responses of marine diatoms to ocean acidification and warming
Dataset: Zenodo Repository

The study examines a 400-generation selection experiment for bacterial biofilm formation under various environmental conditions, providing insights into diatom-bacteria interactions and adaptation mechanisms.

## Overview

The `ComprehensiveBiofilmAnalysis` class integrates multiple analytical approaches to study biofilm formation under varying temperatures and nutrient conditions. The analysis pipeline includes:

- Data loading and preprocessing
- Statistical analysis using parametric and non-parametric tests
- Bootstrap analysis for confidence interval estimation
- Growth curve modeling using logistic functions
- Polynomial fitting for trend analysis
- Visualization of biofilm coverage and formation patterns

## Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- scipy
- plotly.express
- scikit-learn

## Input Data Requirements

The analysis expects three CSV files:

1. `20183009_biofilm_characterise.csv`: Biofilm characterization data
   - Columns: characteristic, selection_temp, bio_replicate, nutrient, sampletype, traitvalue

2. `20180930_biofilm_trajectories.csv`: Biofilm formation trajectory data
   - Columns: cell_number, average_cell_size, pct_coverslip_covered, date, selection_temperature, nutrient_level, week, biofilm_formation_rate, evoplas, assay_temperature

3. `20180930Ability_to_form_biofilms.csv`: Biofilm formation ability data
   - Columns: cell_number, average_cell_size, %coverslip_covered, date, selection_temperature, nutrient_level, biofilm_formation_rate, evoplas, assay_temperature

## Key Features

### Statistical Analysis
- Automated selection between parametric (t-test) and non-parametric (Mann-Whitney U) tests based on normality
- Statistical comparison across temperature conditions and nutrient levels
- Bootstrap analysis for robust confidence interval estimation

### Visualization
- Time series plots of biofilm coverage
- Box plots showing distribution of coverage by temperature and nutrient level
- Bootstrap distribution visualization
- Growth curve fitting and polynomial analysis plots

### Growth Modeling
- Logistic function fitting for biofilm growth curves
- Polynomial fitting with various degrees for trend analysis
- MSE calculation for model comparison


## Output Interpretation

### Statistical Results
- The analysis provides p-values for comparing nutrient conditions at each temperature
- Statistical significance is determined at α = 0.05
- Test selection is automated based on Shapiro-Wilk normality test results

### Bootstrap Analysis
- Provides 95% confidence intervals for biofilm coverage
- Visualizes the sampling distribution
- Helps assess the reliability of mean estimates

### Visualization Outputs
- Growth trajectories across different conditions
- Coverage distributions by temperature and nutrient level
- Model fits and residual analysis

