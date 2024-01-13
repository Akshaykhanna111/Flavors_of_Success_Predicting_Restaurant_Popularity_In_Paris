## Project/Goals
Project Title: Falvors of Success (Predicting the Restaurant Popularity in Paris using Open Data like Yelp, Google Maps and Bike Station density etc.)

Project Summary:
The project focuses on leveraging open data to build a model that will help predict the restaurant popularity in Paris basis features like location of restaurant, competitors in vicinity, POI density within 1km, cuisine type etc.

## Process
### Step 1
Data Collection:
1. Yelp API - We fetched the data of 2500 restaurants in Paris using latitude and longitude.
2. Google Maps Places - For the mentioned latitude and longitude, we got details from google places api regarding the street popularity, reviews, different types of POIs within 1km
3. City Bike API - This api was leveraged to churn the data of bike stations within the 1 km vicinity of the restaurants 
    
### Step 2
Data Cleaning:

  Objective: Address and rectify any inconsistencies, missing values, or anomalies in the dataset.
  
  Activities:  
    *Remove duplicates and drop redundant columns <br>
    *Change data types (if required) <br>
    *Treat outliers and missing values <br>
    *Feature engineering - Create new features for better modeling <br>
    *Modify column names <br>
    *Aggregate data to update the data granularity for merging all the datasets <br>

### Step 3 
Framework Development:
  
  Objective: Establish a structured framework for conducting the analysis based on identified dimensions and measures.
  
  Activities:<br>
    *Defining dimensions and measures of interest.<br>
    *Structuring the analysis framework for comprehensive insights extraction.<br>
    *Following were the analysis aspects created - Geographical Analysis and Host Rating Analysis<br>

### Step 4
Geographical Analysis:
  
  Objective: Analyze and visualize data patterns across different geographies.
  
  Sub-Objectives and Activities:<br>
    *Platform Registration Rate Analysis:<br>
      -Yearly and monthly registration trends visualization.<br>
      -Geographical distribution of registration rates.<br>
    *Impact of External Events:<br>
      -Assessing and visualizing the influence of external events on registration rates.<br>
    *Pricing and BNB Type Preferences:<br>
      -Analyzing pricing trends across geographies.<br>
      -Preference analysis for different BNB types.<br>
    *Forecasting:<br>
      Developing forecasting models for platform registration and pricing trends across geographies.<br>

### Step 5
Host Rating Analysis:

Objective: Investigate host ratings and their correlations with various factors.

Sub-Objectives and Activities:<br>
  *Correlation Analysis:<br>
    -Assessing correlations between host ratings and pricing.<br>
  *Profitability Analysis:<br>
    -Identifying and clustering hosts based on profitability metrics like review count and pricing.<br>
  *Dashboard Creation:<br>
    -Designing interactive dashboards showcasing top hosts across geographies and room categories.<br>

### Step 6 
Documentation and Reporting:

Objective: Document the analysis methodologies, findings, and insights for clear communication and reference in the form of presentation and dashboard.

Activities:<br>
  *Compiling analysis results.<br>
  *Creating detailed documentation and reports highlighting key insights and recommendations.<br>

## Results
For this project Option 2 was selected and within this option, the NY Airbnb dataset was picked for analysis. Results and analysis of this activity are listed below - 
1. Registration trend analysis - For certain geographies like Manhattan and Brooklyn, there has been a significant growth in the registration trend on the platform from 2008 to 2015.
2. Pricing Trend Analysis - Median pricing across geographies has been dropping, though the magnitude of drop is not very high.
3. Forecasting the registration and pricing trends -
   * Registration will be increasing for private rooms whereas for homes it will be dropping in next 6 quarters.
   * Pricing will not vary much and continue to be +-3/4 around the last quarter's median value
4. Registration and Pricing seasonality within a year -
   * Registration spikes during summers whereas pricing doesn't vary much throughout the year
5. Pricing variance by zipcodes
   * Only one zipcode had anomalous median pricing in Staten Islands of 850 rest all were within 150 limit
6. Correlation heatmap between pricing and ratings -
   * Customers in Staten Islands are a bit price sensitive, meaning high prices can negatively impact the rating whereas for other neighborhoods no such pattern was observed
7. K-means clustering -
   * Using clustering analysis in Tableau hosts were clustered into 4 clusters. Hosts within cluster 2 and 3 were found to be most profitable with high ratings and high pricing (leading to higher commissions for Airbnb)
8. Top N hosts dynamic report was created (user can input the ranks through parameter filters)
9. YOY rating growth chart was created - There was a consistent drop (minor) in ratings between 2012 to 2014, which was addressed from 2015 onwards.
10. Dynamic BNB stats report was created to visualize various measures across geographies and room types.
11. Finally a dashboard was created for the user to study all the above insights in a single view

## Challenges 
1. Data Recency was till 2015 only 
2. Geography was limited to NY
3. For 30% records no ratings were available

## Future Goals
1. Accumulate more data for analysis
2. Study patterns across geographies as seasonality, user preferences, macro-economic factors will vary across regions
3. Take into account the macro-economic factors like inflation, flight prices, weather etc. 
