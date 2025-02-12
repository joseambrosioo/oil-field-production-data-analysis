# Oil Field Production Data Analysis

## Project Overview
This project focuses on performing Exploratory Data Analysis (EDA) on publicly available well-production data from the Volve Field. The goal is to analyze the production data of producer wells to gain insights into their performance, identify significant producers, and detect wells that may be nearing depletion. The analysis will help the petroleum management team make informed decisions regarding well optimization and resource allocation.

## Key Takeaways
- **Data Source**: Publicly available Volve Field production data from Equinor.
- **Objective**: Analyze producer wells to identify high-performing wells and those at risk of becoming dry.
- **Insights**: Identified significant producers and wells with declining performance.
- **Visualizations**: Utilized heatmaps, ECDF plots, scatter plots, and line plots for data exploration.
- **Recommendations**: Provided actionable insights for well management and optimization.

## Applications
This analysis has several practical applications in the oil and gas industry:
- **Well Optimization**: Identify wells that require intervention to maintain or enhance production.
- **Resource Allocation**: Allocate resources efficiently to high-performing wells.
- **Production Forecasting**: Predict future production trends based on historical data.
- **Economic Viability**: Assess the economic viability of wells based on production and water cut ratios.

## Methodology
The project followed a structured data analysis pipeline to ensure comprehensive and accurate results:

### 1. **Ask Phase**
- **Business Task**: Analyze the production data of producer wells in the Volve Field to identify significant producers and wells at risk of depletion.
- **Key Stakeholders**: Production Manager, Sales & Marketing Team.
- **Deliverables**: A detailed report with data sources, cleaning processes, analysis summary, visualizations, and recommendations.

### 2. **Prepare Phase**
- **Data Source**: Publicly available Volve Field production data from Equinor.
- **Data Format**: Excel file containing production data for 7 wells (producers and injectors).
- **Data Overview**: The dataset includes 15,634 entries with 24 columns, including date, well codes, production volumes, and operational parameters.

### 3. **Process Phase**
- **Data Cleaning**: Removed irrelevant columns and filtered data to focus on producer wells.
- **Data Imputation**: Addressed missing values and outliers.
- **Feature Engineering**: Created meaningful features for analysis, such as cumulative production and water cut ratios.

### 4. **Analyze Phase**
- **Exploratory Data Analysis (EDA)**: Conducted EDA to uncover patterns, trends, and outliers using visualizations and statistical methods.
- **Key Visualizations**:
  - **Heatmap**: Identified missing data and correlations between variables.
  - **ECDF Plot**: Analyzed cumulative production distribution across wells.
  - **Scatter Plot**: Visualized oil production trends over time.
  - **Line Plot**: Tracked oil, gas, and water production trends.

### 5. **Share Phase**
- **Summary of Findings**:
  - Identified significant producers (Wells #5599 and #5351).
  - Detected wells with declining production and high water cut ratios (Wells #7405, #7289, and #5769).
  - Observed intermittent shut-in periods in production data.
- **Recommendations**:
  - Focus on optimizing high-performing wells.
  - Consider shutting down or re-evaluating wells with declining production and high water cuts.
  - Monitor production trends and water cut ratios to assess economic viability.

### 6. **Act Phase**
- **Recommendations**:
  - **Well Optimization**: Implement strategies to enhance production from high-performing wells.
  - **Resource Allocation**: Allocate resources to wells with the highest production potential.
  - **Economic Viability**: Regularly assess the economic viability of wells based on production and water cut trends.

## Code Snippets
Below are key sections of the code used in this project:

### Data Loading and Initial Exploration
```python
import pandas as pd
from matplotlib import pyplot as plt
import seaborn as sns
import plotly.express as px

# Load data
df_production = pd.read_excel('../input/volve-well-production/Volve production data.xlsx')

# Initial data exploration
df_production.info()
df_production.head()
