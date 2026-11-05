# Movie Financial Success and Investment Risk Prediction

CSF 3127: AI in Finance, Apurv Khanna (Reg. No. 240958208)

Predicts whether a movie earns at least twice its budget (ROI >= 2) using only information known before release: budget, runtime, release year, release month and genre.

## Results (test set, 646 films)

| Model | Accuracy | Failure recall | Macro F1 |
| --- | --- | --- | --- |
| Always guess "success" | 0.56 | 0.00 | n/a |
| Logistic Regression | 0.59 | 0.38 | 0.56 |
| Random Forest (200 trees) | 0.63 | 0.55 | 0.62 |

Votes, vote counts and popularity were excluded on purpose to avoid data leakage, because they are recorded after release.

## Repository contents

| File | What it is |
| --- | --- |
| `movie_financial_risk.ipynb` | Full project code: cleaning, features, models, evaluation, feature importance |
| `data/tmdb_5000_movies.csv` | Dataset (TMDB 5000 Movie Dataset) |
| `requirements.txt` | Python packages needed |

## Dataset

TMDB 5000 Movie Dataset, Kaggle: https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

Movie metadata comes from The Movie Database (TMDb). The file is included here only so the project can be reproduced; all credit goes to TMDb and the Kaggle dataset publisher. 3,229 films remain after removing rows with a budget or revenue of 0.

## How to run

1. Install the packages: `pip install -r requirements.txt`
2. Keep `tmdb_5000_movies.csv` inside the `data/` folder.
3. Open `movie_financial_risk.ipynb` in Jupyter Notebook and run the cells from top to bottom.
