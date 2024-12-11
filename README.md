# TuneTrends: Decade-Based Music Analysis

## Project Overview
**TuneTrends** explores the defining characteristics of popular music from 1980 to 2020, analyzing features like BPM, loudness, sentiment, and danceability to understand how music evolved over decades. The project aims to uncover trends in song features and predict the future popularity of songs using machine learning models.

---

## Research Question
What are the defining characteristics of each decade’s music (1980–2020)? How have song features evolved, and can we use them to predict a song’s popularity?

---

## Data Sources
1. **Billboard Hot 100**: Weekly Top 100 songs (1970–2020) dataset sourced from Kaggle.
   - Cleaned to remove duplicate song-artist pairs.
   - Consolidated metrics: mean rank and weeks on the Billboard.
2. **Spotify API**:
   - Scraped audio features like danceability, energy, valence, and tempo for selected songs.
   - Limited to the top 1500 most popular songs per decade due to API rate limits.

---

## Methodology
1. **Data Cleaning**:
   - Grouped duplicate songs by song-artist pairs.
   - Created a custom popularity metric: `Popularity = Weeks on Billboard / Mean Rank`.

2. **Feature Extraction**:
   - Used Spotify API to fetch key audio features: danceability, acousticness, instrumentalness, energy, tempo, loudness, and more.

3. **Data Analysis**:
   - Visualized trends across decades using histograms and line plots (e.g., average BPM per decade).
   - Applied a Random Forest Regressor to predict song popularity.

4. **Feature Importance**:
   - Leveraged SHAP (SHapley Additive exPlanations) to identify the most significant features contributing to song popularity.

---

## Tools and Technologies
- **Data Collection**: Python, Pandas, Spotify API, Kaggle
- **Data Visualization**: Matplotlib, Seaborn
- **Machine Learning**: Random Forest Regressor, SHAP
- **Development Tools**: Jupyter Notebook, Scikit-learn

---

## Results
1. **Music Trends**:
   - Identified decade-level shifts in key features like BPM, danceability, and valence.
   - Observed higher acousticness in the 1990s compared to the 2000s, indicating a trend toward acoustic sounds.

2. **Popularity Predictors**:
   - Danceability and loudness emerged as the most critical predictors of song popularity.
   - High-energy and danceable songs consistently scored higher on popularity metrics.

3. **Model Insights**:
   - Achieved 93% accuracy in predicting song popularity using Random Forest.
   - SHAP analysis revealed decade-specific feature importance, with valence being more significant in the 1990s than in the 2000s.

---

## Challenges
- **Data Consistency**:
  - Different naming conventions between Spotify API and Billboard datasets resulted in data loss.
- **API Limitations**:
  - Spotify’s rate limits restricted the number of songs scraped per decade.
  
## Future Improvements
- Incorporate additional metrics like YouTube views or weekly Spotify plays to refine the popularity metric.
- Explore neural network models for better prediction accuracy.
- Investigate cultural or technological factors influencing trends in music features.

---

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/tunetrends.git

## Contributors
Yelaman Moladagali, Ryan Ye, Noelle Lin.


