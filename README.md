# 🎬 Movie Recommender System

This project is an AI-powered **content-based movie recommendation system** built using Python, Natural Language Processing (NLP), and machine learning techniques. By leveraging metadata from a popular movie dataset (TMDB 5000), the system provides personalized recommendations based on textual similarity between movies using genres, keywords, cast, and overview information.

---

## 📌 Project Objective

To develop a movie recommendation system that suggests similar movies to a user-selected title based on content similarity, without relying on user ratings or collaborative data. The core goal is to demonstrate how NLP and vectorization can be used to build effective and interpretable recommendation logic.

---

## 🧠 How It Works

The system uses **content-based filtering** by extracting features from metadata such as:

- **Genres**
- **Keywords**
- **Overview**
- **Cast**
- **Crew (Director)**

These features are combined into a unified "tag" for each movie, which is then processed using **text vectorization** and **cosine similarity** to identify similar movies.

---

## 🛠️ Technologies & Libraries Used

| Tool/Library              | Purpose                                              |
|--------------------------|------------------------------------------------------|
| `pandas`                 | Data manipulation and merging datasets               |
| `ast`                    | Parsing stringified Python objects                   |
| `nltk`                   | Tokenization and stemming of text                    |
| `scikit-learn`           | Vectorization (CountVectorizer) and similarity calc |
| `cosine_similarity`      | Pairwise similarity comparison between movie vectors |


---

## 🔍 Feature Transformation & Modeling

- **Vectorization**  
  Applied `CountVectorizer` from `scikit-learn` to convert `tags` into a bag-of-words model with a vocabulary of the top 5000 features, excluding English stopwords.

- **Similarity Computation**  
  Used `cosine_similarity` to compute pairwise distances between all movie vectors.

---

## ▶️ How to Run

- Clone this repository and open it in a Jupyter notebook or Google Colab environment.
  ```bash
  git clone https://github.com/anushka-1205/MovieRecommender.git
  cd MovieRecommender
  ```
- Make sure the `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv` datasets are placed correctly (e.g., in `/content/sample_data/` if using Colab).
- Run all the cells in sequence.
- Call `recommend('Movie Title')` to test recommendations.

---

Author: Anushka Srivastava
