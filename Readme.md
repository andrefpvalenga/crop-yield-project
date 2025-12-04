🌾 **Crop Yield Prediction — Machine Learning Project**

📌 **Overview**

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

### 📁 **Project Structure**
```
crop-yield-project/
│── CropYieldPrediction.ipynb   # Main notebook
│── Data/
│     └── yield_df.csv          # Dataset (local copy)
│── LICENSE
│── README.md
```

___

### 📊 **Dataset**

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