# Problem Analysis Workshop 3 — Clustering & K-Means (Fraud Detection)

This repository contains a step-by-step Jupyter notebook that demonstrates **K-Means clustering** on a financial transactions dataset for a **fraud detection** use case. It aligns with your instructor's Workshop 3 guidelines and rubric.

## Contents
- `Workshop3_ClusteringKMeans_Fraud.ipynb` — main notebook with:
  - Setup & environment info
  - Data loading (tries local file and provides Kaggle path instructions)
  - Cleaning & preprocessing
  - **Exploratory Data Analysis (EDA)** with range and measures of central tendency
  - **Standardization** (z-score) and **Normalization** (min–max)
  - **Feature selection logic** for clustering (why the chosen columns)
  - **K-Means**: elbow (inertia), silhouette, best *k* selection, fit, interpretation
  - PCA visualization and cluster profiles
  - Talking points and 50-word summaries
- `requirements.txt` — minimal environment
- `Submission_Template.md` — fill this and export as PDF (include your GitHub repo URL)

## Data
The notebook first tries to load a local CSV at:
```
/mnt/data/bank_transactions_data_2.csv
```
You can replace this with your file path. The notebook also includes a **Kaggle path stub** for the dataset you referenced:
- Kaggle input location: *(as provided in your kernel environment)*  
  `../input/fraud-detection-clustering-anomaly-analysis/<your-file>.csv`

Your link: https://www.kaggle.com/code/sulaniishara/fraud-detection-clustering-anomaly-analysis/input  
(If running in Kaggle, ensure the dataset is added as an input; locally, download and point the path to your CSV.)

## How to Run
```bash
# (optional) create and activate a virtual environment
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

pip install -r requirements.txt

# Launch Jupyter
jupyter notebook Workshop3_ClusteringKMeans_Fraud.ipynb
```
Follow the notebook cells in order. **Best k** is computed programmatically via silhouette; the value will print in the output.

## Workshop Fit
- Includes initial markdown cell for **name/ID** (edit it).
- Adds <=5-sentence explanations for each process.
- Includes a 50-word **"How clustering applies"** summary and a 50-word **"K-Means output interpretation"** summary.
- Provides figures (histograms, box plots, elbow, silhouette, PCA) and a cluster profile table.

## Notes
- Start with a sample (e.g., 200k rows) if your dataset is very large, to iterate quickly.
- After validating logic and best *k*, rerun on the full dataset if resources allow.
