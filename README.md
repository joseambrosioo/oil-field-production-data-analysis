# Oil Field Production Data Analysis

## Project Overview
This project focuses on performing **Exploratory Data Analysis (EDA)** on publicly available well-production data from the **Volve Field**. The dataset includes data from **7 wells** (both producer and injector wells). The analysis aims to provide insights into the production performance of the wells, identify significant producers, and detect wells that may be nearing depletion.

## Applications
This analysis has several practical applications in the oil and gas industry:
- **Well Optimization**: Identify wells that require intervention to maintain or enhance production.
- **Resource Allocation**: Allocate resources efficiently to high-performing wells.
- **Production Forecasting**: Predict future production trends based on historical data.
- **Economic Viability**: Assess the economic viability of wells based on production and water cut ratios.

## Methodology
The project followed a structured data analysis pipeline to ensure comprehensive and accurate results:

## 1. Ask Phase

### Business Task
The primary goal is to analyze the production data of **producer wells** in the Volve Field to:
- Identify wells with significant production.
- Detect wells that may be on the path to becoming dry.
- Provide actionable insights to the petroleum management team.

### Key Stakeholders
- **Primary Stakeholder**: Production Manager
- **Other Stakeholders**: Sales and Marketing Team

### Deliverables
- A comprehensive report summarizing the analysis.
- Supporting visualizations and key findings.
- Recommendations based on the analysis.

## 2. Prepare Phase

### Data Source
The dataset used is publicly available and can be accessed from [Equinor's Volve Field Data Village](https://www.equinor.com/en/what-we-do/digitalisation-in-our-dna/volve-field-data-village-download.html). The data is provided under an open license by Equinor.

### Data Overview
The dataset contains **24 columns** with information such as:
- **DATEPRD**: Date of production.
- **NPD_WELL_BORE_CODE**: Unique identifier for each well.
- **BORE_OIL_VOL**: Volume of oil produced.
- **BORE_GAS_VOL**: Volume of gas produced.
- **BORE_WAT_VOL**: Volume of water produced.
- **WELL_TYPE**: Type of well (Producer or Injector).

![image](https://github.com/user-attachments/assets/6fba66fd-861d-4b1f-9751-bfc54263c889)

*Figure 1. Heatmap diagram of all the fields in dataframe (The yellow color represents the null values)*

## 3. Process Phase
In this phase we perform data cleaning by imputation, There are many columns that are not useful to our Analysis and we can simply drop them.

### Data Cleaning
- **Filtering**: Only data from producer wells (WELL_TYPE = 'OP') was retained for analysis.
- **Dropping Irrelevant Columns**: Columns such as `WELL_BORE_CODE`, `NPD_WELL_BORE_NAME`, and others were dropped as they were not relevant to the analysis.
- **Handling Missing Data**: Missing values were identified and addressed through imputation or exclusion, depending on the context.

### Data Transformation
- The `NPD_WELL_BORE_CODE` column was converted to a string type for easier visualization and analysis.

## 4. Analyze Phase
![image](https://github.com/user-attachments/assets/e20ee59f-9d95-4ad1-98e6-d3bf12b7cfa2)
* After droping unuseful columns, we can again plot a heatmap plot to visualize null data in our dataframe. As can be seen in the above heatmap, the column BORE_WI_VOL is yellow signifying null value, this is because we have taken only the producing wells, so there is no water injection from producing wells.*

### Key Insights
- **Well Performance**: The wells with codes **5599** and **5351** were identified as the most significant producers.
- **Declining Production**: A declining trend in oil production was observed across all wells, with some wells showing intermittent zero production, indicating periodic shut-ins.
- **Water Production**: Wells **7405**, **7289**, and **5769** showed higher water production relative to oil, making them less economically viable.

### Visualizations
- **ECDF Plot**: Used to visualize the cumulative distribution of oil production across wells.
- **Scatter Plot**: Showed the oil production trends over time for each well.
- **Line Plot**: Highlighted the declining production trends and water production volumes.
- **Heatmap**: Used to identify correlations between different production variables.

## Key Takeaways

1. **Significant Producers Identified**:
   - Wells **5599** and **5351** are the most productive, contributing the majority of oil and gas production in the Volve Field.

2. **Declining Production Trends**:
   - A consistent decline in oil production was observed across all wells, with some wells showing intermittent zero production due to periodic shut-ins.

3. **Water Production Insights**:
   - Wells **7405**, **7289**, and **5769** are producing more water than oil, indicating they may no longer be economically viable and could be nearing the end of their productive life.

4. **Correlation Between Oil and Gas Production**:
   - A strong positive correlation was found between oil and gas production, suggesting that wells with higher oil production also tend to have higher gas production.

5. **Data-Driven Recommendations**:
   - Focus resources on maximizing production from high-performing wells (**5599** and **5351**).
   - Consider shutting down or reassessing the economic viability of wells with high water production (**7405**, **7289**, and **5769**).
   - Investigate the causes of declining production and explore potential interventions to enhance recovery.

6. **Visualizations for Clarity**:
   - Visual tools like ECDF plots, scatter plots, line plots, and heatmaps were used to effectively communicate trends and insights.

7. **Actionable Insights**:
   - The analysis provides actionable insights for the production and management teams to optimize well performance and make informed decisions.

## Conclusion

The exploratory data analysis of the Volve Field production data has provided valuable insights into the performance of the producer wells. By identifying the most productive wells (**5599** and **5351**) and highlighting the declining performance of others (**7405**, **7289**, and **5769**), this analysis offers a clear roadmap for optimizing production and resource allocation. The findings emphasize the importance of integrating domain knowledge with data analysis to draw accurate conclusions, particularly in understanding the economic viability of wells with high water production.

The visualizations and statistical analysis have effectively communicated the trends and correlations within the dataset, enabling stakeholders to make data-driven decisions. This project underscores the power of data analysis in the oil and gas industry to improve operational efficiency and profitability.

## Future Improvements

1. **Predictive Modeling**:
   - Develop machine learning models to predict future production trends and identify wells at risk of declining performance.
   - Use time-series forecasting techniques to estimate future oil, gas, and water production.

2. **Real-Time Monitoring Dashboard**:
   - Create a dashboard for real-time monitoring of well performance, enabling proactive decision-making and early detection of issues.

3. **Advanced Data Integration**:
   - Integrate additional datasets, such as geological data, reservoir pressure data, and maintenance records, to gain a more comprehensive understanding of well performance.

4. **Economic Analysis**:
   - Conduct a detailed economic analysis to determine the profitability of each well, considering factors such as production costs, oil prices, and water disposal costs.

5. **Automated Reporting**:
   - Implement automated reporting tools to generate regular updates on well performance and share insights with stakeholders.

6. **Enhanced Visualization Tools**:
   - Explore advanced visualization tools and techniques, such as 3D plots and interactive dashboards, to provide more intuitive insights.

7. **Domain-Specific Analysis**:
   - Collaborate with petroleum engineers to incorporate domain-specific knowledge into the analysis, ensuring more accurate and actionable insights.

8. **Scalability**:
   - Scale the analysis to include data from multiple fields or regions, enabling comparative analysis and benchmarking.

## Recommendations

Based on the analysis of the Volve Field production data, the following recommendations are proposed to optimize production and improve decision-making:

1. **Focus on High-Performing Wells**:
   - Allocate additional resources to maximize production from the most productive wells (**5599** and **5351**).
   - Implement enhanced recovery techniques, such as water flooding or gas injection, to sustain production levels.

2. **Reassess Low-Performing Wells**:
   - Conduct a detailed economic evaluation of wells **7405**, **7289**, and **5769** to determine their viability.
   - Consider shutting down or converting these wells to injector wells if they are no longer economically viable.

3. **Monitor Water Production**:
   - Closely monitor water production trends in all wells to identify early signs of increasing water cut.
   - Implement water management strategies to mitigate the impact of high water production on overall profitability.

4. **Investigate Declining Production**:
   - Investigate the root causes of declining production in all wells, including reservoir pressure depletion, mechanical issues, or operational inefficiencies.
   - Explore interventions such as well stimulation, workovers, or infill drilling to enhance production.

5. **Leverage Data for Predictive Insights**:
   - Develop predictive models to forecast future production trends and identify wells at risk of underperformance.
   - Use these insights to proactively address potential issues and optimize production schedules.

6. **Enhance Data Collection and Integration**:
   - Integrate additional data sources, such as geological surveys, reservoir simulations, and maintenance records, to gain a more comprehensive understanding of well performance.
   - Ensure data quality and consistency to improve the accuracy of analysis and decision-making.

7. **Implement Real-Time Monitoring**:
   - Deploy a real-time monitoring system to track key performance indicators (KPIs) such as oil, gas, and water production rates.
   - Use dashboards and alerts to enable quick response to operational issues and optimize production in real time.

8. **Optimize Shut-In Strategies**:
   - Analyze shut-in patterns to determine their impact on production and reservoir performance.
   - Optimize shut-in schedules to minimize production losses and maximize recovery.

9. **Collaborate with Domain Experts**:
   - Work closely with petroleum engineers and reservoir specialists to validate findings and incorporate domain-specific knowledge into the analysis.
   - Use their expertise to design and implement effective recovery strategies.

10. **Continuous Improvement**:
    - Regularly review and update the analysis to incorporate new data and insights.
    - Foster a culture of continuous improvement by encouraging feedback and collaboration among stakeholders.

By implementing these recommendations, the production team can optimize well performance, extend the economic life of the field, and maximize profitability. These actions will also support more informed decision-making and strategic planning in the Volve Field.

## Tools and Libraries Used
- **Python**: Primary programming language for analysis.
- **Pandas**: Data manipulation and analysis.
- **Matplotlib & Seaborn**: Data visualization.
- **Plotly**: Interactive visualizations.
- **Openpyxl**: Handling Excel files.

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
