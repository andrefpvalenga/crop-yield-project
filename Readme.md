## 🌾 Crop Yield Prediction — Machine Learning Project

### 📌 Overview

This project aims to predict **crop yield (hg/ha)** using classical Machine Learning models based on environmental and agricultural data.
It demonstrates a full end-to-end Data Science workflow including:
- Data collection and loading
- Exploratory Data Analysis (EDA)
- Feature preprocessing
- Model training and comparison
- Performance evaluation
- Model interpretation
- Conclusions and real-world applications

The goal is to build a baseline model capable of supporting agricultural decision-making in real scenarios (cooperatives, agtechs, government agencies, farms, insurance, trading, etc.). 

___

### 📁 Project Structure
```
crop-yield-project/
│── CropYieldPrediction.ipynb   # Main notebook
│── Data/
│     └── yield_df.csv          # Dataset (local copy)
│── LICENSE
│── README.md
|── requirements.txt
```

___

### 📊 Dataset

The dataset contains agricultural and environmental information per **country**, **crop type**, and **year**, including:
| Feature                       | Description                       |
| ----------------------------- | --------------------------------- |
| Area                          | Country/region                    |
| Item                          | Crop type                         |
| Year                          | Year of production                |
| hg/ha_yield                   | Productivity per hectare (target) |
| average_rain_fall_mm_per_year | Annual rainfall                   |
| avg_temp                      | Average temperature               |
| pesticides_tonnes             | Pesticide usage                   |

It is a simplified version of data available at **FAO (Food and Agriculture Organization)** and **World Data Bank**.

___

### 🔍 Exploratory Data Analysis (EDA)

The EDA covered:

#### ✔ Distribution analysis

- Most features show skewness and presence of outliers.
- Outliers were **not removed**, as they reflect real agricultural variability.

#### ✔ Correlation insights

- Weak correlation with the target variable, indicating a **complex non-linear problem**.
- Temperature shows a slight negative relationship.
- Pesticide usage shows a slight positive one.

#### ✔ Crop and region variability

- Production patterns vary strongly by country and crop.
- Some crops dominate yield variance.

___

### 🤖 Models Implemented

Three baseline regression models were trained and evaluated:

- **Decision Tree Regressor**
- **Random Forest Regressor**
- **Gradient Boosting Regressor**

#### ✔ Best Model

The **Random Forest Regressor** performed the best in the baseline setup.

#### ✔ Why Random Forest won

- Better handling of non-linear relationships
- Robustness to outliers
- Natural ability to rank feature importances
- Consistent performance across folds in cross-validation

___

### 📈 Results (Summary)

| Model             | Performance Summary                                           |
| ----------------- | ------------------------------------------------------------- |
| Decision Tree     | Strong performance; close to RF; slightly higher RMSE         |
| Gradient Boosting | Underperformed significantly; much higher error               |
| **Random Forest** | Best overall model (highest R², lowest RMSE and MSE)          |


> For full metrics (MAE, MSE, RMSE, R²), refer to the notebook.

___

### 🧠 Feature Importance (Insight)

Random Forest revealed that:

- **Crop type (Item) is overwhelmingly the most important variable**, meaning
  - the dataset is dominated by categorical agricultural patterns,
  - possibly requiring domain-specific encoding or feature engineering.
- Climatic variables have weaker but meaningful contributions.

This influences future modeling decisions.

___

### 🧪 How to Run

1. Clone the repository:
```
git clone https://github.com/andrefpvalenga/crop-yield-project
```

2. Install the dependencies:
```
pip install -r requirements.txt
```

3. Run the notebook:
```
jupyter notebook CropYieldPrediction.ipynb
```

Dataset must be placed inside the folder:
```
Data/yield_df.csv
```
___

### 🚀 Real-World Applications

This model can support real agricultural decision-making in:

#### 🌱 Producers and agronomists

- Choosing crops based on expected yield

- Estimating profitability before planting

- Planning irrigation and fertilizer use

#### 🚜 Cooperatives

- Anticipating production volume

- Planning storage and logistics

- Negotiating contracts and inputs

#### 🏭 Industry & agribusiness

- Forecasting demand for raw materials

- Strategic procurement and supply chain planning

#### 🏛 Government & agencies

- National crop forecasting

- Food security planning

- Price and inflation monitoring

#### 💰 Banks & insurers

- Rural credit risk estimation

- Pricing rural insurance policies