# Airbnb Dynamic Pricing Engine

## Overview
The **Airbnb Dynamic Pricing Engine** is an end-to-end Machine Learning web application designed to predict the optimal price for Airbnb listings. Built with Flask, it uses a trained machine learning model to estimate property prices dynamically based on various features such as property type, location, amenities, and host details.

## Features
- **Dynamic Price Prediction:** Predicts property prices in real-time based on multiple input variables.
- **Web Interface:** A user-friendly web interface powered by Flask, allowing users to input property details easily.
- **Machine Learning Models:** Utilizes powerful ML algorithms like CatBoost, XGBoost, and Scikit-Learn.
- **Modular Codebase:** Organizes data processing and prediction logic into pipelines (`src/Airbnb/pipelines/Prediction_Pipeline.py`).

## Tech Stack
- **Backend Framework:** Flask
- **Machine Learning:** Scikit-Learn, CatBoost, XGBoost, Numpy, Pandas
- **Visualization/Analysis:** Seaborn, Pillow
- **Data Version Control:** DVC
- **Frontend:** HTML/CSS (Jinja2 Templates)

## Getting Started

### Prerequisites
- Python 3.8+
- pip (Python package manager)

### Installation
1. Clone the repository:
   ```bash
   git clone <your-repository-url>
   cd Airbnb Dynamic Pricing Engine
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
   Or install as a local package:
   ```bash
   pip install -e .
   ```

### Running the Application
1. Start the Flask server:
   ```bash
   python app.py
   ```

2. Open your web browser and navigate to:
   ```
   http://127.0.0.1:8080/
   ```

## Input Features
The model requires the following features to make a prediction:
- Property Type & Room Type
- Amenities & Accommodates
- Bathrooms, Bedrooms, and Beds
- Cancellation Policy
- Cleaning Fee
- City, Latitude, & Longitude
- Host details (Profile Pic, Identity Verified, Response Rate)
- Instant Bookable
- Number of Reviews & Review Scores Rating

## Project Structure
```
├── app.py                     # Main Flask application
├── requirements.txt           # Project dependencies
├── setup.py                   # Package setup
├── src/                       # Core application logic
│   └── Airbnb/
│       └── pipelines/         # Prediction and Training pipelines
├── static/                    # CSS, JS, and Images for the web app
├── templates/                 # HTML templates (index.html, error.html)
├── Notebook_Experiments/      # Jupyter notebooks for EDA and model training
├── Artifacts/                 # Model and preprocessor artifacts
└── logs/                      # Application logs
```

