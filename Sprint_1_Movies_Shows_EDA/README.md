![Project Banner](images/Movies_and_Shows_EDA_Banner.png)
# Sprint 1 — Movies & Shows Data Analysis

![Python](https://img.shields.io/badge/Python-3.9-blue) ![Pandas](https://img.shields.io/badge/Pandas-EDA-green) ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## Project Overview

This project applies foundational data analysis skills using the Pandas library to explore a dataset of movies and television shows sourced from IMDb. The analysis covers data loading, column standardization, targeted data cleaning, Boolean filtering, and the development of reusable query functions.

---

## Objectives

- Load and inspect a real-world entertainment dataset
- Standardize inconsistent column names using `.rename()`
- Identify and correct data entry errors using `.loc[]`
- Filter and query the dataset using single and compound Boolean conditions
- Build modular, reusable functions for flexible data retrieval

---

## Dataset

| Field | Description |
|-------|-------------|
| `name` | Actor or actress name |
| `character` | Character portrayed |
| `role` | Role type (e.g., ACTOR) |
| `title` | Movie or show title |
| `type` | MOVIE or SHOW |
| `release_year` | Year of release |
| `genres` | List of genres |
| `imdb_score` | IMDb rating (0–10) |
| `imdb_votes` | Number of IMDb votes |

**Source:** `movies_and_shows.csv`

---

## Analysis Summary

### Data Cleaning
The raw dataset contained several inconsistencies requiring correction before analysis:
- Column names with typos, mixed casing, extra whitespace, and zero-substituted characters (e.g., `r0le`, `imdb sc0re`)
- An encoding error replacing special characters in an actor's name (`"In??s Prieto"` → `"Ines Prieto"`)

All issues were resolved using `.rename()` with a column mapping dictionary and `.loc[]` for targeted row-level correction.

### Functions Built

| Function | Description |
|----------|-------------|
| `get_unique_top_movies(min_score)` | Returns unique titles at or above a given IMDb score |
| `get_top_movies_from_decade(decade_start, min_score)` | Returns top-rated titles from a specific decade |
| `get_actors_for_title(title)` | Returns a formatted string of all actors in a given title |
| `categorize_imdb_score(title)` | Classifies a title as Excellent / Good / Average / Low |

### IMDb Score Classification

| Category | Score Range |
|----------|-------------|
| Excellent | ≥ 9.0 |
| Good | 7.0 – 8.9 |
| Average | 5.0 – 6.9 |
| Low | < 5.0 |

---

## Sample Outputs

**Top-rated titles (IMDb ≥ 9.0):**

![Top rated titles](images/top_rated_titles.png)

**Top titles from the 1990s (IMDb ≥ 8.5):**

![1990s top titles](images/top_titles_1990s.png)

---

## How to Run

1. Clone or download this repository
2. Ensure `movies_and_shows.csv` is available in a `/datasets/` directory (or update the file path in the notebook)
3. Open `notebook.ipynb` in Jupyter Notebook or VS Code
4. Run all cells sequentially (`Kernel > Restart & Run All Cells`)

**Dependencies:**
```
pandas
```

---

## Skills Demonstrated

`Python` `Pandas` `Data Cleaning` `Boolean Indexing` `DataFrame Filtering` `Functions` `EDA`
