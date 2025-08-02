# MLflow Machine Learning Experiment Tracking

## Project Status
**This project is currently under development and not yet complete.**

## Overview
This project demonstrates the implementation of machine learning experiments using MLflow for comprehensive experiment tracking and model management. The project structure is organized to support multiple experimental iterations with complete tracking of metrics, parameters, artifacts, and model versions.

## Project Structure
```
project/             
├── mlflow_logs/           # MLflow experiment tracking database
│   ├── 0/                 # Default experiment
│   ├── 147337520425050598/
│   ├── 300921718200322684/
│   ├── 860794644769138398/
│   ├── 957923626761089126/
│   └── models/            # Registered model artifacts
├── notebooks/
│   ├── 1_Preprocessing_&_EDA.ipynb     # Data preprocessing and exploratory analysis
│   ├── 2_experiment_1_baseline_model.ipynb  # Baseline model experiment
│   ├── 3_experiment_2.ipynb           # Second experiment iteration
│   ├── 4_experiment_3.ipynb           # Third experiment iteration
│   └── 5_experiment_4.ipynb           # Fourth experiment iteration
└── requirements.txt       # Project dependencies
```

## MLflow Experiment Tracking
The `mlflow_logs` directory contains comprehensive tracking data for all experiments including:

- **Metrics**: Performance metrics, loss values, accuracy scores
- **Parameters**: Model hyperparameters, training configurations
- **Artifacts**: 
  - Trained model files
  - Data preprocessing pipelines
  - Visualizations and plots
  - Feature importance charts
  - Model performance graphs
- **Model Registry**: Versioned models with staging information

## Getting Started

### Prerequisites
- Python 3.7+
- Virtual environment (recommended)

### Installation
1. Clone the repository
2. Create and activate virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Viewing Experiment Results
To access the MLflow UI and view all experiments, metrics, and artifacts:

```bash
mlflow ui --backend-store-uri mlflow_logs --port 5001
```

Then navigate to `http://localhost:5001` in your browser to explore:
- Experiment comparisons
- Metric visualizations
- Model artifacts
- Parameter tuning results
- Model performance charts

## Development Environment
This project was developed using Google Colab for model training and experimentation, with MLflow providing local experiment tracking and artifact storage.

## Features
- Complete experiment lifecycle tracking
- Model versioning and registry
- Automated artifact logging
- Performance metric visualization
- Hyperparameter comparison
- Reproducible experiment setup

## Contributing
This project is currently in active development. Contributions and suggestions are welcome.

## License
This project is for educational and research purposes.