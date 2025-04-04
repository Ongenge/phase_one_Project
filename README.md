# Project Data Analysis For Aviation Investment
A data-driven exploration of aircraft accident data from 1962 to 2023, using Python and Tableau to assess risk factors, trends, and safety insights. This project involves data cleaning, exploratory analysis, and interactive visualization to uncover patterns in aviation safety.

## Data Loading
### Importing the Dataset for Analysis 

The first step in any data analysis process is loading the dataset into the environment. 
This allows us to inspect, clean, and prepare the data for further exploration.  

### 1. Importing Necessary Libraries
Before loading the dataset, we imported essential Python libraries for data manipulation and analysis:  
```python
import pandas as pd  # For data handling
import numpy as np   # For numerical operations
import matplotlib.pyplot as plt  # For visualizations
import seaborn as sns  # For advanced visualization
```


### 2. Reading the Dataset 
The aviation accident dataset is loaded using "Pandas":  
```python
aviation_df = pd.read_csv("AviationData.csv", encoding='latin1', low_memory=False)
```


### 3.  Inspecting the Data  
After loading, initial checks are performed to understand the dataset structure:  

- **View first few rows:**  
  ```python
  aviation_df.head()
  ```
- **Check dataset shape (rows, columns):**  
  ```python
  aviation_df.shape
  ```
- **Get column names and data types:**  
  ```python
  aviation_df.info()
  ```
- **Check summary statistics:**  
  ```python
  aviation_df.describe()
  ```
  

### 4. Verifying Data Integrity 
To ensure data integrity, we checked for:  
- **Duplicate values** – using `.duplicated().sum()`
- **Inconsistent column names** – using `aviation_df.columns`  
- **Missing values** – using `.isnull().sum()`  


### Outcome: A Successfully Loaded Dataset 
With the data now loaded and verified, we proceeded with **cleaning and preprocessing** to prepare it for analysis.


## Data Cleaning
### Preparing the Dataset for Analysis

Data cleaning is a crucial step in the data analysis process. It ensures the dataset is accurate, consistent, and ready for further analysis. Below are the key steps performed to clean our aviation accident dataset:  

### 1. Handling Missing Values 
Missing values can affect the reliability of our analysis. Different strategies have been used to handle them:  

- **Numerical Data:** Filled missing values with the mean or median, rounding up to the nearest whole number.  
- **Categorical Data:** Filled missing values with the most frequent value (mode).  
- **Columns with High Missing Percentages:** Considered removing features with excessive missing data that provided little value.  


### 2. Standardizing Column Names  
To ensure consistency in the dataset, the following has been done:  
- Capitalizing the first letter of every word in column names.  


### 3. Handling Duplicate Data
- Checked for duplicate records to avoid biased results.  
- Verified that the dataset contained no duplicate values before proceeding.  


### 4. Adding New Features for Better Insights  
- New features were added to enhance the analysis.  


### Outcome: A Clean & Structured Dataset
After these steps, the dataset is now:  
- Free of missing values.  
- Consistent in format.  
- Enhanced with new features for deeper analysis.  

### Exporting Cleaned Data  

After preprocessing and cleaning the dataset, the final step is to **export the transformed data** into a CSV file for further analysis and visualization. 
The cleaned dataset is saved as:  
📂 **Aviation_Data_Cleaned.csv**  
This file contains structured and refined aviation accident data, ensuring consistency and accuracy for deeper insights and modeling.


## Data Visualization 

This project utilizes data visualization to uncover patterns, trends, and relationships within aviation accident data. The visualizations help in understanding key factors that contribute to accidents and injury severity, offering insights for improved aviation safety.  

#### Selected Visualizations: 
1. **Accident Trends Over Time** – Analyzes how accident occurrences have changed over the years.  
2. **Aircraft Damage Types** – Examines the extent of damage sustained in accidents.  
3. **Accidents by Phase of Flight** – Identifies when accidents are most likely to occur (e.g., takeoff, cruise, landing).  
4. **Top Manufacturers Involved in Accidents** – Highlights aircraft manufacturers with the most recorded accidents.  
5. **Number of Engines vs. Accidents** – Investigates whether engine count correlates with accident frequency.  
6. **Manufacturer vs. Number of Engines** – Explores engine distribution across different aircraft manufacturers.  
7. **Purpose of Flight vs. Injury Severity** – Investigates how flight purpose influences accident outcomes. 
8. **Manufacturer vs. Purpose of Flight** – Analyzes how aircraft manufacturers align with different flight purposes.  
9. **Correlation Heatmap of Injury Severity and Number of Engines** – Shows relationships between injury severity and aircraft engine count.   

These visualizations provide a data-driven perspective on aviation safety, helping to identify risk factors and inform future business decisions.