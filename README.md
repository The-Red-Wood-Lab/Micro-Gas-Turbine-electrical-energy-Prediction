# Micro Gas Turbine Electrical Energy Prediction Using XGBoost

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Data](#data)
- [Results](#results)

## Project Overview
This project implements a machine learning pipeline for predicting electrical power using the XGBoost algorithm. The model takes voltage and time as input features to predict electrical power output. The implementation includes hyperparameter optimization to enhance model performance.

## Features
- Data loading from CSV files
- Data preprocessing, including handling missing values
- Feature scaling using `StandardScaler`
- Hyperparameter optimization with `RandomizedSearchCV`
- Model evaluation metrics: R² score, RMSE, and MAE
- Visualizations of learning curves and predictions vs. actual values

## Installation
To set up the project, you need Python and the required libraries. You can create a virtual environment and install the dependencies using pip:

```bash
# Create a virtual environment
python -m venv env

# Activate the virtual environment
# On Windows
.\env\Scripts\activate
# On macOS/Linux
source env/bin/activate

# Install required libraries
pip install pandas numpy matplotlib seaborn scikit-learn xgboost scipy
```

## Usage
1. Place your datasets in the `Dataset/Merged_dataset/` directory, ensuring the filenames are `merged_file.csv` for training data and `test_merged_file.csv` for test data.
2. Run the script to train the model and evaluate its performance:

```bash
python your_script_name.py
```

3. After execution, the model's evaluation metrics and visualizations will be displayed.

## Data
The project uses the following datasets:
- **Training Data**: `merged_file.csv` - Contains time, voltage, and electrical power data.
- **Test Data**: `test_merged_file.csv` - Contains similar features for evaluation.

Ensure that the datasets are preprocessed correctly before using them in the model.

## Results
- **Learning Rate**: The optimized learning rate found during hyperparameter tuning is [0.12538077692527183].
- **Validation R² Score**: 0.8409
- **Validation RMSE**: 289.1317
- **Test R² Score**: 0.8048
- **Test RMSE**: 326.9103
- **Test MAE**: 198.9039
