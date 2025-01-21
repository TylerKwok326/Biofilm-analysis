# Comprehensive Biofilm Analysis

This Python package provides a comprehensive toolkit for analyzing biofilm formation and characteristics across different environmental conditions. The analysis includes statistical testing, bootstrap analysis, growth modeling, and visualization of biofilm development patterns.
Overview
The ComprehensiveBiofilmAnalysis class integrates multiple analytical approaches to study biofilm formation under varying temperatures and nutrient conditions. The analysis pipeline includes:

Data loading and preprocessing
Statistical analysis using parametric and non-parametric tests
Bootstrap analysis for confidence interval estimation
Growth curve modeling using logistic functions
Polynomial fitting for trend analysis
Visualization of biofilm coverage and formation patterns

Dependencies

pandas
numpy
matplotlib
seaborn
scipy
plotly.express
scikit-learn

Input Data Requirements
The analysis expects three CSV files:

20183009_biofilm_characterise.csv: Biofilm characterization data

Columns: characteristic, selection_temp, bio_replicate, nutrient, sampletype, traitvalue


20180930_biofilm_trajectories.csv: Biofilm formation trajectory data

Columns: cell_number, average_cell_size, pct_coverslip_covered, date, selection_temperature, nutrient_level, week, biofilm_formation_rate, evoplas, assay_temperature


20180930Ability_to_form_biofilms.csv: Biofilm formation ability data

Columns: cell_number, average_cell_size, %coverslip_covered, date, selection_temperature, nutrient_level, biofilm_formation_rate, evoplas, assay_temperature



Key Features
Statistical Analysis

Automated selection between parametric (t-test) and non-parametric (Mann-Whitney U) tests based on normality
Statistical comparison across temperature conditions and nutrient levels
Bootstrap analysis for robust confidence interval estimation

Visualization

Time series plots of biofilm coverage
Box plots showing distribution of coverage by temperature and nutrient level
Bootstrap distribution visualization
Growth curve fitting and polynomial analysis plots

Growth Modeling

Logistic function fitting for biofilm growth curves
Polynomial fitting with various degrees for trend analysis
MSE calculation for model comparison

Usage
pythonCopy# Initialize the analyzer
analyzer = ComprehensiveBiofilmAnalysis()

# Run complete analysis pipeline
analyzer.run_complete_analysis()

# Or run individual components:
analyzer.load_all_datasets()
analyzer.prepare_characterization_data()
analyzer.statistical_analysis()
analyzer.create_visualizations()
Output Interpretation
Statistical Results

The analysis provides p-values for comparing nutrient conditions at each temperature
Statistical significance is determined at α = 0.05
Test selection is automated based on Shapiro-Wilk normality test results

Bootstrap Analysis

Provides 95% confidence intervals for biofilm coverage
Visualizes the sampling distribution
Helps assess the reliability of mean estimates

Visualization Outputs

Growth trajectories across different conditions
Coverage distributions by temperature and nutrient level
Model fits and residual analysis
