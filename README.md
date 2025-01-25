# pyspark_basic
analyze MY house pricing data using pyspark
## Data Structure
data is from Kaggle: https://www.kaggle.com/datasets/lyhatt/house-prices-in-malaysia-2025  
Columns:  
- Township: Township or neighborhood of the property (e.g., Cheras, Subang Jaya).
- Area: Larger locality or district (e.g., Klang Valley, Penang Island).
- State: State in Malaysia where the property is located.
- Tenure: Ownership type (e.g., Freehold, Leasehold).
- Type: Property category (e.g., Terrace, Condominium).
- Median_Price: Median property price in Malaysian Ringgit (MYR).
- Median_PSF: Median price per square foot (MYR).
- Transactions: Total number of property transactions recorded in the township. 
## Data Loading & Exploration
### Load Data:
- Load the dataset into PySpark from a CSV or Parquet file.
- Inspect the schema and ensure column types are correctly inferred.
### Basic Statistics:
- Calculate the average Median_Price and Median_PSF across all properties.
- Identify the state with the highest and lowest median property prices.
### Filter & Grouping:
- Filter properties with Median_Price > 1 million MYR and count them by Type.
- Group data by State and calculate:
    - Total Transactions.
    - Average Median_PSF.
### Data Transformation:
- Create a new column, Price_to_PSF_Ratio, as Median_Price / Median_PSF.
- Categorize properties into price ranges (e.g., <500k, 500k-1M, >1M) and count them.
### Insights by Property Type:
- Compare the average Median_Price for Freehold vs. Leasehold properties by Type.
- Find the Township with the highest number of Transactions for condominiums.
### Area Insights:
- Determine the Area with the highest Median_PSF.
- Identify the most popular Type of property in each Area.
- Rank Townships by Median Price within Each Area
