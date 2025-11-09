project:
  title: "ML Assignment 4 — Airline Passenger Satisfaction Pipeline (AdaBoost)"

  short_description: >
    This repository trains and evaluates an AdaBoost-based machine learning pipeline 
    for the Airline Passenger Satisfaction dataset.
    It automates data ingestion, validation, transformation, model training, and evaluation — 
    all driven by YAML configurations.
    The system ensures a modular, reusable, and production-ready structure.

  dataset:
    name: "Airline Passenger Satisfaction Dataset"
    source: "https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction"
    description: >
      The dataset contains passenger details, flight information, and service feedback.
      The goal is to predict satisfaction levels based on various flight and service-related features.

tech_stack:
  - Python
  - scikit-learn
  - pandas
  - numpy
  - joblib
  - YAML
  - logging
  - matplotlib

features:
  - End-to-end ML pipeline for satisfaction prediction
  - YAML-based configuration (no hardcoding)
  - Independent modular components for each pipeline stage
  - Artifact tracking for reproducibility
  - Centralized logging for monitoring
  - Extendable structure for other algorithms
  - Evaluation metrics saved in JSON format
  - Optional Streamlit-ready deployment (via app.py)

setup_instructions:
  - "Create and activate virtual environment:"
  - "python -m venv .venv"
  - ".\\.venv\\Scripts\\activate"
  - "Install dependencies:"
  - "pip install -r requirements.txt"
  - "Ensure dataset exists at: artifacts/data_ingestion/airplane1.csv"

run_instructions: |
  Run the full pipeline (Ingestion → Validation → Transformation → Training → Evaluation):

  ```bash
  python main.py
