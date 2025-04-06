# Wine-Quality-Prediction
# **Summary**


---
## Introduction
The development of a machine learning-based wine quality prediction model is an essential tool for winemakers, providing precise estimates of wine quality based on its physical and chemical characteristics. In addition to helping to comprehend the factors influencing wine quality, this predictive framework assures consistency, makes informed decisions easier, and promotes ongoing improvement in wine production. This method, which makes use of statistical and machine learning tools, gives producers insightful knowledge about the complex interactions that influence wine quality, enabling them to improve their workflows and produce wines that reach new levels of quality.

Dataset consist of 1143 rows 13 column

---

##Data Pre-Processing

The 'Id' column, deemed unimportant, was dropped from the dataset.

* 1.0  *Handling Null Values*
      
    No Null Value

* 1.1  *Handling duplicates*

    It had 125 duplicates removed the duplicate
        
    After handling duplicates data consist of 1018 rows 12 column
        

* 1.2 *Class Distribution Analysis*

    Verified whether the data is imbalanced or balanced. Discovered that the dataset was unbalanced.  Multi-Classification was then converted from Binary Classification. A binary classification system was implemented in the quality column due to the imbalance in classes; ratings below 7 were labeled as 0 (indicating not good quality), and ratings above 7 were labeled as 1 (indicating good quality).

* 1.3 *Data Analysis*

    Utilized visualization techniques such as heatmap for correlation coefficients analysis
    
*  1.4 *Outlier Detection*
    
    Box plots are used to identify outliers that might have an impact on the performance of the model.

* 1.5 *Data Splitting*

    Split the dataset into feature variables (X) and target variable (y), where X comprises the independent variables representing the physicochemical properties of wines, and y represents the dependent variable, which is the wine quality.

* 1.6 *Feature Scaling*

    Applied standard scaling to normalize the feature values within a range of 0 to 1. This step ensures that all features contribute equally to the model training process and prevents any single feature from dominating due to its larger magnitude.


---

## Model Deployment

* 2.0 *Logistic Regression*

    The 100% of the data was divided into 30% for testing and 70% for training.
      Accuracy of 86% was obtained.

* 2.1 *KNN*

    70% of the 100% of the data was split up for training and 30% for testing. Count the 20 closest neighbors.
      Attained an 86% accuracy rate

* 2.2 *Decision Tree*

    The 100% of the data was divided into 30% for testing and 70% for training.Taking into consideration max_depth=40 and min_samples_leaf=25.
      Obtained 87% accuracy


* 2.4 *Random Forset*

    In 100% of data was splited the data into 70% training and 30% testing.Training the model 42 times(running 42 time). Considering 40 Decision Tree.
      Achieved an accuracy of 90%
    
---

## Hyperparameter Tuning

* 3.0 *Entropy as Decision Factor*
    
    From Decision Tree
      Accuracy dropped slightly to 85%.

* 3.1 *Cross Validation*

    From Decision Tree
      Mean Accuarcy of 87%

* 3.2 *Bagging Classifier*

    From Decision Tree
        Accuarcy is 87%

---
##Conclusion

Data-driven models such as Logistic Regression, Decision Tree, KNN, and Random Forest help winemakers show critical physicochemical components of quality wines. Preprocessing corrects for nulls, outliers, and duplicates; transforming unbalanced data improves accuracy. Equitable feature contributions are ensured by feature scaling. With 90% accuracy, Random Forest performs best, followed by Decision Tree at 87%. KNN and logistic regression do somewhat worse, at 86%. Random Forest performs better when its hyperparameters are adjusted, demonstrating how predictive modeling can improve the evaluation of wine quality.
