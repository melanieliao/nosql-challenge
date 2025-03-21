# UK Food Establishments MongoDB Analysis

## Project Overview
This project utilizes MongoDB and Python (pymongo, pandas) to analyze a dataset of UK food establishments. It includes database setup, data insertion, querying, updating records, and performing aggregation pipelines to extract meaningful insights.

## Dependencies
- Python
- pymongo
- pandas
- pprint
- MongoDB server running on port 27017

## Steps Taken

### 1. Database Setup
- Created a MongoDB client instance connected to a local server.
- Created and accessed the database named `uk_food`.
- Assigned the collection `establishments` for data manipulation.

### 2. Data Insertion
- Inserted new restaurant data ("Penang Flavours") into the collection.
- Updated restaurant data with the correct `BusinessTypeID`.

### 3. Data Cleaning
- Removed establishments with `LocalAuthorityName` as "Dover" from the dataset.
- Converted data types:
  - `longitude` and `latitude` from String to Decimal.
  - `RatingValue` from String to Integer (non-standard ratings were set to `None`).

### 4. Data Querying
- Identified establishments with specific hygiene scores.
- Queried establishments based on location (e.g., London) and rating values.
- Used geographical queries to find top-rated establishments near specific coordinates.

### 5. Data Aggregation
- Implemented a MongoDB aggregation pipeline:
  - Matched establishments with a hygiene score of 0.
  - Grouped and counted them by `LocalAuthorityName`.
  - Sorted results to identify areas with the highest occurrences.

### 6. DataFrame Conversion
- Converted MongoDB query results to Pandas DataFrames for detailed analysis.

## Usage
- Ensure MongoDB is running locally (`mongodb://localhost:27017`).
- Run Python scripts or Jupyter notebooks provided in the project directory.

## Results
- Outputs include printed counts, DataFrame views, and detailed queries facilitating insights into establishment hygiene, ratings, and geographical distribution.


