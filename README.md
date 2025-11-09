 # ☀️ **Solar Energy Prediction using XGBoost and Random Forest**
This project predicts **solar radiation levels (solar energy output)** using **meteorological parameters** such as temperature, humidity, pressure, wind speed, and wind direction.
The goal is to accurately forecast **solar energy potential** using two advanced machine learning algorithms — **Random Forest** and **XGBoost**.

---

## 📘 Project Overview

This notebook demonstrates the full workflow of a **machine learning regression project** for solar-energy prediction:

1. **Data Loading** – Imported and read the cleaned dataset `SolarPrediction_cleaned.csv`
2. **Data Cleaning** – Fixed inconsistent timestamps, handled missing values, and removed redundant columns
3. **Feature Engineering** –

   * Extracted time-based features (`hour`, `dayofyear`) and applied sine/cosine encoding
   * Filtered out nighttime samples (low radiation) for more realistic accuracy
   * Added derived features such as `hour²`, rolling averages, and an `is_day` indicator
4. **Data Splitting** – Used a **time-based split** (70% train / 15% validation / 15% test)
5. **Model Training** – Trained and compared two regression models:

   * 🌳 **Random Forest Regressor**
   * ⚡ **XGBoost Regressor** (tuned with Randomized Search CV)
6. **Model Evaluation** – Calculated performance metrics (RMSE, MAE, R², MAPE, Accuracy)
7. **Visualization** – Compared **Actual vs Predicted Solar Radiation** with clear visual charts

---

## 🧠 Key Features

* Predicts **solar radiation (W/m²)** based on weather data
* Implements **time-aware train/validation/test splitting**
* Uses **Random Forest** and **XGBoost** regression algorithms for accuracy comparison
* Automatically calculates **RMSE**, **MAE**, **R²**, **MAPE**, and **Average Accuracy**
* Generates insightful visualizations for performance analysis
* Establishes a baseline for **renewable-energy forecasting systems**

---

## 🧩 Project Progress Tracker
| Step | Task                                        | Status |
| :--: | ------------------------------------------- | :----: |
|  ✅ 1 | Data cleaned and datetime fixed             | ✔ Done |
|  ✅ 2 | Data split into Train/Val/Test (time-based) | ✔ Done |
|  ✅ 3 | Model trained (Random Forest, XGBoost)      | ✔ Done |
|  ✅ 4 | Predictions generated                       | ✔ Done |
|  ✅ 5 | Compared predicted vs actual solar values   | ✔ Done |
|  ✅ 6 | Calculated RMSE, MAE, R², MAPE, Accuracy    | ✔ Done |
|  ✅ 7 | Created visual chart (Actual vs Predicted)  | ✔ Done |

## 📊 Dataset Information

**Dataset Name:** Solar Prediction Dataset
**Source:** Cleaned and preprocessed open dataset
**Rows:** ~32,000

**Columns:**

* `Radiation` — Solar radiation in W/m² (**Target Variable**)
* `Temperature` — Ambient temperature (°C)
* `Pressure` — Atmospheric pressure (mbar)
* `Humidity` — Relative humidity (%)
* `WindDirection(Degrees)` — Wind direction in degrees
* `Speed` — Wind speed (m/s)
* `TimeSunRise`, `TimeSunSet`, `Data`, `Time` — Time features used for datetime creation

---

## 🧰 Tech Stack

* **Python 3 (Google Colab)**
* **Pandas**, **NumPy** — Data manipulation and analysis
* **Scikit-learn**, **XGBoost** — Model training and evaluation
* **Matplotlib** — Data visualization
* **Math**, **Datetime** — Time-series feature handling

---

## 🧪 Model Evaluation Results

| Model                | RMSE (W/m²) | MAE (W/m²) |       R² |  MAPE (%) | Avg Accuracy (%) |
| :------------------- | ----------: | ---------: | -------: | --------: | ---------------: |
| 🌳 Random Forest     |      163.17 |      86.12 |    0.398 |     97.00 |            49.00 |
| ⚡ XGBoost (Improved) |      140.32 |      78.45 | **0.78** | **43.43** |        **60.87** |

✅ **Final Model Metrics (Filtered Daylight):**

* **Mean Absolute Percentage Error (MAPE): 43.43%**
* **Average Prediction Accuracy: 60.87%**
* **Minimum Accuracy:** 0.00%
* **Maximum Accuracy:** 99.95%

These metrics show a **54% reduction in prediction error** and a significant **accuracy improvement** compared to the initial baseline.

---

## 📈 Visualizations

* **Actual vs Predicted Scatter Plot**
* **Prediction Accuracy Comparison (Filtered Daylight)**
* **Feature Importance Bar Chart**

These plots illustrate how closely model predictions align with true solar-radiation readings and identify which weather factors influence predictions the most.

---

## 🚀 How to Run

1. Clone this repository

   ```bash
   git clone https://github.com/your-username/Week-2-Solar-Energy-Prediction-System.git
   cd Week-2-Solar-Energy-Prediction-System
   ```

2. Install dependencies

   ```bash
   pip install pandas numpy scikit-learn xgboost matplotlib
   ```

3. Open the notebook

   ```bash
   jupyter notebook Week2_SolarEnergyPrediction.ipynb
   ```

4. Run all cells sequentially to reproduce the training, prediction, and visual results.

---

## 🏁 Results Summary

The **Week-2 Solar Energy Prediction System** demonstrates a complete **end-to-end machine learning pipeline** for solar radiation forecasting.

* **Best Model:** XGBoost Regressor
* **Performance:**

  * MAPE = 43.43%
  * Accuracy ≈ 60.87%
  * R² ≈ 0.78
* The project effectively predicts solar radiation using standard weather data, forming a solid baseline for improvement.

---


## 🌟 Acknowledgments

* **SolarPrediction Dataset** contributors for open data
* **Scikit-learn** and **XGBoost** teams for powerful ML libraries
* **Google Colab** for providing a free computational environment

---

