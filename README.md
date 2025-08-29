## Glass Classification

### Project Overview

This project aims to classify **different types of glass** based on their chemical composition. By analyzing the concentrations of various chemical components such as silicon, sodium, magnesium, and aluminum, the goal is to develop a machine learning model that can accurately distinguish between different glass types. This is a classic classification problem with applications in forensics and materials science.

-----

### Technical Highlights

  * **Dataset**: The dataset used is `glass.xls` which contains the chemical analysis of 214 glass samples.
  * **Size**: 214 entries, 10 columns.
  * **Key Features**:
      * `RI` (Refractive Index), `Na` (Sodium), `Mg` (Magnesium), `Al` (Aluminum), `Si` (Silicon), `K` (Potassium), `Ca` (Calcium), `Ba` (Barium), `Fe` (Iron).
  * **Approach**:
      * **Data Cleaning**: One duplicate row was found but not removed in the provided code. The dataset has no missing values.
      * **Exploratory Data Analysis**: The code checks basic statistics, null values, duplicates, and unique values.
      * **Multi-class Classification**: The target variable `Type` has 6 distinct integer values representing different glass types (1, 2, 3, 5, 6, 7). The `LabelEncoder` was used to convert these into a zero-indexed format for model training.
      * **Models Used**:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * **76.9%** with XGBoost, Random Forest, and Gradient Boosting Classifiers.
      * **72.3%** with Bagging Classifier.
      * The moderate accuracies suggest that while the models have some predictive power, the task is challenging due to the small dataset size and the complexity of distinguishing between multiple glass types with similar chemical compositions.

-----

### Purpose and Applications

  * **Forensic Analysis**: Assist forensic scientists in identifying glass fragments found at crime scenes.
  * **Quality Control**: Help manufacturers ensure the chemical consistency and quality of glass products.
  * **Material Science Research**: Provide insights into the relationship between glass composition and its properties.
  * **Recycling**: Aid in the sorting of different types of glass for recycling purposes.

-----

### Installation

To install the necessary libraries, the following command is needed:

```bash
pip install xlrd pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Handling the duplicate entry by either dropping it or investigating its significance.
  * Performing comprehensive hyperparameter tuning and cross-validation for the top-performing models.
  * Exploring the use of dimensionality reduction or feature engineering, as some features might be highly correlated.
  * Adding explainability (e.g., SHAP or LIME) to understand which chemical components are the most critical for classifying a specific glass type.
