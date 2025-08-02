# Ev-Vehicle-charging-demand-prediction

## Overview
A machine learning project to forecast Electric Vehicle (EV) adoption rates across Washington State counties. Uses historical DOL registration data to predict future EV adoption trends and support infrastructure planning.

## Quick Start
```bash
# Clone repository
git clone https://github.com/yourusername/ev-adoption-forecast.git

# Create virtual environment
python -m venv .venv
.\.venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run Streamlit app
streamlit run app.py
```

## Dependencies
```txt
numpy==1.26.4
pandas==1.5.3
scikit-learn==1.6.1
matplotlib==3.7.1
seaborn==latest
joblib==1.3.1
streamlit==1.44.1
```

## Project Structure
```
PROJECT_EV/
├── .venv/                         # Virtual environment
├── app.py                         # Streamlit web application
├── EV_Adoption_Forecasting.ipynb  # Main development notebook
├── requirements.txt               # Package dependencies
├── Electric_Vehicle_Population_By_County.csv
├── preprocessed_ev_data.csv       # Processed dataset
├── forecasting_ev_model.pkl       # Trained model
└── README.md
```

## Dataset
- Source: Washington State DOL
- Time Period: 2017-2024
- Features: 10 columns including:
  - Date
  - County
  - Vehicle types (BEV, PHEV)
  - Total registrations
  - [Download Link](https://www.kaggle.com/datasets/sahirmaharajj/electric-vehicle-population-size-2024/data)

## Features
- County-wise EV adoption forecasting
- Interactive Streamlit dashboard
- 3-year prediction horizon
- Visualization of historical and forecast trends
- Top county analysis

## Model Details
- Algorithm: Random Forest Regressor
- Features: 9 engineered features including lag indicators
- Performance Metrics: R², MAE, RMSE
- Cross-validation: 3-fold

## Usage
1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Prepare data:
```python
python data_preprocessing.py
```

3. Run Streamlit app:
```bash
streamlit run app.py
```

## Results
- Successfully forecasted EV adoption for Washington State counties
- Identified leading adoption regions
- 13.8% CAGR projected (2024-2032)
- Top predictive features: 2-month lag, growth slope

## Contributing
1. Fork the repository
2. Create feature branch
3. Commit changes
4. Push to branch
5. Create Pull Request
