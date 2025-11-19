# Cambridge Energy Use Prediction

**CSCI E-109a Group Project**

**Authors:** Jie Zhao, Michael Assmus, Mohanish Kashiwar

## 📋 Project Overview

This project aims to better understand energy consumption patterns and identify factors affecting energy efficiency in Cambridge buildings. Using machine learning models, we predict energy consumption based on property data and provide actionable recommendations to reduce energy usage, supporting ESG goals in Cambridge.

## 🎯 Problem Statement

Buildings in Cambridge are subject to energy reporting requirements, but understanding which factors most significantly impact energy consumption remains challenging. This project uses data-driven approaches to:

- Predict energy consumption based on property characteristics
- Identify key contributing factors to energy usage
- Provide actionable recommendations for reducing energy consumption

## 📊 Data Sources

The analysis uses two primary datasets from the [Cambridge Open Data Portal](https://data.cambridgema.gov/):

1. **Cambridge Building Energy Use Data (BEUDO)**
   - Source: [Building Energy Use Disclosure Ordinance Data 2015-2022](https://data.cambridgema.gov/Energy-and-the-Environment/Cambridge-Building-Energy-Use-Disclosure-Ordinance/72g6-j7aq/about_data)
   - Contains energy and water use data at the parcel level
   - Covers large residential (50+ units), nonresidential (25,000+ sq. ft.), and municipal (10,000+ sq. ft.) buildings
   - Years: 2015-2022

2. **Cambridge Property Database**
   - Source: [Property Database FY2016-FY2024](https://data.cambridgema.gov/Assessing/Cambridge-Property-Database-FY2016-FY2024/eey2-rv59/about_data)
   - Contains physical property details (wall types, interior space, number of kitchens, etc.)
   - Data at building/unit level, requiring aggregation
   - Years: 2016-2024

## 🎯 Target Variable

**Weather-Normalized Site Energy Use Intensity (Site EUI)** - measured in kBtu/ft²

This metric normalizes for:
- Building size
- Yearly weather variance

Allowing focus on the impact of materials, age, and other physical property characteristics.

## 🔧 Methodology

### Data Processing
- Merged energy use and property databases on MapLot and Year
- Handled missing values and data quality issues
- Performed exploratory data analysis (EDA)
- Feature engineering and selection
- Data normalization and encoding

### Models Used
- **Linear Regression** - Baseline model
- **Polynomial Regression** - Capturing non-linear relationships
- **Gradient Boosting Regressor** - Advanced ensemble method
- **SHAP Values** - Model interpretability and feature importance

### Evaluation Metrics
- R² Score (Coefficient of Determination)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

## 🚀 Setup & Installation

### Prerequisites
- Python 3.8+
- Jupyter Notebook

### Installation

1. Clone this repository:
```bash
git clone https://github.com/jessie1007/Cambridge-Energy-Usage.git
cd Cambridge-Energy-Usage
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Download the data files:
   - Download the BEUDO dataset from the [Cambridge Open Data Portal](https://data.cambridgema.gov/Energy-and-the-Environment/Cambridge-Building-Energy-Use-Disclosure-Ordinance/72g6-j7aq/about_data)
   - Download the Property Database from the [Cambridge Open Data Portal](https://data.cambridgema.gov/Assessing/Cambridge-Property-Database-FY2016-FY2024/eey2-rv59/about_data)
   - Place CSV files in the `data/` directory (or update file paths in the notebook)

4. Open and run the Jupyter notebook:
```bash
jupyter notebook CambridgeEnergyUse_final.ipynb
```

## 📖 Usage

1. Ensure data files are in the correct location (or update paths in the notebook)
2. Run all cells in the notebook sequentially
3. The notebook includes:
   - Data loading and exploration
   - Data cleaning and preprocessing
   - Model training and evaluation
   - Results visualization
   - Feature importance analysis

## 📈 Key Findings

- Non-residential buildings show the highest average Site EUI
- Building age, property type, and physical characteristics significantly impact energy consumption
- Weather normalization is crucial for accurate year-over-year comparisons
- Gradient Boosting models provide superior predictive performance

## 🛠️ Technologies Used

- **Python** - Primary programming language
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Scikit-learn** - Machine learning models
- **Matplotlib & Seaborn** - Data visualization
- **SHAP** - Model interpretability
- **Statsmodels** - Statistical modeling

## 🤝 Contributing

This is a course project. For questions or collaboration, please contact the authors.

## 📄 License

See LICENSE file for details.

## 🙏 Acknowledgments

- Cambridge Open Data Portal for providing the datasets
- CSCI E-109a course instructors
- Harvard Extension School


---

**Note:** This project was completed as part of CSCI E-109a at Harvard Extension School.
