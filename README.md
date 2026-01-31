# 🎵 Hit Song Predictor with Logistic Regression

This project explores **logistic regression** as a supervised machine learning technique for predicting hit songs, using **audio features** from a Spotify dataset.

The goal is to understand **how audio characteristics influence commercial success**, and identify which features—individually and in combination—best distinguish hits from non-hits.

---

## 📌 Project Overview

A binary classification model to predict whether a song will be a "hit" based on its audio features.

### 🎯 Approach
* **Algorithm:** Logistic Regression
* **Features:** Danceability, Energy, Valence, Tempo, Acousticness, Instrumentalness, Liveness, Speechiness, Loudness
* **Target:** Binary classification (Hit vs Non-Hit)
* **Purpose:** Identify patterns in successful songs and provide data-driven insights for playlist curation

---

## 🔍 Why Feature Engineering Matters

Initial correlation analysis revealed that **no individual audio feature strongly correlates with hit status** (all correlations < 0.10).

This finding led to a critical insight:
* **Hit songs are not defined by single characteristics**
* Success depends on **combinations and interactions** of multiple features
* Marketing, timing, and artist popularity play significant roles beyond audio alone

**Solution:** Creating interaction features to capture complex relationships:
* `Energy × Danceability` → "Party factor" (energetic & danceable)
* `Valence × Energy` → Upbeat, positive vibes
* `Mood Score` → Overall emotional tone
* `Normalized Tempo` → Standardized BPM for better scaling

---

## 📊 Exploratory Data Analysis

### Feature Distributions: Hits vs Non-Hits

**Key Observations:**
* **Danceability:** Hits skew toward higher values (0.6-0.8)
* **Energy:** Hits favor energetic tracks (0.7-0.9)
* **Valence:** Hits slightly more positive/happy
* **Tempo:** Nearly identical distributions—weak predictor
* **Instrumentalness:** Extreme left skew—vocals dominate hits

### Correlation Analysis

**Findings:**
* Low multicollinearity (most pairs < 0.3) ✅
* Energy ↔ Loudness strongest correlation (0.65)
* Features are largely independent, contributing unique information
* No single feature strongly predicts hits—feature engineering necessary

---

## 🧪 Progress So Far

✅ Data loading and exploration  
✅ Exploratory Data Analysis (EDA) with visualizations  
✅ Feature distribution analysis  
✅ Correlation heatmap  
✅ Feature engineering strategy defined  
⏳ Model training (in progress)  
⏳ Model evaluation (upcoming)  
⏳ Feature importance analysis (upcoming)  

---

## 🚀 Technologies Used

* **Python 3.13.9**
* **pandas** - Data manipulation and analysis
* **NumPy** - Numerical operations
* **matplotlib & seaborn** - Data visualization
* **scikit-learn** - Machine learning (upcoming)

---

## 🙌 Credits

Built with 💻 and 🎵 by **@marcanjoul**

### Dataset

The dataset used in this project was sourced from Kaggle:
- **Source:** Top Hits Spotify from 2000-2019  
- **Link:** [https://www.kaggle.com/datasets/paradisejoy/top-hits-spotify-from-20002019]

The dataset was used for educational purposes to explore binary classification and music analytics.

---
