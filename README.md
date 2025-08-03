# MLflow Machine Learning Experiment Tracking

## Project Status
**This project is currently under development and not yet complete.**

## Overview
This project demonstrates the implementation of machine learning experiments using MLflow for comprehensive experiment tracking and model management. The project structure is organized to support multiple experimental iterations with complete tracking of metrics, parameters, artifacts, and model versions.

## Project Structure
```
project/            
├── notebooks/
│   ├── 1_Preprocessing_&_EDA.ipynb     # Data preprocessing and exploratory analysis
│   ├── 2_experiment_1_baseline_model.ipynb  # Baseline model experiment
│   ├── 3_experiment_2.ipynb           # Second experiment iteration
│   ├── 4_experiment_3.ipynb           # Third experiment iteration
│   └── 5_experiment_4.ipynb           # Fourth experiment iteration
└── requirements.txt       # Project dependencies
```

## MLflow Experiment Tracking
```
├── mlflow_logs/           # MLflow experiment tracking database
│   ├── 0/                 # Default experiment
│   ├── 147337520425050598/
│   ├── 300921718200322684/
│   ├── 860794644769138398/
│   ├── 957923626761089126/
│   └── models/            # Registered model artifacts
```
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

## Accessing MLflow Logs

### Download from Google Drive
The MLflow tracking is available at:
[MLflow Logs - Google Drive](https://drive.google.com/drive/folders/1YJP3wNBcTx65KjdBwP8PlxtRpQUTD_JO?usp=sharing)

To use the logs:
1. Download the `mlflow_logs` folder from the Google Drive link
2. Place it in your project root directory
3. Follow the "Viewing Experiment Results" section below

## Getting Started

### Prerequisites
- Python 3.7+
- Virtual environment (recommended)

### Installation
1. Clone the repository
2. Download MLflow logs from the Google Drive link above
3. Create and activate virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
4. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Viewing Experiment Results
To access the MLflow UI and view all experiments, metrics, and artifacts:

```bash
# Navigate to project directory
cd /path/to/your/project

# Start MLflow UI
mlflow ui --backend-store-uri mlflow_logs --port 5001
```

Then navigate to `http://localhost:5001` in your browser to explore:
- Experiment comparisons
- Metric visualizations  
- Model artifacts
- Parameter tuning results
- Model performance charts

### Alternative MLflow Commands
```bash
# View experiments in default location
mlflow ui

# Use different port
mlflow ui --port 8080

# Specify host for network access
mlflow ui --host 0.0.0.0 --port 5001
```

## Experiment Details

### Key Metrics Tracked
- Accuracy
- Precision, Recall, F1-Score
- ROC-AUC
- Training/Validation Loss
- Model Training Time
- Feature Importance Scores

## Development Environment
This project was developed using Google Colab for model training and experimentation, with MLflow providing local experiment tracking and artifact storage.

## Best Practices Implemented
- **Reproducible Experiments**: All random seeds and environment configurations tracked
- **Version Control**: Model versions managed through MLflow Model Registry
- **Artifact Management**: Complete model artifacts, plots, and data artifacts stored
- **Parameter Tracking**: Comprehensive hyperparameter logging
- **Performance Monitoring**: Multi-metric evaluation across experiments

## Troubleshooting

### Common Issues
1. **MLflow UI not loading**: Ensure the `mlflow_logs` directory is in the correct location
2. **Port conflicts**: Use `--port` flag to specify different port
3. **Missing artifacts**: Verify all artifact files were downloaded from Google Drive

### Useful MLflow Commands
```bash
# List all experiments
mlflow experiments list --tracking-uri mlflow_logs

# Search runs with specific metrics
mlflow runs list --experiment-id <experiment_id>

# Export experiment data
mlflow experiments csv -x <experiment_id> -o results.csv
```

## Contributing
This project is currently in active development. Contributions and suggestions are welcome.

## License
This project is for educational and research purposes.

## Contact
For questions about the experiments or accessing the data, please open an issue in this repository.
