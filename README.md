**Tourism Industry Analysis — Travel Trends, Seasonal Demand, and Customer Preferences**

**INTRODUCTION**

In today's rapidly evolving world, the tourism industry plays a critical role in connecting people from different cultures and promoting economic growth. This report delves into the latest trends and insights shaping the global tourism sector, drawing insights from various sources such as industry reports, podcasts, documentaries, expert interviews, and consumer surveys. By analyzing these diverse perspectives, this report aims to provide a comprehensive view of the challenges, opportunities, and emerging trends in the tourism landscape.

**PROBLEM STATEMENT**

The Global Tourism and Travel Trends aims to analyze tourism data using Python to understand travel patterns, tourist preferences, spending behavior, and environmental impact. The dataset contains information about travel years, destinations, travel purposes, transport modes, accommodation types, visa categories, booking channels, trip duration, expenses, tourist satisfaction, and carbon footprint.
The main problem is to identify meaningful patterns and relationships within the data to understand how tourists travel, how much they spend, which factors influence their satisfaction, and how different modes of transportation affect carbon emissions. The project also aims to identify missing values, detect potential outliers, and explore relationships between numerical and categorical variables using statistical techniques and data visualizations.
By applying Exploratory Data Analysis (EDA), charts, correlation analysis, and outlier detection using Python libraries such as Pandas, NumPy, and Matplotlib, this project seeks to generate useful insights that can support better tourism planning, improve tourist experiences, and encourage more sustainable travel practices.

**Key questions addressed**

1.	How have travel patterns changed over the years?
2.	Which travel purposes, seasons, and destinations are most common?
3.	What is the relationship between trip duration, number of travellers, and total spending?
4.	Is there a relationship between transport mode and carbon footprint?
5.	How do tourists rate their travel experiences, and what factors may be associated with satisfaction?
6.	Are there missing values or potential outliers in the dataset?
7.	What insights can help improve tourism services and promote sustainable travel?

**Project Objectives**
The main objective of the Global Tourism and Travel Trends Data Analytics Project is to analyze tourism data using Python and extract meaningful insights about travel patterns, tourist behavior, spending, satisfaction, and environmental sustainability.
Specific Objectives
1. To analyze travel trends: Identify changes in the number of recorded trips across different years and seasons.
2. To identify popular travel destinations: Determine which destination countries and travel purposes are most frequently recorded in the dataset.
3. To analyze tourist spending: Study the relationship between  total trip expenditure, number of travellers, and trip duration.
4. To examine transportation patterns: Identify the most commonly used modes of transportation and compare their associated carbon footprints.
5. To evaluate tourist satisfaction: Analyze trip ratings, overall satisfaction, safety perceptions.
6. To detect outliers: Identify unusual values in numerical variables, such as total trip spending, trip duration, and carbon footprint, using statistical methods such as the Interquartile Range (IQR).
7. To handle missing data: Identify missing values and determine suitable methods for cleaning and preparing the dataset for analysis.
8. To explore relationships between variables: Use correlation analysis, cross-tabulations, and visualizations to understand relationships among tourism-related factors.
9. To create meaningful visualizations: Develop charts such as bar charts, line charts, histograms, box plots, heat maps, and scatter plots using Python libraries.
10. To promote sustainable tourism: Generate insights into transportation choices and environmental impact that may help encourage environmentally responsible travel.
11. To support data-driven decision-making: Present findings and recommendations that can help tourism businesses and planners improve services and understand tourist preferences.

**Dataset Description**

The dataset is taken from the source – Kaggle Global tourism travel trend data set, which contains information about tourist travel patterns, spending behavior, travel preferences, satisfaction levels, and environmental impact. It is analyzed using Python to identify useful trends and relationships in the tourism industry.
The dataset contains 10,000 records and 33 columns, covering the period from 2019 to 2024. Each record represents a trip and includes both numerical and categorical variables related to travel.

Category	|Important columns	|Description
| :--- | :---: | ---: |
Travel information	|trip_id, year, month, season|	Identifies trips and records when travel occurred
Destination details|	origin_country, destination_country|	Shows the traveler's origin and destination
Traveler details	|num_travelers, traveler_type	|Describes the number and type of travelers
Trip purpose|	travel_purpose	|Identifies reasons for travel, such as leisure, business, or pilgrimage
Trip duration|	duration_nights|	Number of nights spent on the trip
Transport|	transport_mode, local_transport_used	|Records the main and local modes of transportation
Accommodation|	accommodation_type	|Type of accommodation selected by the traveler
Booking details	|booking_channel, advance_booking_days	|Shows how and how early trips were booked
Visa information|	visa_type	|Records the type of visa or visa arrangement
Financial details|	budget_per_person_usd, total_trip_spend_usd, restaurant_spend_per_day_usd|	Measures travel budgets and expenditure
Tourism activities|	attractions_visited	|Records the attractions visited
Customer satisfaction	|overall_satisfaction, trip_rating, wifi_satisfaction, currency_satisfaction|	Measures the travel experience and satisfaction
Safety and convenience	|safety_perception, language_barrier, health_safety_compliance	|Describes safety perceptions and travel-related challenges
Environmental impact|	carbon_footprint_kg_co2, eco_friendly_choices|	Measures estimated carbon emissions and environmentally friendly choices
Travel preferences	|travel_insurance, repeat_visitor, would_recommend, social_media_shared|	Describes traveler choices, loyalty, and recommendations

 **LIBRARIES AND TOOLS USED**

Library / tool 	Role in this project 
Python 	Programming language used to run the analysis. 
Google Colab 	Analysis environment for running Python cells. 
Google Drive 	Used to mount Drive and load the CSV file. 
Pandas (pd) 	Loads CSV data and performs data cleaning, grouping, counting and tabular summaries. 
NumPy (np) 	Imported for numerical and array-related operations; the analysis's main analysis primarily uses Pandas. 
Matplotlib (plt) 	Creates bar, line, histogram and pie visualisations. 
Seaborn (sns) 	Creates statistical visualisations such as box plots, scatter plots and correlation heatmaps. 
Plotly Express (px) 	Creates interactive department-wise bar, doctor experience scatter and satisfaction violin plots. 

**DATA CLEANING AND PREPROCESSING**
Data cleaning prepares records for analysis by addressing missing values, duplicate rows, inconsistent labels,unsuitable data types and implausible values. The analysis carries out the following steps.
Missing Values

Column(s)| 	Missing-value treatment |
|--------|------------|
language_barrier|	Filled with mode 
health_safety_compliance|	Filled with  mode 
social_media_shared|	Filled with mode

The analysis fills these fields using the rules above and rechecks missing-value counts. 

Duplicate Records and inconsistencies

The duplicate values are checked in the analysis.The analysis shows zero duplicates and no inconsistencies. Number of travelers ,year and trip rating was checked for invalid data. The analysis shows no results for invalid data.

**OUTLIER ANALYSIS** 
An outlier is a value that lies unusually far from the main distribution. The analysis explains the Interquartile Range (IQR) method and checks the total_trip_spend_usd column. 
 
IQR Method 
Q1 is the 25th percentile and Q3 is the 75th percentile. The interquartile range is IQR = Q3 − Q1. The conventional lower and upper fences are Q1 − 1.5 × IQR and Q3 + 1.5 × IQR. Values beyond these fences are flagged as potential outliers.

Column |	Q1 |	Q3 |	IQR 	|Upper IQR fence |	Values flagged in analysis|
|------|-------|--------|--------|------------|--------|
Tota_trip_spend_column|	1559.5725|	9998.3575|	8438.785|	22656.535|	1216 records 
 
 neglecting the outliers as the total money spend may reflect genuine travel pattern.

**Exploratory Data Analysis (EDA)**
 
Exploratory Data Analysis (EDA) is used to summarise the dataset, understand category frequencies and examine relationships before drawing conclusions. The analysis includes numerical summaries, categorical counts, distribution analysis, percentage analysis and correlation analysis.

Numerical Summary

Numerical variable|	Mean|	Median|	Minimum|	maximum
|-------|------|-----|-----|-------|
Trip duration (nights)|	17.47|	11|	2|	179
Total trip spending (USD)	|11,549.69|	3,721.87|	150.00|	612141.57
Budget per person (USD)|	2,558.94|	1,732.73|	150.00|	40962.530
Trip rating	|3.94 |	4	|1|	5
Carbon footprint (kg CO₂)|	1,671.85|	593.10|	6.1|	25612.9
Number of travelers	|4.5|	2|	1|	29

 Group by average analysis
 
Analysis| 	Analysis result |	Interpretation| 
|----------|----------------|----------------|
Average trip spending by travel purpose|Highest:business:13981 usd,lowest: digital nomad:8463 usd|Business travel has highest expense compared to other categories. 
Average Carbon Footprint by Transport|Highest: Air    :        2282.05,Lowest:Rail: 149.99	|Air transport has the highest carbon emission.
Average trip rating by Destination country|Highest: New Zealand :4,Lowest: Spain:3.89|Highest rating for new Zealand. 
Average trip duration by season|Highest:Winter:17.75 days,Lowest summer :16.9 days|	Highest trip duration in winter.

7.3.Categorical Analysis 
Categorical analysis counts records in fields such as season, origin country,destination country, travel purpose, traveler type, transport mode, accommodation type , visa type ,booking agent, travel insurance, overall satisfaction. The analysis uses value_counts() to show the frequency of categories and mode() to identify the most frequent category. 

INTERPRETATION

•	Summer has the highest number of trips compared to other season.
•	France is the most visted country. Canada is the most origin country.
•	Air is the most used mode of transport and taxi/Ride share is the local transport used.
•	Most of them are repeat visitors.
•	3 star accommodation is mostly used.
•	Online travel agency is used for booking and visa free travellers are more.
•	Most of them have travel insurance.
•	Most of them does not opt for eco friendly choices.

**Visualisation & Interpretation** 

Line chart-yearly  number of travelers.

bar chart showing season with more travelers.

Bar chart showing number of trips by travel purpose

Bar chart showing top 10 tourist destination.

Pie chart showing most used transport mode

scatter plot showing relation between trip spending and carbon footprint

Scatter plot showing relation between number of travelers and carbon footprint

Bar chart finding which transport mode has more carbon emission

Histogram showing distribution of trip days.

Bar chart showing number of trips by visa type and trip rating.

Bar chart showing number of trips by booking channel and trip rating.

pie chart showing safety perception

Heat map showing relation between numeric variables.

pie chart showing overall satisfaction.

**KEY FINDINGS AND INSIGHTS**

1.The data set contains 10000 rows and 33 columns.missing values were found in 3 categorical columns and was filled with mode value.

2.There was no duplicate records and inconsistent values.

3.Outliers was detected in some numerical columns.But neglecting outliers as they may be genuine travel patterns.

4.2023 has the most number of travelers after the corona impact.

5.Leisure or tourism is the most frequent travel purpose(3251 records)

6.France is the most visited country whereas New Zealand has the highest average trip rating.

7.Air is the most common mode of transport and taxi/ride share is mainly used for local transport.

8.Air transport accounts for most of the carbon emissions and number of travelers also contribute for carbon footprint.

9.Summer season is the mostly travelled season but winter season has large trip duration.

10.Average total spend in the trip is higher than the median indicating high spending pattern.

11.Most of the travelers are satisfied with the trip and trip rating has an average of 3.9.

**CONCLUSION**
This analysis demonstrates how Python can be used to inspect, summarize, visualize, and investigate tourism data. The most useful next steps are to validate data quality, examine spending and carbon outliers, compare travel modes using grouped statistics, and analyze how travel purpose, booking channel, visa type, and satisfaction relate to travel patterns. Findings should be interpreted as patterns in this dataset rather than universal statements about global tourism.




