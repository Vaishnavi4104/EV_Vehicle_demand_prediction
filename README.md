# 🔮 EV Vehicle Demand Prediction

A machine learning-powered web application that forecasts electric vehicle (EV) adoption trends for counties in Washington State. This project helps urban planners and policymakers anticipate infrastructure needs by predicting future EV adoption based on historical data.

![EV Forecast Dashboard](ev-car-factory.jpg)

## 🚀 Features

- **Interactive Forecasting**: Predict EV adoption for the next 3 years for any county in Washington State
- **Multi-County Comparison**: Compare adoption trends across up to 3 counties simultaneously
- **Real-time Visualizations**: Dynamic charts showing historical data and future predictions
- **Growth Analysis**: Percentage growth calculations and trend analysis
- **User-friendly Interface**: Beautiful Streamlit web application with modern UI

## 📊 Dataset

The application uses the **Electric Vehicle Population Size History by County** dataset from Washington State Department of Licensing (DOL), containing:

- **Date Range**: 2017-01-31 to 2024-02-29
- **Geographic Coverage**: All counties in Washington State
- **Vehicle Types**: Battery Electric Vehicles (BEVs) and Plug-in Hybrid Electric Vehicles (PHEVs)
- **Key Metrics**: 
  - Electric Vehicle Total (BEVs + PHEVs)
  - Non-Electric Vehicle Total
  - Total Vehicles
  - Percent Electric Vehicles

## 🛠️ Technology Stack

- **Frontend**: Streamlit (Python web framework)
- **Backend**: Python 3.x
- **Machine Learning**: 
  - Random Forest Regressor
  - Scikit-learn
  - NumPy & Pandas
- **Data Visualization**: Matplotlib
- **Model Persistence**: Joblib

## 📋 Prerequisites

- Python 3.7 or higher
- pip (Python package installer)

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Vaishnavi4104/EV_Vehicle_demand_prediction.git
   
   ```

2. **Install dependencies**
   ```bash
   pip install -r reqirements.txt
   ```

3. **Run the application**
   ```bash
   streamlit run app.py
   ```

4. **Access the application**
   Open your browser and navigate to `http://localhost:8501`

## 📈 How It Works

### Data Preprocessing
- Historical EV data is loaded and preprocessed
- Feature engineering creates lag variables, rolling means, and growth metrics
- County encoding for categorical variables

### Model Training
- Random Forest Regressor trained on historical data
- Features include:
  - Lag variables (1, 2, 3 months)
  - Rolling means
  - Percentage changes
  - Growth slopes
  - County encoding

### Forecasting Process
1. User selects a county from the dropdown
2. System loads historical data for the selected county
3. Model generates 36-month forecast (3 years)
4. Results are visualized with interactive charts
5. Growth percentages and trends are calculated

## 🎯 Key Features Explained

### Single County Forecasting
- Select any county in Washington State
- View historical EV adoption trends
- See 3-year forecast with confidence intervals
- Analyze growth percentages and trends

### Multi-County Comparison
- Compare up to 3 counties simultaneously
- Side-by-side trend analysis
- Growth rate comparisons
- Identify high-growth vs. low-growth regions

### Interactive Visualizations
- Cumulative EV adoption charts
- Historical vs. forecasted data
- Color-coded trends (increase/decrease)
- Responsive design for all screen sizes

## 📁 Project Structure

```
ev-vehicle-demand-prediction/
├── app.py                              # Main Streamlit application
├── EV_Vehicle_demand_prediction (1).ipynb  # Jupyter notebook with model training
├── forecasting_ev_model.pkl            # Trained Random Forest model
├── preprocessed_ev_data.csv           # Preprocessed dataset
├── Electric_Vehicle_Population_Size_History_By_County_.csv  # Raw dataset
├── ev-car-factory.jpg                 # Project banner image
├── reqirements.txt                    # Python dependencies
└── README.md                          # This file
```

## 🔧 Model Details

### Algorithm: Random Forest Regressor
- **Advantages**: Handles non-linear relationships, robust to outliers
- **Features**: 8 engineered features from historical data
- **Performance**: Optimized using RandomizedSearchCV
- **Persistence**: Model saved using joblib for fast loading

### Feature Engineering
- `ev_total_lag1/2/3`: Previous month EV counts
- `ev_total_roll_mean_3`: 3-month rolling average
- `ev_total_pct_change_1/3`: Percentage changes
- `ev_growth_slope`: Linear growth trend
- `county_encoded`: Encoded county identifiers

## 📊 Sample Output

The application provides:
- **Cumulative EV Forecast Charts**: Historical + 3-year predictions
- **Growth Analysis**: Percentage increase/decrease over forecast period
- **Multi-county Comparisons**: Side-by-side trend analysis
- **Interactive Elements**: Dropdown selections, real-time updates

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## 🙏 Acknowledgments

- **Dataset Source**: Washington State Department of Licensing (DOL)
- **Kaggle Dataset**: [Electric Vehicle Population Size History by County](https://www.kaggle.com/datasets/sahirmaharajj/electric-vehicle-population-size-2024/data)
- **Streamlit**: For the beautiful web framework
- **Scikit-learn**: For the machine learning capabilities

## 📞 Contact

- **Project Link**: [ https://github.com/Vaishnavi4104/EV_Vehicle_demand_prediction.git]( https://github.com/Vaishnavi4104/EV_Vehicle_demand_prediction.git)

## 🔮 Future Enhancements

- [ ] Add more sophisticated time series models (ARIMA, Prophet)
- [ ] Include additional features (population, income, charging stations)
- [ ] Real-time data updates
- [ ] Export functionality for reports
- [ ] Mobile-responsive design improvements
- [ ] API endpoints for programmatic access

---

⭐ **Star this repository if you find it helpful!** 