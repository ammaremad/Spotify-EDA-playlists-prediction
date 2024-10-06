# Spotify Most Streamed Songs Analysis

## Project Overview
This project aims to analyze the dataset of Spotify's most streamed songs to identify factors influencing their popularity and to build predictive models for estimating the number of playlists a song is featured in on Spotify. The analysis includes data preprocessing, exploratory data analysis (EDA), feature engineering, and the implementation of various machine learning models.

## Table of Contents
- [Objective](#objective)
- [Data Overview](#data-overview)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Results](#results)
- [Conclusion](#conclusion)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Objective
The primary goal of this project is to analyze the dataset of Spotify's most streamed songs to understand the factors influencing their popularity and to build predictive models to estimate the number of playlists a song is featured in on Spotify.

## Data Overview
The dataset consists of 953 entries and 25 columns, including features such as:
- **Track_Name**: Name of the song
- **Artist_Name**: Name of the artist(s)
- **Artist_Count**: Number of artists contributing to the song
- **Released_Year**: Year when the song was released
- **In_Spotify_Playlists**: Number of Spotify playlists the song is included in (target variable)
- **Streams**: Total number of streams on Spotify
- Various musical attributes (e.g., BPM, Danceability, Energy, Acousticness)

## Data Preprocessing
- **Data Cleaning**: Dropped irrelevant columns and handled missing values by replacing them with the mode for categorical variables.
- **Feature Engineering**: Encoded categorical variables using label encoding and dropped features with weak to moderate negative correlations with the target variable.
- **Normalization**: Scaled features to a common range using MinMaxScaler.

## Exploratory Data Analysis
- **Visualizations**: Created various plots including bar plots for the top 10 most streamed songs, total streams per year, and top artists by total streams. Heatmaps were used to visualize correlations between numerical variables, and scatter plots were used to explore relationships between features.

## Feature Engineering
The target variable chosen for modeling is `In_Spotify_Playlists`. The dataset was refined to include only relevant features based on correlation analysis, leading to the removal of several columns with weak relationships to the target.

## Modeling
Multiple machine learning models were implemented to predict the target variable:
1. **Linear Regression**
2. **Random Forest Regression**
3. **XGBoost Regression**
4. **Decision Tree Regression**
5. **Gradient Boosting Regression**

Each model was evaluated using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared values.

## Results
- **Random Forest Regression** achieved the best performance with an R-squared value of 0.93.
- **Decision Tree Regression** followed closely with an R-squared value of 0.92.
- Other models, including XGBoost and Gradient Boosting, also performed well but were slightly less accurate.

## Conclusion
The analysis successfully identified key factors influencing song popularity on Spotify and established robust predictive models for estimating playlist inclusion. The Random Forest model emerged as the top performer, demonstrating the effectiveness of ensemble methods in this context.

## Installation
To run this project, ensure you have Python installed along with the following libraries:
```bash
pip install pandas numpy matplotlib seaborn plotly scikit-learn xgboost imbalanced-learn
```

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/spotify-streamed-songs-analysis.git
   ```
2. Navigate to the project directory:
   ```bash
   cd spotify-streamed-songs-analysis
   ```
3. Run the Jupyter Notebook or Python script to execute the analysis.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

Feel free to customize the sections as needed, especially the installation and usage instructions to match your project's structure and requirements.
