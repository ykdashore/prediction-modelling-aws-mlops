# Restaurant Revenue Prediction

This project aims to predict restaurant revenue based on various features using machine learning models. It involves downloading a dataset from Kaggle, preprocessing it, training models, and deploying the models to AWS S3 for future predictions.

## Requirements

- Python 3.x
- `boto3`
- `joblib`
- `numpy`
- `pandas`
- `scikit-learn`
- `xgboost`
- `logging`

## Setup

1. **Install Dependencies**  
   Ensure you have all the required Python packages installed. You can install them using pip:

   ```bash
   pip install boto3 joblib numpy pandas scikit-learn xgboost

## Kaggle API Key

Place your Kaggle API key in the appropriate location (`~/.kaggle/kaggle.json`).

## Usage

1. **Download the Dataset**

   The script automatically downloads the dataset from Kaggle using the Kaggle API.

2. **Load and Preprocess Data**

   The data is loaded from a CSV file and preprocessed, including handling missing values and scaling features.

3. **Train Models**

   The script trains two models:
   - Random Forest Regressor
   - XGBoost Regressor

4. **Evaluate Models**

   Models are evaluated based on Mean Squared Error (MSE) and the results are logged.

5. **Save Models and Preprocessor to S3**

   The trained models and preprocessor are saved to an AWS S3 bucket.

6. **Load Models and Preprocessor from S3**

   The saved models and preprocessor can be loaded from S3 for making predictions.

7. **Make Predictions**

   Example data is used to make predictions using the loaded models. Results are logged and printed.

## Logging

All major actions and errors are logged to `app.log`.

## AWS S3 Configuration

Update the `S3_BUCKET` and `S3_PREFIX` variables to match your S3 bucket and desired prefix.



