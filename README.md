# Residential Pricing Optimization Using Machine Learning

## Overview

This project focuses on developing machine learning models to predict and optimize housing prices based on various business metrics such as leads, visits, and reservations. By leveraging models like **Random Forest**, **XGBoost**, and potentially **time-series forecasting**, the project aims to support data-driven pricing decisions, prevent unprofitable pricing strategies, and ensure optimal price points for residential properties.

## Objective

The main goals are to:

- Accurately predict housing prices using key features like leads, visits, and reservations.
- Optimize pricing to align with market conditions and business goals, avoiding suboptimal pricing.
- Provide actionable insights to guide sales strategies, lead qualification, and inventory planning.

## Methodology

This project follows the **CRISP-DM** framework:

1. **Business Understanding**: Identify key variables (leads, visits, reservations) and the target variable (price).
2. **Data Understanding**: Explore and analyze the dataset (`Weekly.csv`) containing metrics like website leads, showroom visits, and separations.
3. **Data Preparation**: Clean, transform, and preprocess data, including feature engineering and encoding categorical variables.
4. **Modeling**: Train machine learning models, including:
   - Random Forest
   - XGBoost
   - Time-series forecasting (if applicable)
5. **Evaluation**: Assess model performance using metrics such as R², RMSE, and MAE.
6. **Deployment**: Plan for operationalizing the model with integration, dashboards, and retraining strategies.

## Dataset

The dataset (`data/Weekly.csv`) contains 1197 rows with the following key columns:

| Column Name               | Description                                            |
|---------------------------|--------------------------------------------------------|
| **ID**                     | Unique identifier from the ERP system.                 |
| **Fecha**                  | First day of the week.                                |
| **Semana**                 | Week of the year.                                     |
| **Proyecto**               | Name of the project within the enterprise.            |
| **Modelo**                 | Type of residential unit.                             |
| **Website Leads**          | Number of potential customers or visitors.            |
| **Showroom Visits**        | Number of in-person visits to the residential unit.   |
| **Separaciones**           | Number of bookings after the showroom stage.          |
| **Price**                  | Target variable (actual price of the housing; 0 indicates unavailable data). |
| **Inventario restante**    | Stock of available residential units.                 |
| **Conversión Separaciones (%)** | Conversion rate from leads to bookings.            |

## Model Performance

The **Random Forest** model achieved strong results:

- **R² Score**: 0.9796 (explains 97.96% of the variance in housing prices).
- **RMSE**: 168,393.56 (moderate error relative to the price range).
- **MAE**: 41,611.53 (low average deviation from actual values).

### Feature Importance

The most influential features for price prediction are:

- **Conversión Separaciones (%)**: Strongest predictor, indicating the efficiency of converting leads to bookings.
- **Separaciones and Ventas**: Reflect customer interest and actions.
- **Proyecto (e.g., NOV, STA)**: Specific projects significantly impact pricing.
- **Modelo (e.g., ATT2)**: Unit type has a moderate influence.

## Deployment Plan

To operationalize the model:

1. **Model Integration**: Deploy the Random Forest model for real-time or scheduled pricing predictions.
2. **Dashboarding**: Create visualizations for feature importance, predicted prices, and KPIs.
3. **Actionable Insights**: Use key features like 'Separaciones' and 'Conversión Separaciones (%)' to inform sales and inventory strategies.
4. **What-if Analysis Tools**: Enable scenario simulations by adjusting inputs (e.g., leads, prices).
5. **Retraining Strategy**: Schedule periodic retraining to maintain model performance with new data.

## Requirements

To run the notebook, install the required Python libraries by executing the following:

```bash
pip install pandas numpy scikit-learn xgboost matplotlib seaborn joblib
```

## 🧰 Dependencies

- Python 3.x
- Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `scikit-learn`
  - `xgboost`
  - `seaborn`

---

## 🚀 Usage

1. Clone this repository or download the notebook. (`HousingPriceOptimizer.ipynb`).
2. Place the dataset (`Weekly.csv`) in the data/ directory
3. Install the required dependencies (see above).
4. Run the notebook using Jupyter or a compatible environment to explore data, train models, and visualize results..

---

## 🚧 Expected Outcomes
* A robust machine learning model for accurate housing price predictions.
* Insights into key drivers of pricing, enabling data-driven decision-making.
* A framework for dynamic pricing and inventory management in the real estate industry.

## 📄 License

This project is open-source under the [MIT License](LICENSE).

---

## 🙏 Acknowledgments

- Dataset provided by the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing).
- Inspired by applied machine learning coursework and practical scenarios.

---

## 💬 Feedback

Feel free to open an issue for questions, suggestions, or feedback.

---
