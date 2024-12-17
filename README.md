# Light Brightness Index and Suicide Rate Analysis
The final project which made by Darren, Cassie, Joya

# Project Overview
This project aims to explore the relationship between light pollution, mental health indicators (e.g., PTSD, depression, trauma rates), and suicide rates across counties. We conducted data analysis, classification tasks, and predictive modeling to identify patterns and key influencing variables.

# Data Sources
The project utilized the following datasets:
1. Light Pollution Data: Brightness measurements with latitude and longitude (2018~2022).
2. County Geographical Data: Latitude and longitude coordinates for counties.
3. Mental health and Suicide Data: 
(1). Suicide Data (age-adjusted death per 100k)
(2). PTSD rate, trauma rate, and depression rate per 100k
4. Other data:
(1). Tree cover loss
(2). Real_GDP

File names:
1. light_pollution_(2018~2022).csv
2. GEOINFO2023.GEOINFO-Data.csv
3. Mental health data files
4. HDPulse_data_filtered.csv
5. Other data(csv)

# Project Workflow
1. Data Preprocessing
Cleaned all datasets by:
Handling missing values and ensuring correct data types.
Dropping invalid rows (e.g., non-numeric coordinates).

Merged light pollution data with county-level information:
Calculated distances between light pollution points and county centers using the geopy library.
Assigned each light pollution measurement to its nearest county.

Ouput: county_light_pollution_(2018~2022).csv  Aggregated light pollution data by county.

2. Merge dataset file
Handling missing values and ensuring correct data types.
Dropping invalid rows
Then get a clean data file for regression later: merge_data_final
This including:
Index: County_Name
Indepent variable: Suicide rate(Age-adjusted Death Rate)
Dependent Varibale:
(1). Brightness
(2). Real_GDP
(3). depression rate
(4). PTSD rate
(5). Trauma rate
(6). tree_cover_loss

3. Exploratory Data Analysis (EDA)
Examined the statistical relationships between:
Brightness, mental health indicators, and suicide rates.

Visualization included:
Scatter plots with regression lines.
Histograms and box plots of key variables.

4. Classification task
We performed a classification task to categorize counties into:
High Suicide Rate and Low Suicide Rate based on the median suicide rate.

Steps:
Split data into training and testing sets (70/30 split).

Applied machine learning models:
Logistic Regression
Support Vector Machine (SVM)
Random Forest Classifier
K-Nearest Neighbors (KNN)

Evaluated models using:
Accuracy, Precision, Recall, F1-Score
Confusion Matrix with heatmaps

Results:
Logistic Regression achieved the best performance.
Key influencing variables were identified using feature importance analysis.

# Requirements
install the following Python libraries:
pip install pandas numpy scikit-learn geopy matplotlib seaborn

# How to Run the project
1. Clone the repository:
git clone <https://github.com/Darren-Deng-GU/FInal-Project-Brightness-Suicide>

2. Place the datasets in the appropriate

3. Run the Jupyter Notebook files:
Data processing: plus_independent_variable.ipynb
Regression: regression analyze.ipynb
Classification: 2_Machine_Learning_Classification.ipynb
