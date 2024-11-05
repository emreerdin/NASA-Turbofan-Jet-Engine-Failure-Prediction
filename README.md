
# NASA Turbofan Jet Engine Failure Prediction

This project involves predicting the Remaining Useful Life (RUL) of jet engines using the NASA C-MAPSS (Commercial Modular Aero-Propulsion System Simulation) dataset. The aim is to develop a predictive model that helps in estimating the time until an engine fails, which is crucial for effective maintenance and operational safety.

## Project Overview

The NASA C-MAPSS dataset provides operational sensor data and settings from a simulated fleet of aircraft engines under various operating conditions and fault modes. The project focuses on preprocessing the data, feature selection, building a regression model, and evaluating its performance.

### Key Objectives
- Preprocess the data for model readiness, including handling duplicates and null values.
- Perform feature engineering and selection to enhance model accuracy.
- Train a predictive model to estimate the RUL of jet engines.
- Evaluate model performance using metrics such as RMSE (Root Mean Squared Error).

## Dataset

### Source
The dataset used is the NASA C-MAPSS dataset, which consists of:
- **Training data** (`train_FD001`, `train_FD002`, etc.): Engine operation records with known RUL.
- **Test data** (`test_FD001`, `test_FD002`, etc.): Engine operation data for model evaluation.
- **RUL files** (`RUL_FD001`, `RUL_FD002`, etc.): Actual RUL values for the engines in the test set.

### Data Columns
- **Engine ID**: Identifier for each engine.
- **Cycle**: Time unit indicating the operational cycle of the engine.
- **Operational Settings**: Parameters that affect engine performance (e.g., `OperationalSetting1`, `OperationalSetting2`).
- **Sensor Readings**: Measurements from various engine sensors (e.g., temperature, pressure).

## Project Workflow

### 1. Data Preprocessing
- **Duplicate Removal**: Applied techniques to ensure no redundant data points skew the analysis.
- **Feature Scaling**: Normalized sensor readings for consistency.
- **Missing Values**: Checked for and handled any missing data.

### 2. Feature Engineering
- **Correlation Analysis**: Evaluated relationships between features to retain relevant variables.
- **Rolling Averages and Trend Calculations**: Created new features to capture patterns over cycles.

### 3. Model Development
- **Modeling Approach**: Implemented regression models (e.g., XGBoost, Random Forest) to predict RUL.
- **Hyperparameter Tuning**: Optimized the models for better accuracy.

### 4. Evaluation Metrics
- **RMSE**: Used to evaluate the prediction accuracy.
- **Heatmaps and Visuals**: Employed visual tools to assess feature importance and model diagnostics.

## Challenges Faced

- **High RMSE Values**: Initial models showed an RMSE of around 35, indicating room for further improvement.
- **Non-correlated Features**: Some operational settings did not show correlation in heatmaps, prompting further investigation.

## Results and Insights

- The trained models were able to provide a reasonable prediction of RUL, though there is scope for further tuning and feature engineering.
- Visualizations helped identify key features influencing the prediction accuracy.

## Future Work

- **Advanced Model Exploration**: Investigating other machine learning techniques like neural networks for better performance.
- **Feature Enrichment**: Adding domain-specific features based on further exploration of sensor data.

## Getting Started

### Prerequisites
- Python 3.x
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `xgboost`

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/emreerdin/NASA-Turbofan-Jet-Engine-Failure-Prediction.git
   cd NASA-Turbofan-Jet-Engine-Failure-Prediction
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Run the Project
1. Preprocess the data using the provided scripts.
2. Train and evaluate the model by running the `train_model.py` script.

   ```bash
   python train_model.py
   ```

## Author

**Emre Erdin**  
*Software Engineer & Data Enthusiast*

For questions or collaborations, please contact [Emre's GitHub](https://github.com/emreerdin).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
