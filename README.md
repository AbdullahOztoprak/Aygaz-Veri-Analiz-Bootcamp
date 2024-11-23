House Price Prediction - Real Estate Data Analysis and Preprocessing
Project Overview
Project by: Abdullah Öztoprak and Elif Beyza Öztoprak

This project focuses on analyzing a house price prediction dataset from Kaggle, where the goal is to clean, explore, and prepare the data for predictive modeling. The project includes various steps like data loading, handling missing values, exploratory data analysis (EDA), feature engineering, and model evaluation. The primary aim is to predict house prices based on multiple features such as location, property type, and size.

Link to Kaggle

Dataset Overview
The dataset contains real estate property data, including location, price, property type, and other related attributes. It has a total of 168,446 rows and 20 columns.

Dataset Columns
Column Name	Description
property_id	Unique identifier for each property
location_id	Location identifier
page_url	URL of the property listing
property_type	Type of property (e.g., Flat, House)
price	Price of the property
location	Location of the property within the city
city	City where the property is located
province_name	Province name
latitude	Latitude coordinates of the property
longitude	Longitude coordinates of the property
baths	Number of bathrooms
area	Area size in Marla/Kanal
purpose	Purpose of the listing (e.g., For Sale)
bedrooms	Number of bedrooms
date_added	Date when the property was listed
agency	Real estate agency name
agent	Real estate agent name
Area Type	Type of area (e.g., Marla, Kanal)
Area Size	Area size in numerical form
Area Category	Area category based on size (e.g., 0-5 Marla)


Project Workflow


1. Loading the Dataset
The first step of the project is to load the dataset into the Python environment.

Dataset Source: The dataset is retrieved from Kaggle and loaded using pandas.
Initial Review: After loading the data, the structure of the dataset is assessed by displaying the first few rows. This helps in understanding the columns and the type of data each column contains.
Data Types Inspection: Ensure that the data types of the columns are appropriate for analysis (for example, numerical data types for numerical features and categorical data types for non-numerical features).
By performing this step, you gain insight into the dataset’s basic structure, which helps in deciding the next steps for data cleaning and preprocessing.




2. Small Data Analysis
General Analysis:
View the first few rows using head().
Calculate basic statistics with describe() and check data types using info().
Missing Data Analysis:
Identify the columns with missing values and calculate their percentage.
Visualization:
Use histograms and box plots for distribution analysis of numeric variables (e.g., price, area).
Use a heatmap for correlation analysis to examine relationships between numeric variables.
Plot the geographical locations of properties using latitude and longitude.
Categorical Data Analysis:
Analyze the frequency distribution of categorical variables such as property_type, city, and purpose.



3. Handling Missing Data
Handling missing values is an essential part of data preprocessing. Missing data is identified in several columns, and gaps are filled using different techniques tailored to the type of data.

Numerical Columns:
Missing values in numerical columns (such as price, area, etc.) are filled with the median of the column.
The median is preferred over the mean because it is less sensitive to outliers, ensuring that the imputed values are more robust and reflective of the overall distribution of data. For example, missing values in the area column are replaced by the median value of area.
Categorical Columns:
For categorical columns (such as property_type, city, etc.), missing values are filled by the mode (the most frequent value) of each respective column.
In certain cases where forward filling is appropriate, missing values are replaced with the previous row's value (i.e., the most recent valid value). This is especially useful in time-series or ordered data.
By applying these strategies, the dataset is made complete without losing significant information due to missing values.


4. Exploratory Data Analysis (EDA)
Exploratory Data Analysis (EDA) allows for a deeper understanding of the dataset, uncovering key patterns, correlations, and potential issues that may impact the model.

Data Visualization:
Various plots, including box plots, histograms, and scatter plots, are created to visually explore the distribution of numerical features (such as price and area).
Box plots help in identifying outliers, while histograms provide insights into the distribution of individual features. Scatter plots are used to explore the relationships between pairs of variables, such as the relationship between area and price.
Statistical Summary:
Descriptive statistics such as mean, median, standard deviation, and correlation coefficients are computed to understand the spread and correlation of numerical features.
The correlation matrix helps identify which features are highly correlated with the target variable (price), aiding in feature selection for future modeling.
Through EDA, key insights were gained into the dataset’s structure and important patterns and correlations were identified.




5. Saving the Processed Dataset
After cleaning and preprocessing, the final dataset is saved as cleaned_dataset.csv for future analysis or modeling.
Setup Instructions
Clone or Download this repository to your local system.

Conclusion
This project demonstrates the essential steps involved in preparing a dataset for predictive modeling. From handling missing data and exploring the dataset to applying data preprocessing techniques, the groundwork has been laid to predict house prices. Although the actual modeling isn't implemented in this project, it sets the stage for training predictive models using machine learning algorithms like Linear Regression, Decision Trees, or Random Forests.

The processed dataset is now ready for further analysis, where machine learning models can be applied to predict house prices accurately.
