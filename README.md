# Package-Sorting_and_Management
A Hybrid Model for Predicting Priority Scores in Logistics.

The hybrid predictive model assigns a *Normalized Priority Score* to package delivery tasks, improving logistical efficiency and task prioritization. Using a meta-learning approach, it combines XGBoost and a Deep Neural Network (DNN) to produce highly accurate predictions. This project demonstrates how integrating multiple models can outperform single-model approaches in a controlled, linear setting.

## Data Description

The dataset consists of 50,000 rows and includes the following columns:
- `Package_ID`: Unique identifier for each package
- `Urgency`: Priority level of the package
- `Order_Availability`: Stock status of the order
- `Size_cm3`: Package size in cubic centimeters
- `Fragility`: Binary value indicating if the package is fragile
- `Speed`: Delivery speed requirements
- `Weight_kg`: Package weight in kilograms
- `distance_in_km`: Delivery distance
- `Return_Rate`: Rate of package returns
- `FIFO`, `FEFO`: Inventory handling methods
- `Shipment_cost`: Shipping cost
- `Priority_Score`: Assigned priority level of the package

## Models and Results

Three models were trained to predict the *Normalized Priority Score*:
1. **XGBoost Model**  
   - **RMSE**: 0.1704  
   - **MAE**: 0.1084  
   - **R²**: 0.9930

2. **Deep Neural Network (DNN) Model**  
   - **RMSE**: 0.1736  
   - **MAE**: 0.7213  
   - **R²**: 0.9928

3. **Meta-Learner (Hybrid Model)**  
   - **RMSE**: 0.0674  
   - **MAE**: 0.0423  
   - **R²**: 0.9989  

The meta-learner effectively combines XGBoost and DNN models, achieving the best performance with an R² of 0.9989, demonstrating the power of ensemble learning in predictive accuracy.

