# Movie Recommendation System 🎬

This repository contains a Movie Recommendation System built using Collaborative Filtering and Matrix Factorization techniques. The project explores different recommendation algorithms, evaluates their performance, and demonstrates how to handle sparse datasets effectively.

## 📊 Dataset
**MovieLens 100K Dataset** (Source: [Kaggle](https://www.kaggle.com/datasets/rajmehra03/movielens100k/))
The dataset consists of 100,000 ratings (1-5) from 943 users on 1,682 movies.
* `movies.csv`: Contains `movieId`, `title`, and `genres`.
* `ratings.csv`: Contains `userId`, `movieId`, `rating`, and `timestamp`.

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, Scikit-surprise, SciPy

## 🧠 Methodologies Implemented

1.  **User-Based Collaborative Filtering:**
    * Calculates user similarity using **Cosine Similarity** on a user-item matrix.
    * Predicts movie ratings based on a weighted average of highly similar users.
2.  **Item-Based Collaborative Filtering:**
    * Calculates similarity between movies rather than users, which is often more stable since movie attributes do not change over time.
3.  **Matrix Factorization via Funk SVD (`scikit-surprise`):**
    * Refactored the SVD approach using the `Surprise` library.
    * **Solution:** Funk SVD only calculates errors on *observed* ratings, ignoring missing data. This drastically improved model accuracy.

## 📈 Evaluation Metrics

* **Precision@K:** Used to evaluate ranking accuracy (how many of the Top-K recommended movies were actually liked by the user in a hidden test set). 
* **Root Mean Squared Error (RMSE):** Used to evaluate rating prediction accuracy.
    * *Funk SVD (Surprise) RMSE:* ~0.93.

## 🚀 How to Run

1. Clone the repository.
2. Ensure you have the required libraries installed:
   ```bash
   pip install pandas numpy scikit-learn scikit-surprise scipy
