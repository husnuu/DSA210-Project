# Predicting Airline Seat Occupancy in Turkey

## Motivation
Air travel demand fluctuates due to various factors, including economic conditions, seasonal trends, holidays, and unexpected events such as the COVID-19 pandemic. Understanding these patterns is essential for airlines to optimize pricing strategies, allocate resources efficiently, and enhance customer experience. This project aims to analyze historical flight occupancy rates in Turkey and develop predictive models to forecast future occupancy trends. By integrating economic indicators, fuel prices, holidays, external disruptions, and climate patterns such as temperature, the project seeks to provide valuable insights into passenger load factors and their determining factors.

## Objectives
- **Analyze Historical Flight Occupancy Trends**: Examine past flight occupancy rates in Turkey to identify patterns and fluctuations over time.
- **Assess the Impact of Economic Indicators**: Evaluate how factors such as fuel prices, inflation rates, and currency exchange fluctuations influence air travel demand and seat occupancy.
- **Evaluate the Effects of External Disruptions**: Investigate the impact of events like the COVID-19 pandemic on passenger load factors and identify any lasting effects on travel behavior.
- **Incorporate Weather Effects**: Examine how seasonal and monthly temperature variations affect passenger demand and seat occupancy.
- **Develop Predictive Models**: Create machine learning models that forecast future flight occupancy rates based on historical data and identified influencing factors.
- **Provide Strategic Insights**: Offer actionable recommendations for airlines to optimize pricing strategies, resource allocation, and customer experience based on predictive insights.

## Data Sources
The data for this project has been collected from multiple sources to ensure comprehensive analysis:
- **Turkish Airlines & DHMI Reports**: Official reports detailing monthly passenger statistics, seat capacity, and flight occupancy rates.
- **Google Flights / Skyscanner API**: Real-time data on available seats and ticket pricing trends.
- **Economic Indicators**: Data on fuel prices, inflation rates, and currency exchange fluctuations that may impact travel demand.
- **COVID-19 Impact Data**: Historical restrictions on air travel and their effect on passenger load factors.
- **Holiday & Seasonal Data**: Public holiday schedules and peak travel periods influencing occupancy rates.
- **Istanbul Temperature Data**: Monthly average temperatures from 2019 to 2024 to capture climate seasonality and its correlation with travel patterns.

## Data Analysis Steps
The project involves multiple stages of data processing and analysis:
- **Data Collection & Cleaning**: Integrating multiple data sources, handling missing values, and ensuring data consistency.
- **Exploratory Data Analysis (EDA)**: Identifying trends in flight occupancy over different time periods, visualizing demand fluctuations, and determining correlations between variables.
- **Feature Engineering**: Creating new features from raw data, including economic indices, airline-specific factors, and external influences like COVID-19 cases, fuel costs, and temperature data.
- **Hypothesis Testing**: Conducting t-tests to compare pre-COVID and COVID-era statistics for significant differences, as well as evaluating the impact of temperature on occupancy.

## Findings

### 1. Seasonality Effects
Monthly occupancy rates show clear seasonal trends, with noticeable peaks during summer months (June to August). This is consistent with the high demand for leisure travel during the holiday season.

### 2. COVID-19 Impact
A significant drop in both occupancy rates and passenger counts is observed in 2020, correlating with the onset of the COVID-19 pandemic.
- Statistical testing confirms that average occupancy rates and passenger volumes during the COVID-affected years (2020–2021) were significantly lower than in 2019 (pre-pandemic), with **p-values < 0.05**.
- Although recovery is evident by 2022, the post-pandemic trend still trails pre-2020 levels slightly, suggesting lingering behavioral changes in air travel.

### 3. Economic Influences
- **Inflation** shows a weak or slightly negative correlation with occupancy rates. Higher inflation months (e.g., mid to late 2021) align with reduced load factors.
- **Fuel prices**, surprisingly, do not appear to have a strong linear relationship with occupancy, likely because fuel costs impact airlines more directly than passengers unless passed on via ticket pricing.

### 4. Holiday and Summer Effects
- Summer holiday months consistently exhibit higher occupancy, as supported by the boxplot distribution.
- Months with more public holidays also tend to have slightly elevated passenger volumes, though this varies by year.

### 5. COVID Case Correlation
- A visible negative relationship exists between monthly COVID case counts and both occupancy rates and passenger volumes.
- As case numbers decreased into 2022–2024, both metrics recovered in parallel, reinforcing the impact of health and safety perception on travel behavior.

### 6. Temperature Effects
- Monthly **average temperature** shows a moderately positive correlation with occupancy rates and passenger counts.
- Warmer months (especially those above 20°C) align with peak travel demand periods, further validating the seasonal leisure travel pattern.
- A **statistically significant** difference was observed in occupancy rates between colder and warmer months using t-tests, confirming that climate factors influence flight demand.

## Limitations and Future Work
While this project seeks to provide meaningful insights, certain limitations must be acknowledged:
- **Data Availability**: Some airline-specific data may not be publicly accessible, requiring estimation techniques or alternative data sources.
- **External Factors**: Unexpected events (geopolitical crises, new travel restrictions) may impact airline occupancy in ways that are difficult to model.
- **Model Accuracy**: While machine learning models can make predictions, they rely on the quality and completeness of historical data.

For future improvements, additional data sources such as real-time social media sentiment analysis or customer booking behavior could enhance prediction accuracy. Including regional weather anomalies or airport-specific disruptions could further improve the robustness of the models.
