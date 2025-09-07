# Egyptian Fruit Bat Foraging Behavior Analysis

## Project Overview

This repository contains a comprehensive data science analysis of Egyptian Fruit Bat (*Rousettus aegyptiacus*) foraging behavior in the presence of Black Rats (*Rattus rattus*). The study investigates two key behavioral ecology questions through statistical analysis of observational data collected over a 7-month period in a semi-natural bat colony.

## Research Context

A team of zoologists monitored bat-rat interactions on a provisioned food platform using surveillance video cameras to understand:
1. Whether bats perceive rats as potential predators (beyond just competitors)
2. How these behavioral responses change with seasonal variations in food availability and rat encounters

## Investigations

### Investigation A: Predator Perception
**Research Question**: Do bats perceive rats not just as competitors for food but also as potential predators?

**Hypothesis**: If rats are considered a predation risk, bats will exhibit higher avoidance behavior or increased vigilance (longer landing times) when rats are present.

**Analysis**: Two-sample t-test comparing bat landing durations when rats are present vs. absent.

### Investigation B: Seasonal Behavioral Changes
**Research Question**: Do risk behaviors change following seasonal changes?

**Context**: 
- **Winter**: Alternative food sources are scarce, rat encounters are less frequent
- **Spring**: Food is more abundant, rat encounters are more common

**Analysis**: Two-sample t-test comparing risk behavior patterns between winter and spring seasons.

## Repository Contents

- `bat_rat_analysis.ipynb` - Complete Jupyter notebook containing all analyses
- `dataset1.csv` - Individual bat landing events with behavioral metrics
- `dataset2.csv` - Aggregated 30-minute period activity data
- `README.md` - This documentation

## Technical Approach

### Data Science Techniques Applied
- **Missing Data Handling**: KNN imputation for robust data preprocessing
- **Feature Engineering**: Creation of risk scores and temporal indicators
- **Exploratory Data Analysis**: Correlation analysis and descriptive statistics
- **Linear Regression**: Predictive modeling of bat behavior patterns
- **Statistical Testing**: 
  - Central Limit Theorem demonstration
  - Confidence intervals calculation
  - One-sample and two-sample t-tests
  - Effect size analysis (Cohen's d)

### Key Features
- **Adaptive Analysis**: Code automatically adapts to different data structures
- **Comprehensive Visualizations**: 2×2 subplot layouts showing multiple analytical perspectives
- **Statistical Rigor**: Proper hypothesis testing with effect size interpretation
- **Biological Context**: Results interpreted within behavioral ecology framework

## Dataset Information

### Dataset 1: Individual Bat Events
- **bat_landing_to_food**: Duration from landing to reaching food (seconds)
- **habit**: Feeding behavior type (rat-deterred, fast, pick)
- **risk**: Rat presence indicator (0 = absent, 1 = present)
- **reward**: Successful feeding outcome (0 = no, 1 = yes)
- **season**: Seasonal period (0 = winter, 1 = spring)
- **hours_after_sunset**: Temporal feeding pattern data

### Dataset 2: Aggregated Activity (Augmented)
- **bat_landing_number**: Count of bat landings per 30-min period
- **rat_arrival_number**: Count of rat arrivals per 30-min period
- **food_availability**: Available food quantity
- **season**: Added through month-season mapping from Dataset 1

## Key Findings

The analysis provides statistical evidence for:
1. **Predator perception effects** on bat vigilance behavior
2. **Seasonal variation** in risk assessment strategies
3. **Environmental factor influences** on foraging decisions

## Academic Context

This project was completed as part of **HIT140 Foundations of Data Science** at Charles Darwin University (Assessment 2: Group Project Presentation, 40% weighting). The analysis demonstrates application of statistical methods learned in Weeks 1-5, focusing on real-world behavioral ecology data.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scipy
- scikit-learn

## Usage

1. Clone the repository
2. Ensure datasets (`dataset1.csv`, `dataset2.csv`) are in the same directory
3. Run `bat_rat_analysis.ipynb` in Jupyter Notebook/Lab
4. Execute cells sequentially for complete analysis

## Statistical Methods

- **Hypothesis Testing**: Rigorous statistical testing with α = 0.05
- **Effect Size Analysis**: Cohen's d for practical significance assessment
- **Data Validation**: Multiple analytical approaches for robust conclusions
- **Visualization**: Enhanced plots for clear result communication

## Contributing

This analysis was developed for academic assessment purposes. The methodology can be adapted for similar behavioral ecology studies involving predator-prey interactions and seasonal behavioral variations.

---

*Note: This project demonstrates the application of data science techniques to real behavioral ecology research questions, bridging statistical methodology with biological understanding.*
