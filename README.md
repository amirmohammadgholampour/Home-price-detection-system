# California Housing Price Prediction 

## Project Overview  
This project focuses on predicting California housing prices using machine learning techniques.  
The model is trained on the **California Housing dataset** and applies **Extreme Gradient Boosting (XGBoost)** with engineered features to achieve high accuracy.  

---

## Dataset Description  

The dataset contains information about California districts, including geographical, demographic, and economic data.  
The **target variable** is `median_house_value`.  

| Feature | Description |
|---------|-------------|
| longitude | Geographic coordinate (west-east) |
| latitude | Geographic coordinate (north-south) |
| housing_median_age | Median age of houses in the district |
| total_rooms | Total number of rooms in all houses |
| total_bedrooms | Total number of bedrooms in all houses |
| population | Population of the district |
| households | Number of households in the district |
| median_income | Median income of households (in tens of thousands of dollars) |
| ocean_proximity | Proximity to the ocean (categorical: `<1H OCEAN`, `INLAND`, `NEAR OCEAN`, `NEAR BAY`, `ISLAND`) |
| rooms_per_household | Engineered feature: total rooms ÷ households |
| bedrooms_per_room | Engineered feature: total bedrooms ÷ total rooms |
| population_per_household | Engineered feature: population ÷ households |
| **median_house_value** | **Target variable – median house value in USD** |

---

## Model Description  

- **Algorithm used**: Extreme Gradient Boosting (**XGBoost**)  
- **Feature Engineering**: Added new features such as `rooms_per_household`, `bedrooms_per_room`, and `population_per_household`.  
- **Evaluation Metrics**: MAE, MSE, and R² score.  

### Model Performance  

| Metric | Test Set | Validation Set |
|--------|----------|----------------|
| MAE | 27,364 | 28,020 |
| MSE | 1.63e9 | 1.66e9 |
| R² | 0.83 | 0.82 |

The model explains **~83%** of the variance in housing prices, which is a strong performance for real-world data.  

---

## Installation  

Clone the repository and install dependencies:  

```bash
git clone https://github.com/amirmohammadgholampour/Home-price-detection-system/
pip install -r requirements.txt
```


## Future Improvements  
- Hyperparameter tuning with **GridSearchCV**  
- Feature selection and dimensionality reduction  
- Comparison with Deep Learning models  
