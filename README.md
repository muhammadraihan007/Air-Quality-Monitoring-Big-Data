# Air Quality Monitoring and Pollution Pattern Analysis Using Big Data

## Project Overview

This project analyzes large-scale air quality data from monitoring stations across India using Big Data technologies. The project focuses on understanding pollution patterns, predicting AQI categories from pollutant measurements, and grouping monitoring stations based on their pollution characteristics.

## Dataset

**Dataset:** Air Quality Data in India (2015–2020)

**Source:** Kaggle  
https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india

The dataset contains hourly air quality measurements from monitoring stations across India.

## Technologies Used

- Python
- Apache Spark / PySpark
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab
- Parquet

## Project Workflow

1. Data loading and preprocessing
2. Missing-value analysis
3. Exploratory Data Analysis
4. AQI category classification
5. Station-level pollution clustering
6. Model evaluation
7. Data storage using Parquet
8. Visualization and interpretation

## Machine Learning

### Classification

Random Forest was used to predict `AQI_Bucket` using pollutant measurements such as:

- PM2.5
- PM10
- NO2
- SO2
- CO
- O3

Random Forest achieved:

- Accuracy: **62.78%**
- Weighted Precision: **61.48%**
- Weighted Recall: **62.78%**
- Weighted F1 Score: **61.47%**

### Clustering

K-Means clustering was used to group monitoring stations according to their pollution profiles.

The optimal number of clusters was found to be **3** using the Silhouette Score.

- Silhouette Score: **0.6585**
- Davies-Bouldin Index: **0.6008**
- Calinski-Harabasz Score: **55.9135**

## Big Data Processing

Apache Spark was used to process the large air-quality dataset.

The processed data was also stored and queried using **Parquet** format.

Dataset size:

- **2,589,083 hourly records**
- **110 monitoring stations**
- **16 columns**

## Key Findings

- PM10 and PM2.5 were the most important pollutants for AQI category prediction.
- PM10 and PM2.5 together contributed approximately **77.11%** of Random Forest feature importance.
- Monitoring stations could be grouped into three distinct pollution profiles.
- One cluster represented a single-station outlier with particularly high SO2 and CO levels.
- Delhi had the highest average PM2.5 among the top cities analyzed.

## Project Notebook

The complete implementation is available in:

`Air_Quality_Big_Data_Project.ipynb`

## Note

The current implementation uses Apache Spark and Parquet for Big Data processing. HDFS integration was proposed as future work and was not implemented in the current project.
