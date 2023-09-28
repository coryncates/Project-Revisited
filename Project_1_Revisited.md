
# Project 1 Revisited - Supermarket Sales Prediction

## Overview
This project aims to predict supermarket sales, focusing on enhancing predictive models and providing detailed interpretations of the results. Two main models, Linear Regression and Random Forest, are employed to understand the significant features impacting sales.

## Stakeholder Observations
Detailed observations and insights are crucial for stakeholders to comprehend the model's predictions and make informed decisions. The observations are based on extensive analysis and visualizations, providing a comprehensive understanding of the supermarket sales data and model outcomes.



## Linear Regression Coefficients

### Linear Regression Coefficients Interpretation
![Linear Regression Plot](https://github.com/coryncates/Prediction-of-Product-Sales/blob/main/Lin.png?raw=true)

The Linear Regression coefficients plot reveals the influence of each feature on the predicted supermarket sales. Each coefficient represents the change in sales for a one-unit change in the respective feature, assuming other features remain constant.

1. **Item_MRP:** A positive and high coefficient suggests that the Maximum Retail Price (Item_MRP) has a significant positive impact on sales, indicating that items with higher prices tend to have higher sales.
2. **Outlet_Type_Supermarket Type3:** The positive coefficient for this feature suggests that being of 'Supermarket Type3' type is associated with increased sales, implying that outlets of this type generally experience higher sales.
3. **Outlet_Type_Supermarket Type1:** This feature also has a positive coefficient, indicating that 'Supermarket Type1' outlets tend to have higher sales, but the impact is less compared to 'Supermarket Type3' outlets.


## Random Forest Feature Importances

### Random Forest Feature Importances Interpretation
![Random Forest Importances Plot](https://github.com/coryncates/Prediction-of-Product-Sales/blob/main/Reg.png?raw=true)

The Random Forest feature importances plot illustrates the significance of each feature in predicting supermarket sales. Features with higher importance values have a greater impact on the model's predictions.

1. **Item_MRP:** This feature has the highest importance, indicating that the Maximum Retail Price (Item_MRP) is a critical factor influencing sales predictions, reaffirming its pivotal role observed in Linear Regression analysis.
2. **Outlet_Type_Supermarket Type3:** This feature also has high importance, suggesting that the 'Supermarket Type3' outlets play a crucial role in sales predictions, likely due to their distinct operational characteristics leading to higher sales.
3. **Outlet_Identifier_OUT027:** The importance of this feature implies that the outlet identified as 'OUT027' has unique attributes or operational strategies contributing significantly to sales predictions.

### Reassessing the Models: A Closer Look at Random Forest and SHAP Analysis

In our journey to predict supermarket sales, we've employed various models and techniques. One of the pivotal models used was the [Random Forest model](https://github.com/coryncates/Prediction-of-Product-Sales/blob/main/Reg.png?raw=true). Its initial interpretations provided essential insights into feature importances and helped shape our understanding of the model’s decision-making process.

To deepen our insights, we also employed SHAP (SHapley Additive exPlanations) to interpret the model. SHAP values provide a unified measure of feature importance and allow a more detailed understanding of feature interactions and impacts.

#### **Comparison between Random Forest and SHAP Feature Importances:**
The Random Forest model provided us with a primary understanding of feature importances based on the mean decrease in impurity, revealing ‘Item_MRP’ as a highly influential feature. However, SHAP values, through their intricate calculations considering all possible feature value combinations, offered a more nuanced view.

SHAP unveiled not just the magnitude but also the direction of the influence of the features. While the [bar plot summary](https://github.com/coryncates/Prediction-of-Product-Sales/blob/main/bar.png?raw=true) highlighted the impactful features, the [dot plot summary](https://github.com/coryncates/Prediction-of-Product-Sales/blob/main/dot.png?raw=true) allowed us to visualize the intricate details of each feature's influence on individual predictions, with each dot representing a Shapley value for a feature and an instance.

#### **Interpretation of SHAP values:**
- The bar plot indicates the average magnitude of SHAP values per feature, reflecting the impact of features on the model output. In this model, ‘Item_MRP’, ‘Outlet_Type’, and ‘Item_Visibility’ predominantly influence the predictions.
- The dot plot, with its color-coded details (blue indicating lower and red indicating higher feature values), offers insights into how each feature value (high or low) pushes the model’s output from the base value. The spread of the dots along the x-axis represents the range of the Shapley values, revealing the variability of the impact of the feature values on the model predictions.

#### **Feature Insights:**
- ‘Item_MRP’ emerges as a prominent feature in both the models, with the models heavily relying on it for predictions. However, the exact quantitative relationship between ‘Item_MRP’ and ‘Item_Outlet_Sales’ is model-specific and not necessarily reflective of real-world relationships.
- The model's extensive reliance on a single feature like ‘Item_MRP’ might lead to overemphasis and potentially overshadow the contribution of other significant features, affecting the model's generalization capability on unseen data.

#### **Conclusion:**
While both Random Forest and SHAP analyses have their unique strengths in interpreting model decisions, a synergistic approach leveraging both methods can offer richer, more nuanced insights, enhancing our understanding of model intricacies and aiding in the development of more robust, informed models.


## Note
For detailed insights and accurate interpretations, please refer to the actual results and outputs in the [Project 1 Revisited Notebook](Project_1_Revisited.ipynb).

### Additional Details
- Linear Regression Coefficients Plot: ![Linear Regression Plot](https://github.com/coryncates/Prediction-of-Product-Sales/blob/main/Lin.png?raw=true)
- Random Forest Feature Importances Plot: ![Random Forest Importances Plot](https://github.com/coryncates/Prediction-of-Product-Sales/blob/main/Reg.png?raw=true)
