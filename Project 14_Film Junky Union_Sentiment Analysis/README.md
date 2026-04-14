# Film Junky Union — Sentiment Analysis (NLP)

**Dr. Danisha L. Thomas** | TripleTen Data Science Bootcamp | Sprint 14

---

## Project Overview

The Film Junky Union, a community for classic movie enthusiasts, needed a system to automatically filter and categorize movie reviews. This project builds a sentiment classification model to detect negative reviews from a dataset of IMDB movie reviews with polarity labels.

**Primary Metric:** F1 Score  
**Benchmark:** F1 ≥ 0.85  
**Best Test F1:** 0.89 ✅  
**Status:** Approved on first submission

---

## Dataset

- IMDB movie reviews dataset with binary polarity labels (positive/negative)
- Train/test split provided by project
- Text preprocessing applied before vectorization

---

## Models Trained

| Model | Preprocessing | Vectorization | Classifier | Test F1 |
|-------|--------------|---------------|------------|---------|
| Model 0 | — | — | Dummy Classifier (baseline) | ~0.50 |
| Model 1 | NLTK stopword removal | TF-IDF | Logistic Regression | **0.89** ✅ |
| Model 3 | spaCy lemmatization | TF-IDF | Logistic Regression | **0.89** ✅ |
| Model 4 | spaCy lemmatization | TF-IDF | LightGBM | 0.87 ✅ |

> Note: BERT (Model 9) was not implemented due to computational constraints on the training platform.

---

## Results

| Metric | Score |
|--------|-------|
| Best Test F1 | **0.89** |
| Benchmark | ≥ 0.85 |
| Status | ✅ Approved — First Submission |

---

## Key Findings

- TF-IDF with Logistic Regression achieved the highest F1 score (0.89), matching spaCy lemmatization with the same classifier
- NLTK stopword removal alone was sufficient to reach the benchmark without more complex preprocessing
- LightGBM performed competitively (0.87) but did not outperform the simpler Logistic Regression approach
- All models significantly exceeded the 0.85 benchmark, demonstrating the strength of classical NLP pipelines for binary sentiment classification

---

## Tech Stack

`Python` `NLTK` `spaCy` `TF-IDF` `Scikit-learn` `LightGBM` `Logistic Regression` `NLP` `Pandas` `Jupyter Notebook`

---

## Author

**Dr. Danisha L. Thomas, PhD**  
Data Scientist | Behavioral Intelligence & Healthcare Analytics  
[LinkedIn](https://linkedin.com/in/drdlthomas) | [GitHub](https://github.com/drdanishalthomas)
