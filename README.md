# CHEG472_Week3_SAF

# Sustainable Aviation Fuel (SAF) Dataset Analysis

## Objective
To analyze the relationship between biomass feedstock characteristics, operating conditions, and Minimum Selling Price (MSP) of SAF produced through fast pyrolysis, with focus on clustering analysis based on plant location and capacity.

## Dataset Overview
- 186 samples with 14 features
- Features include:
  - Biomass composition (C, H, N, O, S percentages)
  - Process characteristics (VM%, Ash%, FC%)
  - Biomass properties (Cel%, Hem%, Lig%)
  - Plant parameters (Location, Capacity)
  - Target variable: MSP (Minimum Selling Price)

## Data Processing Steps
1. Outlier removal (36 rows removed) 
2. One-hot encoding of categorical variables (Location)
3. Multicollinearity handling for highly correlated features (threshold = 0.8)
   - C% and O% showed strong correlation (-0.94)

## Key Findings
1. Strongest correlations:
   - C% and O%: -0.94 (negative correlation)
   - N% and Ash%: 0.72 (positive correlation)
   - MSP and Location_China: -0.70 (negative correlation)

2. Primary MSP determinants:
   - Plant location
   - Plant capacity
   - Less influenced by biomass characteristics

## Usage
```python
import pandas as pd
# Load dataset
df = pd.read_excel('SAF Dataset.xlsx')
# Access processed dataset
df_processed = # processed dataframe after cleaning
```

## Dependencies
- pandas
- numpy
- matplotlib
- seaborn
- scipy

## Follow-up Analysis
Recommended clustering analysis based on:
- Plant location
- Plant capacity
- MSP distribution patterns
