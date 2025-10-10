# Air Quality Prediction Analysis

## Overview

This project analyzes the UCI Air Quality Dataset to predict high pollution events using machine learning techniques. The analysis includes comprehensive data preprocessing, exploratory data analysis (EDA), and implementation of multiple machine learning models to classify pollution events.

## How to Run

1. Clone the repository

``` git bash
git clone https://github.com/Hansen256/artificial_intelligence_coursework_redo
```

1. Ensure all required packages are installed

1. Open the Jupyter notebook:

   ```bash
   jupyter notebook air_quality_analysis.ipynb
   ```

1. Run all cells sequentially to reproduce the complete analysis

## Project Objectives

- Load and preprocess historical air quality measurements from an Italian monitoring station
- Perform exploratory data analysis to understand pollution patterns and relationships
- Build machine learning models to predict high pollution events
- Evaluate and compare model performance using cross-validation and ROC analysis

## Dataset

- **Source**: UCI Machine Learning Repository - Air Quality Dataset
- **Time Period**: March 2004 - February 2005 (hourly measurements)
- **Location**: Italian city monitoring station
- **Features**:
  - **Pollutants**: CO (Carbon Monoxide), NOₓ (Nitrogen Oxides), NO₂ (Nitrogen Dioxide), O₃ (Ozone)
  - **Environmental**: Temperature, Relative Humidity
  - **Temporal**: Date and time information
- **Target**: Binary classification of high vs. normal pollution events

## Analysis Components

### Part A: Data Loading & Preprocessing

- Load and inspect the raw air quality dataset
- Handle missing values (encoded as -200 in the dataset)
- Convert date/time strings to proper datetime format
- Remove rows with excessive missing data (>50% of columns)
- Impute remaining missing values using median values
- Normalize numerical features using standard scaling

### Part B: Exploratory Data Analysis (EDA)

- Statistical analysis of pollutant distributions
- Correlation analysis between different pollutants and environmental factors
- Temporal pattern analysis (hourly, daily, seasonal trends)
- Outlier detection and analysis
- Statistical hypothesis testing (weekday vs. weekend pollution levels)

### Part C: Machine Learning Implementation

- **Models Implemented**:
  - Logistic Regression (interpretable linear model)
  - Decision Tree Classifier (non-linear pattern recognition)
- **Evaluation Metrics**:
  - Cross-validation with stratified k-fold
  - Accuracy, Precision, Recall, F1-score
  - ROC-AUC analysis with curve visualization
  - Confusion matrix analysis

## Key Findings

- Strong correlations between combustion-related pollutants (CO, NOx, NO2)
- Inverse relationship between O3 and primary pollutants
- Clear temporal patterns with peak pollution during specific hours
- Both models successfully classify high pollution events with good performance
- Significant differences in pollution levels between weekdays and weekends

## Technical Requirements

```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy
```

## Project Structure

```text
artificial_intelligence_coursework_redo/
├── air_quality_analysis.ipynb    # Main analysis notebook
├── AirQualityUCI.csv            # Dataset file
└── README.md                    # This file
```

## Model Performance

Both models demonstrate strong performance in classifying pollution events:

- **Logistic Regression**: Stable performance with good interpretability
- **Decision Tree**: Captures non-linear patterns with competitive accuracy
- Cross-validation ensures robust performance estimates

*This project demonstrates practical application of data science techniques to environmental monitoring and prediction.*
