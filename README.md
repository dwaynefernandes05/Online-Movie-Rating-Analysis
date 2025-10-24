# 🎬 Movie Rating Analysis

## 📘 Overview
This project analyzes how trustworthy online movie ratings are — particularly focusing on whether platforms like **Fandango** display higher ratings than what movies actually deserve.

It uses real-world data from the [FiveThirtyEight](https://fivethirtyeight.com/features/fandango-movies-ratings/) article *“Be Suspicious Of Online Movie Ratings, Especially Fandango’s”*, which questions whether Fandango inflates its ratings.

---

## 📂 Dataset Information

Two CSV files are used in this analysis:

### 1. `fandango_scrape.csv`
Contains data pulled directly from Fandango.

| Column | Description |
|--------|--------------|
| FILM | The movie title |
| STARS | Number of stars displayed on Fandango |
| RATING | The actual average rating value from HTML |
| VOTES | Number of user reviews |

---

### 2. `all_sites_scores.csv`
Contains aggregated data from other rating platforms.

| Column | Description |
|--------|--------------|
| FILM | The movie title |
| RottenTomatoes | Rotten Tomatoes critic score |
| RottenTomatoes_User | Rotten Tomatoes user score |
| Metacritic | Metacritic critic score |
| Metacritic_User | Metacritic user score |
| IMDB | IMDb user score |
| Metacritic_user_vote_count | Vote count on Metacritic |
| IMDB_user_vote_count | Vote count on IMDb |

---

## 🧠 Key Objectives
- Compare **Fandango displayed ratings** vs **true user ratings**.
- Investigate potential bias in Fandango’s rating system.
- Compare Fandango with **Rotten Tomatoes**, **Metacritic**, and **IMDb**.
- Normalize all ratings to a 0–5 scale for fair comparison.
- Visualize distributions, correlations, and outliers.

---

## ⚙️ Requirements

Install the required Python libraries before running the script:

```bash
pip install pandas numpy matplotlib seaborn
```

---

## 🚀 How to Run

1. Place movie_rating_analysis.py and the two CSV files (fandango_scrape.csv, all_sites_scores.csv) in the same folder.
2. Open a terminal in that folder.
3. Run:
```
python movie_rating_analysis.py
```
4. The script will perform all analyses and generate visualizations (scatterplots, KDE plots, countplots, histograms, and clustermaps).

---

## 📊 Analysis Summary

- Fandango’s displayed ratings were often higher than actual user ratings.
- A clear positive bias was observed compared to other sites.
- Critics and users on Rotten Tomatoes showed more balanced distributions.
- Example: Taken 3 was rated 4.5 stars on Fandango while averaging ~1.8 stars across other platforms.

---

## 🖼️ Visualizations Generated

- Scatterplots: Rating vs Votes
- KDE Plots: Fandango Stars vs True Ratings
- Countplots: Rating differences
- Histograms: Critics vs User differences
- Clustermap: Cross-platform normalized comparisons

---

## 🧩 Files in This Project

```
movie_rating_analysis.py
fandango_scrape.csv
all_sites_scores.csv
README.md
```

---

## 🏁 Conclusion

- This project highlights how platform incentives can bias movie ratings, especially when the same company profits from ticket sales.
- The analysis supports FiveThirtyEight’s conclusion that Fandango inflated displayed ratings during the data collection period.

--- 
