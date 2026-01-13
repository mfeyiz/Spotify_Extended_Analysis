# Spotify Extended Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-green)
![Plotly](https://img.shields.io/badge/Visualization-Plotly-informational)

This project is a comprehensive **Data Mining** study that analyzes listening habits, creates user profiles, and provides future predictions using personal Spotify streaming history data.

The project utilizes machine learning techniques such as **K-Means Clustering**, **Apriori Algorithm** (Association Rules), and **Random Forest Regression**.

## Features and Techniques Used

This notebook (.ipynb) file includes the following analysis steps:

### 1. Data Preprocessing
* Merging multiple JSON files containing streaming history.
* Timestamp conversions and data cleaning.
* Filtering for tracks played for at least **30 seconds** to ensure meaningful listens.

### 2. Exploratory Data Analysis (EDA)
* Basic statistics for most played tracks and artists.
* **Weekly Activity Heatmap:** Visualizing listening patterns by day of week and hour.
* **Trend Analysis:** Identifying "Forgotten Artists" (previously popular) and "Rising Artists" (new favorites).

### 3. K-Means Clustering Analysis
* Grouping hours of the day by listening activity patterns.
* Using the **Elbow Method** to find the optimal number of clusters (k).

### 4. Association Rules Mining (Apriori Algorithm)
* Discovering which artists are frequently listened to together.
* Visualizing artist associations using **Lift** and **Confidence** metrics.

### 5. Statistical Tests and Anomaly Detection
* **T-Test:** Analyzing statistically significant differences between weekday and weekend listening.
* **Anomaly Detection:** Using the **Z-Score** method to identify extreme listening days.

### 6. Time Series Forecasting with Random Forest
* Training a model on historical data to capture trends and seasonality.
* Predicting future monthly listening counts for the next **6 months**.

### 7. Generate HTML Report
* Exporting all visualizations and analysis results into a comprehensive, interactive `Spotify_Data_Mining_Report.html` file.

## 🛠️ Installation

Follow these steps to run the project on your local machine:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/username/Spotify_Extended_Analysis.git](https://github.com/username/Spotify_Extended_Analysis.git)
   cd Spotify_Extended_Analysis
Install required libraries:

Bash

pip install pandas numpy plotly scikit-learn mlxtend scipy jupyter
Add Your Data:

Request your "Extended streaming history" from your Spotify Privacy Settings.

Place your Streaming_History_Audio_....json files into the project directory.

Start the Notebook:

Bash

jupyter notebook spotify_data_mining_project.ipynb
📊 Sample Visuals
When the project runs, it creates interactive Plotly visualizations:

Activity Heatmap: Shows peak listening times throughout the week.

Association Network: Displays artist pairs with high co-listening probability.

Forecast Graph: Shows historical play counts alongside a 6-month forecast.

📂 File Structure
Plaintext

Spotify_Extended_Analysis/
├── spotify_data_mining_project.ipynb  # Main project code
├── Streaming_History_Audio_2023.json  # (Example) Data file
├── Streaming_History_Audio_2024.json  # (Example) Data file
├── Spotify_Data_Mining_Report.html    # Generated interactive report
└── README.md                          # Project documentation
