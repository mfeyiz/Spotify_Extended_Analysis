# Spotify Extended Data Mining Analysis

This project is a **Data Mining** study that analyzes personal Spotify listening data (2023-2025) to understand user behavior, artist associations, and future trends.

---

## Project Overview
The project covers the entire data mining pipeline, starting from processing raw JSON data to applying to machine learning models. The primary goal is to interpret music listening habits through statistical and algorithmic methods.
advanced
## Technologies and Libraries
The project is developed in Python and utilizes the following libraries:

* **Data Manipulation:** `Pandas`, `NumPy`, `JSON`.
* **Visualization:** `Plotly`.
* **Machine Learning (Scikit-Learn):**
    * `KMeans` (Clustering).
    * `RandomForestRegressor` (Forecasting).
    * `StandardScaler` (Data Normalization).
* **Association Rules:** `MLxtend` (Apriori & Association Rules).
* **Statistics:** `SciPy` (T-Test & Z-Score).

## Analysis Layers

### 1. Data Preprocessing
* 15 streaming history JSON files were merged into a single dataset.
* **Filtering:** Tracks played for less than 30 seconds were excluded to remove accidental skips.
* **Feature Engineering:** Derived hour, day name, weekday/weekend status, and listening duration in hours from timestamps.

### 2. Exploratory Data Analysis (EDA)
* **Weekly Heatmap:** Visualized listening density by hour and day of the week.
* **Trend Analysis:** Identified "Forgotten Artists" (high past play count, low recent count) and "Rising Artists" (new favorites).

### 3. K-Means Clustering
* Hours of the day were grouped into **3 distinct clusters** based on activity levels:
    * **Low Activity**.
    * **Medium Activity**.
    * **High Activity**.
* **Model Validation:** Verified using the Elbow method, Silhouette Score, and Davies-Bouldin index.

### 4. Association Rules (Apriori)
* Analyzed co-listening patterns of artists within the same day.
* Calculated metrics such as **Support**, **Confidence**, and **Lift** to determine the probability of listening to Artist Y given Artist X.

### 5. Anomaly Detection and Statistics
* **T-Test:** Performed an independent t-test to check for statistically significant differences between weekday and weekend listening habits.
* **Z-Score:** Identified anomalous days with extreme listening counts using Z-score outliers.

### 6. Future Forecasting (Random Forest)
* Predicted listening trends for the next 6 months using time-series analysis.
* Utilized **Sine/Cosine transformations** for month numbers to capture seasonality within the Random Forest model.

## File Structure
* `spotify_data_mining_project.ipynb`: The main notebook containing all analysis code and visualizations.
* `Streaming_History_Audio_*.json`: Raw Spotify data files.

## How to run?
To run this analysis on your local machine, follow these steps:

### 1. Prerequisites
Ensure you have **Python 3.8+** installed. It is recommended to use a virtual environment or a Jupyter Notebook environment.

### 2. Install Dependencies
Install the required Python libraries using pip:

```bash
pip install pandas numpy plotly scikit-learn mlxtend scipy
```bash

### 3. Data Setup

Download your Extended Streaming History from your Spotify Account privacy settings.

Place all Streaming_History_Audio_*.json files in the same directory as the notebook.

Ensure the file names match the list in the Load Data section of the notebook (e.g., Streaming_History_Audio_2023_0.json to Streaming_History_Audio_2025_14.json).

### 4. Running the Notebook

Open spotify_data_mining_project.ipynb.

Run the cells in sequence, starting with the Library Imports and Data Loading cells.
---
*This study was prepared as a final project for a Data Mining course.*
