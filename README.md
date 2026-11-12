# UCSD Natural Language Processing 258

Final classification notebook for UC San Diego's DSE 258 (Natural Language Processing). It predicts labels for restaurant reviews by combining TF-IDF text features with business attributes, using a tuned logistic regression.

## Repository Contents

| File | Description |
|---|---|
| `Logistic Regression with HyperParamterization Final.ipynb` | Text preprocessing, TF-IDF features, logistic regression with grid search, and the submission output |

## Commit History

### `1e20bb1`: Upload of the final NLP notebook (2025-09-05)
- **Data:** loaded the course's `train.csv` and `test.csv` review datasets.
- **Features:**
  - converted restaurant attributes (e.g. outdoor seating, delivery) into true/false (1/0) columns
  - preprocessed the review text with NLTK: sentence and word tokenization, stop-word removal and Porter stemming
  - built TF-IDF features from the review text
  - combined the TF-IDF matrix with the attribute columns into one sparse matrix, then scaled it
- **Model:**
  - class-balanced logistic regression
  - tuned with `GridSearchCV` (5-fold, accuracy) over `C` from 0.01 to 100, L1 vs. L2 penalty, and three solvers
- **Output:** wrote the test-set predictions to the required `Id`/`Predicted` submission format.

## Tools
Python, pandas, NumPy, SciPy, scikit-learn, NLTK, gensim, Jupyter Notebook
