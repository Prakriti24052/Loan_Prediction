##Loan Prediction API

#Overview
The Loan Prediction API is a machine learning-powered FastAPI application that predicts loan approval outcomes based on input financial parameters. The API preprocesses input data using a pre-trained scaler and applies a trained model to make predictions.

#Features
Accepts five numerical financial parameters as input.
Utilizes a pre-trained scaler for input normalization.
Applies a machine learning model to predict loan approval status.
Provides a RESTful endpoint for making predictions.

#Installation

Prerequisites
Ensure you have Python installed (Python 3.7 or later recommended). You also need pip for package management.

Clone the Repository
git clone <repository_url>
cd loan-prediction-api

Install Dependencies

pip install -r requirements.txt

Required Files

Ensure that Scaler.pkl and model.pkl are present in the project directory.

Usage

Running the API

Start the FastAPI server:

uvicorn app:app --host 127.0.0.1 --port 8000

Making Predictions

Send a POST request to http://127.0.0.1:8000/predict/ with JSON input in the following format:

{
  "x1": 1000.5,
  "x2": 500,
  "x3": 750,
  "x4": 5,
  "x5": 2
}

The API will respond with:

{
  "prediction": 1
}

where 1 indicates loan approval and 0 indicates rejection.

File Structure

loan-prediction-api/
│── app.py  # FastAPI application
│── loan_data.csv  # Dataset used for training
│── Scaler.pkl  # Pre-trained scaler
│── model.pkl  # Trained machine learning model
│── requirements.txt  # Dependencies

Dependencies

FastAPI

Uvicorn

NumPy

Joblib

Pydantic

You can install dependencies using:# Loan_Prediction
