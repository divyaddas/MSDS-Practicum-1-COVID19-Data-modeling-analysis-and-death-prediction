# MSDS-Practicum-1-COVID19-Data-modeling-analysis-and-death-prediction
                                        Project Summary (README.MD)

                                            MSDS Practicum Project: 1 –Regis University
             Project Title: COVID – 19 Data modeling, analysis and death prediction.

We are living in an era where we’re continuously generating the different forms of data throughout the day after the introduction of computers. The technology advancement and adoption of IOT will be making exponential data growth across different business domains. Over the last two years alone 90 percent of the data in the world was generated. As big data expands into AI and machine learning, its scope is very vast and, for any business data analysis is very important because it helps in decision making as well as provides explanation to important concepts and problems. Also we can find solution of various difficult real life problems. Scientists around the world develop algorithms that can help to predict infections based on that data. 
Project Summary:
 	The world is going through a difficult time and fighting with a deadly virus called COVID-19. Coronavirus disease 2019 (COVID-19) is an infectious disease caused by severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2). It was first identified in December 2019 in Wuhan, China, and has resulted in an ongoing pandemic. The first case may be traced back to 17 November 2019.As of 8 June 2020, more than 7.06 million cases have been reported across 188 countries and territories, resulting in more than 403,000 deaths. More than 3.16 million people have recovered. (Wikipedia)
As a data scientist it’s our duty is to do good for our society, and I believe we can get through it. The objective of the project is to use the COVID-19 data from CSSE at Johns Hopkins University and Our World in Data. Explored and analyzed the data using python, created visualizations. Also build Prophet, SIR, Extended SIR, linear regression and XGBoost model for death prediction.
Data and variables:
For the analysis and Machine Learning I have used the time series data from CSSE at Johns Hopkins University and Our World in Data. The variables represent all of the main data related to confirmed cases, deaths, and testing, as well as other variables.
The main independent variables that I’m focusing for this analysis are: total_cases, new_cases, total_deaths, new_deaths, aged_65_older, aged_70_older, gdp_per_capita, diabetes_prevalence, female_smokers, male_smokers, handwashing_facilities, hospital_beds_per_thousand
Data Cleaning Methods:
	Data preprocessing is the crucial step while creating a machine learning model, and while doing any operation with data, it is mandatory to clean it and put in a formatted way. First of all I have identified the columns that are required for my analysis and selected those columns to clean and further analysis.
•	Handling null or empty data is important since most of the model doesn’t work well with null data. I have use panda function to handle empty string using fillna(‘’) and null values in float/int columns.
•	Formatting data  is important avoid errors and improve the readability. Date fields are one of the most common fields which need formatting to ensure it works properly. Also sometime you get float or int as object so need to cast it correct data type. Similarly we need to rename columns to improve the readability.
•	Aggregation of data one of the common step need to be performed in order to get the summary of data. In our case we need summarize the data by date and country. Also some of the field we need to take mean of the values
•	Concatenation and appending required when we work with multiple sources, in this project I have used data from john Hopkins and oneworldin.org so I had to perform the similar operation to prepare the data.  
•	One of the challenge I want to call out here is to work with date for a linear regression model. In this project I have solved the challenge by converting to a index. AS you can see here to_datetime will convert date string to datetime data type and set_index in pandas library will set it as index.

Analysis Methods/ Visualizations:
For the EDA and Visualization I have used the time series data from CSSE at Johns Hopkins University and Our World in Data. Based on the research, I decided to use packages like Plotly and folium for better visualization, also it needed jupyter extensions to display the graph. I have created couple of plots and maps, created bar plot to display top 10 countries with highest number of death rates and bottom 10 countries with lowest death rate, created sub bar plots for displaying Top 10 Countries with Confirmed Cases, Top 10 Countries with Death Cases, Top 10 Countries with Recovered Cases, and Top 10 Countries with Active Cases. Also created a bar chart for comparing confirmed, death and recovered cases. Created correlation heat map to find out the highly correlated variables.
Created Scatter geo map for displaying the trend over the time and created TrendLine chart to display World Death and new cases over the time using plotly. Created comparison chart showing Top 10 Countries with Death Cases VS Bottom 10 including variables like gdp_per_capita , diabetes_prevalence ,female_smokers, male_smokers, hospital_beds_per_100k, cvd_death_rate.
*visualizations of the analysis are included in the attached document.

Machine Learning Models:
Created a Linear regression model and fit the model with owid COVID19 data, predicted the world death projection for the next 30 days. In this project I have used sklearn for creating Linear Regression model and created training split with 80 to 20%. The trained the model and predicted the death for next 30 days. Also created model using XGBoost for improving the linear regression model and fit the model with owid COVID19 data, predicted the world death projection for the next 30 days. Created a model and predicted US death projection using the prophet model. Using prophet I have predicted the death for future with date, It also shows a upper and lower limit of y value, The blue line shows the prediction along with its lower and upper bound of the uncertainty interval. Prophet simple and great for predicting different forecast with time series data like covid19 data. Created SIR model, SIR model is one of the simplest compartment model consist of three compartments S for the number of susceptible, I for the number of infectious, and R for the number of recovered or deceased. Created the extended SIR model (SIR Extended Model: This model extended SIR with Exposed, Hospitalized and Dead Compartments).
Results/Conclusions:
In this project I have used data from multiple sources and  used them to perform EDA and created visualizations. I have created Five Different Machine Learning Models for COVID-19. Then Predicted the death for the world and US. Also Fitted the model with real time data from Ourdworldin.org and john Hopkins. I believe every effort count in this kind of pandemic and we all can get through it.
References:
https://github.com/CSSEGISandData
 https://ourworldindata.org/coronavirus (https://github.com/owid/covid-19-data/tree/master/public/data)
https://facebook.github.io/prophet/
(https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology





	

