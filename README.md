# INDENG-242-Final-Project NBA Game Outcome Prediction

This repository contains the code and assets for an NBA game outcome prediction system. The project involves data cleaning, feature engineering, machine learning modeling, and a Flask-based user interface.

---

## Directory Structure

```plaintext
├── templates/                # HTML templates for the UI
├── Data Cleaning & EDA.ipynb # Data Cleaning and EDA notebook
├── Modeling.ipynb            # Feature engineering, model training, and evaluation
├── app.py                    # Flask application for user interface
├── README.md                 # Project documentation
├── best_lgbm.joblib          # Trained LightGBM model
├── best_lgbm.pkl             # LightGBM backup (pickle format)
├── final_log.zip             # Preprocessed dataset (compressed)
├── full_gamelog.csv          # Raw team game log data
├── full_player_gamelog.csv   # Raw player game log data
├── full_player_stats.csv     # Raw player statistics data
├── lstm_model.h5             # Trained LSTM model
└── scaler.pkl                # Scaler object for feature normalization
└── requirements.txt          # Dependency requirements
```

## Requirements

**Python Version**: 3.8 or later  
**Dependencies**: Install the required libraries using the following command:

```bash
pip install -r requirements.txt
```

## Steps to Replicate
### 1. Data Cleaning and EDA
#### File: Data Cleaning & EDA.ipynb
#### Input:

full_gamelog.csv

full_player_gamelog.csv

full_player_stats.csv

#### Output:

final_log.csv (compressed as final_log.zip for GitHub size limitations)
#### Instructions:

Extract final_log.csv from final_log.zip:
```bash
unzip final_log.zip
```

Run Data Cleaning & EDA.ipynb to clean and preprocess the raw data.

### 2. Model Development
#### File: Modeling.ipynb

#### Input:

final_log.csv (preprocessed dataset)

#### Steps:

Perform feature engineering.

Train LightGBM and LSTM models.

Combine predictions using an ensemble method.

#### Output:

best_lgbm.joblib: Trained LightGBM model

lstm_model.h5: Trained LSTM model

scaler.pkl: Scaler for feature normalization

### 3. Run the Flask Application
#### Required Files:

app.py

best_lgbm.joblib

lstm_model.h5

scaler.pkl

final_log.csv (extracted from final_log.zip)

templates/ (HTML files)

#### Instructions:

Run the Flask app:
```bash
python app.py
```

Open a web browser and navigate to:
```arduino
http://127.0.0.1:5000
```

## UI Workflow
**Team Selection**: Use dropdown menus to select two NBA teams.

**Player Selection**: Checkboxes will appear for each team’s players.

**Prediction Results**: Click the "Predict Outcome" button to view the predicted result.

**Navigation**: Easily return to team selection or modify player choices.

## Notes
Extract final_log.csv from final_log.zip before running any notebook or the Flask app.

Pre-trained models (best_lgbm.joblib and lstm_model.h5) and the scaler (scaler.pkl) are provided.

Raw data is split into multiple CSV files due to GitHub size limits.
