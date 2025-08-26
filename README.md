# Supplement Sales Revenue Prediction using XGBoost

This project implements a regression model using XGBoost to predict supplement sales revenue based on various product and marketing features, achieving 99.94% R² accuracy.

## 🎯 Project Objective
To predict supplement sales revenue using product characteristics, pricing, discount information, and sales platform data to enable better inventory management and sales forecasting.

## 📊 Dataset Information
- **Source**: Supplement Sales Weekly Expanded Dataset
- **Size**: 4,384 observations × 10 features
- **Target Variable**: Revenue (continuous)
- **Time Period**: Weekly sales data spanning multiple years
- **Data Quality**: No missing values detected

### Features Overview
- **Product Information**: Product Name, Category (Protein, Vitamin, Omega, Performance)
- **Sales Metrics**: Units Sold, Price, Revenue, Units Returned
- **Marketing**: Discount percentage
- **Distribution**: Location (Canada, UK), Platform (Amazon, Walmart, iHerb)
- **Temporal**: Date information

## 🔧 Technologies Used
```python
pandas==1.5.0
numpy==1.23.0
xgboost==1.7.0
scikit-learn==1.1.0
matplotlib==3.6.0
seaborn==0.12.0
```

## 📈 Model Performance Results

### XGBoost Regressor Metrics:
- **R² Score**: 99.94% (Exceptional accuracy)
- **Mean Absolute Error (MAE)**: 36.74
- **Mean Squared Error (MSE)**: 2,800.85
- **Root Mean Squared Error (RMSE)**: 52.92

### Performance Analysis
The model demonstrates exceptional predictive capability with R² = 0.9994, indicating it explains 99.94% of the variance in supplement sales revenue.

## 🔍 Feature Importance Analysis
Top predictive features identified by XGBoost:
1. **Units Sold**: Primary driver of revenue (as expected)
2. **Price**: Strong correlation with revenue generation
3. **Product Category**: Different supplement types show varying sales patterns
4. **Platform**: Sales channel significantly impacts revenue
5. **Location**: Geographic factors influence purchasing behavior

## 🛠️ Data Preprocessing
- **Categorical Encoding**: One-hot encoding for Category, Location, Platform
- **Feature Selection**: Removed non-predictive columns (Date, Product Name)
- **Train-Test Split**: 80-20 ratio (3,507 training, 877 testing samples)
- **Missing Values**: None detected in the dataset

## 🚀 Installation & Usage

### Requirements
```bash
pip install pandas numpy xgboost scikit-learn matplotlib seaborn jupyter
```

### Data Download
Download from Kaggle:
```bash
kaggle datasets download -d zahidmughal2343/supplement-sales-data 
```

### Execution
```bash
jupyter notebook predicting-supplement-sales-revenue-using-xgboost.ipynb
```

## 📊 Dataset Statistics
- **Revenue Range**: $1,284 - $10,762 (Mean: $5,227)
- **Units Sold Range**: 103 - 194 units (Mean: 150)
- **Price Range**: $10.00 - $59.97 (Mean: $34.78)
- **Discount Range**: 0% - 25% (Mean: 12.4%)
- **Return Rate**: 0-8 units (Mean: 1.5 units)

## 🎯 Key Insights
1. **Strong Revenue Predictability**: XGBoost effectively captures revenue patterns
2. **Units Sold Dominance**: Primary factor in revenue determination
3. **Category Performance**: Different supplement types show distinct sales patterns
4. **Platform Impact**: Sales channels significantly influence revenue outcomes
5. **Geographic Variations**: Location-based purchasing patterns identified

## 💼 Business Applications
- **Sales Forecasting**: Predict future revenue streams
- **Inventory Management**: Optimize stock levels based on predicted demand
- **Pricing Strategy**: Understand price-revenue relationships
- **Platform Optimization**: Identify best-performing sales channels
- **Product Portfolio**: Analyze category-wise performance

## 🔬 Model Characteristics
- **Algorithm**: XGBoost Regressor (Gradient Boosting)
- **Hyperparameters**: Default settings with random_state=42
- **Training Time**: Fast convergence on this dataset size
- **Prediction Speed**: Real-time inference capability

## ⚠️ Model Considerations
The extremely high R² score (99.94%) suggests:
- Strong linear relationships between features and target
- Possible data leakage (investigate further if deploying)
- Excellent model fit for current dataset characteristics
- May require validation on new, unseen data

## 🚀 Future Improvements
- Cross-validation for robust performance assessment
- Hyperparameter tuning using GridSearch/RandomSearch
- Feature engineering (seasonality, interaction terms)
- Model ensemble with Random Forest/Linear Regression
- Time series analysis for temporal patterns

## 📈 Production Deployment
For business use:
- Validate on recent sales data
- Monitor model drift over time
- Implement A/B testing for predictions
- Add confidence intervals for predictions

## 👤 Developer
- **Kaggle**: [@kurkigal](https://www.kaggle.com/kurkigal)

## 📄 License
MIT License

## 🤝 Contributing
Contributions welcome! Focus areas:
- Time series forecasting components
- Advanced feature engineering
- Model interpretability enhancements

---
⭐ If this project helps your sales forecasting needs, please consider starring it!