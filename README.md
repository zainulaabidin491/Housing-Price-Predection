# Real Estate Price Prediction 🏠

This project implements a machine learning system to estimate property prices in Pakistan. It features a comprehensive data processing pipeline, a high-performance regression model, and a web-based interface for real-time predictions.

## 1. Project Overview
The objective of this project is to develop a predictive model that estimates property prices based on features such as location, property type, area, and the number of bedrooms/baths. The system includes:
* **Data Processing Pipeline**: For cleaning and normalizing raw real estate data.
* **Trained Regression Model**: A Random Forest approach for high accuracy.
* **Web Interface**: A user-friendly interaction layer for price estimation.

## 2. Data Engineering & Preprocessing
To ensure model quality, the following preprocessing steps were implemented:
* **Data Cleaning**: Removed non-predictive columns such as `property_id`, `page_url`, and agent info to reduce noise.
* **Missing Value Analysis**: Identified null values, particularly in `agency` and `agent` columns, which were subsequently dropped.
* **Feature Scaling**: Applied `MinMaxScaler` to numerical features ($Total\_Area$, $bedrooms$, $baths$, $latitude$, $longitude$, and $price$) to normalize values between 0 and 1.
* **Categorical Encoding**: Utilized `LabelEncoder` to convert object types (e.g., $city$, $property\_type$, $purpose$) into numerical format for model compatibility.

## 3. Model Development
* **Algorithm**: A **Random Forest Regressor** was selected for its ability to handle non-linear relationships and high-dimensional data.
* **Configuration**: The model was initialized with **200 estimators** and a fixed random state for reproducibility.
* **Training**: The dataset was split into an **80/20 train-test ratio**.



### Evaluation Metrics
The model demonstrates strong predictive performance with the following scores:
| Metric | Value |
| :--- | :--- |
| **Mean Absolute Error (MAE)** | $\approx 3953.74$ |
| **Mean Squared Error (MSE)** | $\approx 25,437,036.39$ |
| **R² Score** | **0.97** |

