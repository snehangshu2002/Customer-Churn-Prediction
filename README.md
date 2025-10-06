# Telco Customer Churn Prediction System

A comprehensive machine learning application for predicting customer churn using Streamlit.

## Features

### 🎯 Three Prediction Modes

1. **Single Customer Prediction**
   - Interactive form to input individual customer details
   - Real-time churn probability prediction
   - Visual gauge chart showing risk level
   - Actionable recommendations

2. **Batch Prediction**
   - Upload CSV files with multiple customers
   - Bulk predictions with downloadable results
   - Summary statistics and visualizations
   - Risk level categorization (Low/Medium/High)

3. **Data Exploration**
   - Interactive visualizations of the dataset
   - Churn rate analysis by various features
   - Correlation heatmaps
   - Distribution plots

### 🤖 Multiple ML Models

- **Logistic Regression**: Fast, interpretable baseline model
- **Random Forest**: Ensemble method for robust predictions
- **XGBoost**: Advanced gradient boosting for high accuracy

### 📊 Visualizations

- Gauge charts for churn probability
- Pie charts for churn distribution
- Histograms for probability distributions
- Scatter plots for feature relationships
- Bar charts for categorical analysis
- Correlation heatmaps

## Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Setup

1. **Clone or navigate to the project directory:**
   ```bash
   cd c:/Users/SNEHANGSHU/Desktop/Internship
   ```

2. **Create a virtual environment (recommended):**
   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment:**
   - Windows:
     ```bash
     venv\Scripts\activate
     ```
   - Mac/Linux:
     ```bash
     source venv/bin/activate
     ```

4. **Install required packages:**
   ```bash
   pip install -r requirements.txt
   ```

## Running the Application

1. **Ensure you're in the project directory:**
   ```bash
   cd c:/Users/SNEHANGSHU/Desktop/Internship
   ```

2. **Run the Streamlit app:**
   ```bash
   streamlit run app.py
   ```

3. **The app will automatically open in your default browser at:**
   ```
   http://localhost:8501
   ```

## Usage Guide

### Single Customer Prediction

1. Select "Single Customer Prediction" from the sidebar
2. Choose your preferred ML model
3. Adjust the churn probability threshold if needed
4. Fill in the customer details in the form:
   - **Demographics**: Gender, Senior Citizen status, Partner, Dependents
   - **Services**: Phone, Internet, and additional services
   - **Account Info**: Tenure, Contract type, Billing, Payment method, Charges
5. Click "Predict Churn" to see results
6. Review the gauge chart and risk assessment
7. Read the recommendations for customer retention

### Batch Prediction

1. Select "Batch Prediction" from the sidebar
2. Choose your preferred ML model
3. Upload a CSV file with customer data
   - File should have the same columns as the training data
   - See `WA_Fn-UseC_-Telco-Customer-Churn.csv` for format reference
4. Click "Predict Churn for All Customers"
5. Review the summary statistics and visualizations
6. Filter results by risk level or churn prediction
7. Download the results as CSV for further analysis

### Data Exploration

1. Select "Data Exploration" from the sidebar
2. View dataset overview and statistics
3. Explore various visualizations:
   - Churn distribution
   - Tenure analysis
   - Monthly vs Total charges
   - Contract type impact
   - Internet service analysis
   - Feature correlations
4. Use insights to understand churn patterns

## File Structure

```
Internship/
│
├── app.py                                    # Main Streamlit application
├── customer.ipynb                            # Jupyter notebook with model training
├── WA_Fn-UseC_-Telco-Customer-Churn.csv     # Dataset
│
├── Logistic_churn_model.pkl                 # Trained Logistic Regression model
├── random_forest_churn_model.pkl            # Trained Random Forest model
├── xgboost_churn_model.pkl                  # Trained XGBoost model
│
├── requirements.txt                          # Python dependencies
└── README.md                                 # This file
```

## Model Information

### Training Data
- **Dataset**: Telco Customer Churn Dataset
- **Samples**: ~7,000 customers
- **Features**: 19 customer attributes
- **Target**: Binary classification (Churn: Yes/No)

### Features Used
- **Demographics**: Gender, Senior Citizen, Partner, Dependents
- **Services**: Phone Service, Multiple Lines, Internet Service, Online Security, Online Backup, Device Protection, Tech Support, Streaming TV, Streaming Movies
- **Account**: Tenure, Contract, Paperless Billing, Payment Method, Monthly Charges, Total Charges

### Model Performance
Models are evaluated using:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

## Customization

### Adjusting Threshold
- Use the sidebar slider to adjust the churn probability threshold
- Default: 0.5 (50%)
- Lower threshold: More sensitive (catches more potential churners)
- Higher threshold: More specific (focuses on high-risk customers)

### Model Selection
- Switch between models in the sidebar
- Compare predictions across different algorithms
- Choose based on your priority (speed vs accuracy)

## Troubleshooting

### Common Issues

1. **Models not loading:**
   - Ensure all `.pkl` files are in the same directory as `app.py`
   - Check that models were trained and saved correctly

2. **CSV upload errors:**
   - Verify CSV format matches the training data
   - Check for missing columns or incorrect column names
   - Ensure numeric fields contain valid numbers

3. **Prediction errors:**
   - Make sure all required fields are filled
   - Check for data type mismatches
   - Verify categorical values match expected options

4. **Port already in use:**
   ```bash
   streamlit run app.py --server.port 8502
   ```

## Tips for Best Results

1. **For Single Predictions:**
   - Provide accurate customer information
   - Pay special attention to tenure, contract type, and charges
   - Consider the customer's service usage patterns

2. **For Batch Predictions:**
   - Ensure data quality before upload
   - Remove or handle missing values
   - Use consistent formatting across all records

3. **Interpreting Results:**
   - Probability > 70%: High risk, immediate action needed
   - Probability 30-70%: Medium risk, monitor closely
   - Probability < 30%: Low risk, maintain service quality

## Future Enhancements

- [ ] Add SHAP values for model explainability
- [ ] Include feature importance visualization
- [ ] Add model comparison dashboard
- [ ] Implement A/B testing for retention strategies
- [ ] Add customer segmentation analysis
- [ ] Include time-series analysis for churn trends

## Support

For issues or questions:
1. Check the troubleshooting section
2. Review the usage guide
3. Examine the Jupyter notebook for model details

## License

This project is for educational and demonstration purposes.

## Acknowledgments

- Dataset: IBM Sample Data Sets
- Framework: Streamlit
- ML Libraries: scikit-learn, XGBoost
- Visualization: Plotly

---

**Built with ❤️ using Streamlit and Machine Learning**
