📦 Build & Track ML Pipeline with DVC

A complete end-to-end machine learning workflow demonstrating data ingestion, preprocessing, feature engineering, model training, evaluation, experiment tracking, and versioning using DVC (Data Version Control).

This project ensures reproducible ML pipelines, consistent datasets, and experiment traceability.


- Project Structure
Build_track_ML_pipeline_with_DVC/
│
├── data/                     # Raw & processed data (DVC-managed)
│   ├── raw/
│   └── processed/
│
├── src/                      # Source code files
│   ├── data_ingestion.py
│   ├── data_transformation.py
│   ├── model_training.py
│   ├── model_evaluation.py
│   └── utils/
│
├── models/                   # Saved models (DVC-managed)
│
├── dvc.yaml                  # DVC pipeline configuration
├── dvc.lock                  # Auto-generated lock file
├── params.yaml               # Configurable pipeline parameters
├── requirements.txt          # Python dependencies
├── README.md                 # Project documentation
└── .dvc/                     # DVC cache & metadata



📊 Pipeline Stages

This project contains the following DVC stages:

1️⃣ Data Ingestion (data_ingestion.py)

Loads raw dataset

Cleans and prepares base dataframe

Maps sentiment labels (e.g., happiness = 1, sadness = 0)

Saves processed dataset to data/

2️⃣ Data Transformation

Performs text preprocessing

Tokenization / stop-word removal

Creates final training dataset

3️⃣ Model Training

Trains ML models on processed data

Saves model artifacts under models/

Uses params from params.yaml

4️⃣ Model Evaluation

Generates metrics (accuracy, precision, recall, F1)

Outputs a classification_report

Saves metrics under reports/


- OUTPUT
![alt text](<WhatsApp Image 2025-11-24 at 01.40.52_679705f5.jpg>)


# Build & Track ML Pipelines with DVC

## How to run?

conda create -n test python=3.11 -y

conda activate test

pip install -r requirements.txt


## DVC Commands

git init

dvc init

dvc repro

dvc dag

dvc metrics show
