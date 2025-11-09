

project:
  title: "ML Assignment 4 — Airline Passenger Satisfaction Pipeline (AdaBoost)"
  short_description: >
    This project implements a complete Machine Learning pipeline using the AdaBoost Classifier 
    on the Airline Passenger Satisfaction dataset. It automates all key stages — 
    Data Ingestion, Validation, Transformation, Model Training, and Evaluation — 
    controlled entirely through YAML configurations. 
    The system ensures a modular, reusable, and production-ready structure.
  dataset: 
    name: "Airline Passenger Satisfaction Dataset"
    source: "Kaggle - https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction"
    description: >
      The dataset contains information about airline passengers including 
      flight details, service quality feedback, and overall satisfaction levels.
      The goal is to predict passenger satisfaction based on various flight and service attributes.

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
  - Automated ML pipeline for airline satisfaction prediction
  - YAML-based configuration (no hardcoded parameters)
  - Independent modular components for each pipeline stage
  - Artifact tracking for reproducibility
  - Logging system for detailed runtime monitoring
  - Extendable structure for integrating new models or datasets
  - Evaluation metrics saved automatically in JSON format
  - Optional Streamlit-ready deployment (via app.py)

repository_structure: |
  ML_Assignment_4/
  ├── main.py                 # Runs all pipeline stages sequentially
  ├── app.py                  # Optional deployment or prediction script
  ├── params.yaml             # Model hyperparameters and tuning settings
  ├── config.yaml             # File path and component configurations
  ├── schema.yaml             # Data schema for validation
  ├── requirements.txt        # Project dependencies
  ├── README.md               # Project documentation
  │
  ├── src/
  │   ├── components/         # Modules for each ML pipeline stage
  │   ├── config/             # Configuration loader/manager
  │   ├── constants/          # Global constants and schema references
  │   ├── entity/             # Data classes for configs and artifacts
  │   ├── pipeline/           # Scripts to run each stage
  │   └── utils/              # Helper utilities (file handling, YAML ops)
  │
  ├── artifacts/              # Auto-generated outputs after execution
  │   ├── data_ingestion/
  │   ├── data_validation/
  │   ├── data_transformation/
  │   ├── model_trainer/
  │   └── model_evaluation/
  │
  ├── research/               # Experimental notebooks for testing modules
  └── logs/                   # Runtime logs and error tracking

setup_instructions:
  - "1️⃣ Create and activate virtual environment:"
  - "python -m venv .venv"
  - ".\\.venv\\Scripts\\activate"
  - "2️⃣ Install dependencies:"
  - "pip install -r requirements.txt"
  - "3️⃣ Ensure dataset file exists at:"
  - "artifacts/data_ingestion/airplane1.csv"

run_instructions: |
  Run the complete ML pipeline (Ingestion → Validation → Transformation → Training → Evaluation):
  ```bash
  python main.py
