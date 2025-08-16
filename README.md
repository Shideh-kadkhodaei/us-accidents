# US Accidents Outlier Detection

This repository contains a Google Colab project for detecting outliers in the US Accidents dataset using cuDF for GPU-accelerated data processing. The project demonstrates how to preprocess large datasets, handle missing values, and visualize geographical outliers.

## Project Overview

The code performs the following steps:

1. Install Kaggle API – Installs the kaggle Python package to download datasets directly from Kaggle.  
2. Upload Kaggle API Token – Upload your kaggle.json token to authenticate Kaggle API access.  
3. Setup Kaggle Authentication – Move the token to the hidden .kaggle folder and set proper permissions.  
4. Download Dataset – Downloads the [US Accidents dataset](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents) from Kaggle.  
5. Extract Dataset – Unzip the downloaded dataset to access CSV files.  
6. Load Data with cuDF – Load the CSV into a GPU DataFrame for faster processing.  
7. Data Cleaning – Remove rows with missing latitude and longitude values, and ensure valid coordinate ranges.  
8. Outlier Detection – Identify outliers using the 3 standard deviations method for latitude and longitude.  
9. Visualization – Plot normal points and outliers on a scatter plot using matplotlib.

## Usage

1. Open the notebook in Google Colab.  
2. Upload your kaggle.json API token when prompted.  
3. Run the cells sequentially from top to bottom.  
4. The final plot will show outliers in red on a US map.  

## Requirements

- Python 3.x  
- Google Colab  
- Libraries:
  - cudf
  - matplotlib
  - kaggle
  
> Note: cuDF requires a GPU runtime in Colab. Make sure your notebook is set to Runtime → Change runtime type → GPU.

## Notes

- This project uses cuDF for GPU acceleration. If you don’t have a GPU, you can replace cudf with pandas, but processing will be slower.  
- Outlier detection is based purely on statistical deviation; for more advanced anomaly detection, machine learning methods can be applied.  
- Ensure the dataset CSV file path matches the one in the code (US_Accidents_March23.csv).  
