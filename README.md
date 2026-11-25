# Password Strength Classification

A notebook that predicts whether a password is weak, medium or strong with a random forest classifier.

## How it works

1. Reads a CSV of passwords and their strength labels (`pw_strength.csv`, with columns `password` and `strength`), skipping bad lines and dropping rows with missing values.
2. Turns each password into features with a character-level `TfidfVectorizer`, where every character is a token.
3. Splits the data 80/20 and trains a `RandomForestClassifier` with 100 trees.
4. Prints training and test scores, a confusion matrix (Weak, Medium, Strong) and a classification report.
5. Predicts the strength of a sample password at the end.

The dataset file is not included in this repo. The notebook reads it from `/content/pw_strength.csv`, which is the Google Colab working directory, so upload your own copy there or change the path.

## Tech stack

Python, pandas, NumPy, scikit-learn, seaborn, matplotlib.
