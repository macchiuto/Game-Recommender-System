# Game Recommendation System: Marketplace ML Project

![Python](https://img.shields.io/badge/language-Python-blue)
![Jupyter Notebook](https://img.shields.io/badge/output-Jupyter%20Notebook-orange)

## Overview
This repository contains a **content-based game recommendation system** for a marketplace platform.  
The goal is to suggest 5 games similar to a given game based on game attributes, including sales, scores, platforms, genres, publishers, developers, and ratings.  
The project is developed as a **final project for the Machine Learning course**.

The dataset contains game sales and metadata. After cleaning, imputing missing values, and encoding categorical features, a content-based recommender using **cosine similarity** is implemented.

---

## Repository Structure

- `3A.tsv` → raw dataset for game recommendation system
- `game_recommender.ipynb` → main notebook containing EDA, preprocessing, encoding, content-based recommendation model, and evaluation

---

## Methodology
1. **Exploratory Data Analysis (EDA)**
   - Inspected and summarized data
   - Imputed missing values (median for numerical, mode for categorical)
   - Corrected incorrect types
2. **Encoding Categorical Features**
   - One-hot encoding for Platform, Genre, Publisher, Developer, and Rating
   - Grouped rare categories under "Others"
3. **Content-Based Recommendation**
   - Built feature matrix from sales, scores, and one-hot encoded features
   - Computed cosine similarity between games
   - Wrapped recommendation logic in a function returning 5 similar games
4. **Evaluation**
   - Tested with 3 example games
   - Recommended games matched input games’ platforms, genres, and ratings

---

## Key Insights

- Recommended games generally share **platforms, genres, and ratings** with the input game.
- Cosine similarity on combined numeric and categorical features provides relevant game suggestions.
- Function works reliably for games present in the dataset; rare or missing entries return a clear message.
- The system can be extended with more features or user interactions for hybrid recommendations.

---

## Presentation Video
[Game Recommendation System – Video Presentation](https://drive.google.com/file/d/1tlU7sOtTOs8HT3vSJJ0ED6F4mzMuArwL/view?usp=sharing)

---

## References
- Python libraries: pandas, scikit-learn, numpy, matplotlib

---

## Author

Syalista Galuh Nadira
