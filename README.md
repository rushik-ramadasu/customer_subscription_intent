# AI-Powered Marketing Optimization System

**Live Demo:** [https://customer-subscription-intent.streamlit.app/](https://customer-subscription-intent.streamlit.app/)

An intelligent web application that predicts customer subscription intent by forecasting monthly conversion rates using a time-series regression model enhanced with external indicators. This multi-level prediction system handles time-level forecasting, customer-level prediction, and campaign-level analysis, presented through an interactive Streamlit dashboard.

## Features

- **Data Generation & Processing**: Robust synthetic dataset generation representing time-series trends, customer demographics, and campaign interaction records.
- **Customer Segmentation**: K-Means clustering to identify distinct customer behavioral segments.
- **Predictive Modeling**: Uses XGBoost for precise customer-level conversion probabilities.
- **Time-Series Forecasting**: Incorporates Facebook Prophet to predict future trends and seasonality in marketing campaigns.
- **Interactive Dashboard**: A dynamic Streamlit interface that enables business users to monitor KPIs, analyze segment behavior, and run marketing scenarios.

## Project Structure

```text
├── data/                                 # Generated marketing datasets
│   └── synthetic_marketing_data.csv
├── models/                               # Pre-trained models and scalers
│   ├── features.txt
│   ├── kmeans.joblib
│   ├── prophet_model.pkl
│   ├── scaler.joblib
│   └── xgb_model.joblib
├── data_generator.py                     # Script to generate synthetic datasets
├── implementation_plan.md                # System outline and architecture
├── marketing_optimization.py             # Core data processing & engineering
├── README.md                             # Project documentation
├── requirements.txt                      # Project dependencies
├── streamlit_app.py                      # Main entry point for Streamlit dashboard
└── subscription_model.py                 # Core model inference logic
```
## Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/rushik-ramadasu/mini-project.git
   cd mini-project
   ```

2. **Set up a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run Data Generation (optional):**
   The repository already includes trained models and data. If you wish to regenerate the synthetic dataset and retrain the models from scratch, run:
   ```bash
   python data_generator.py
   ```

5. **Start the Streamlit Application:**
   ```bash
   streamlit run streamlit_app.py
   ```

## Usage

Once the application is running, open your browser to the URL provided in the terminal (usually `http://localhost:8501`). You can navigate through different dashboard sections to view overview metrics, model performance, and customer segmentation insights.
