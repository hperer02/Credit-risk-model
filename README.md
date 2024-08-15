# Home Credit Risk Model Pipeline

## Overview 
Discover a comprehensive approach to constructing credit risk models, employing some various machine learning algorithms like LightGBM and CatBoost, alongside ensemble techniques for robust predictions. Our pipeline emphasizes data integrity, feature relevance, and model stability, crucial elements in credit risk assessment. 

## Requirements

- Libraries: NumPy, pandas, polars, seaborn, matplotlib, scikit-learn, lightgbm, imbalanced-learn, joblib, catboost

## Methodology

1. **Data Loading**: All files are found in both .csv and .parquet formats and the dataset can be found in the given competition link at the end.
2. **Initialization**: Run initialization code to set up necessary functions and configurations.
3. **Data Preprocessing**: Execute data preprocessing steps to handle missing values and optimize memory usage.
4. **Feature Engineering**: Use provided feature engineering functions to extract relevant features from the dataset.
5. **Model Training**: Train machine learning models like LightGBM and CatBoost using preprocessed data.
6. **Ensemble Learning**: Combine predictions from multiple models using the custom Voting Model for improved performance.
7. **Evaluation**: Assess ensemble model performance and generate submission files for further analysis.

## Detailed Steps

### Data Loading & Preprocessing
This dataset contains a large number of tables as a result of utilizing diverse data sources and the varying levels of data aggregation used while preparing the dataset. We start by loading the necessary datasets and performing initial preprocessing steps. This includes handling missing values, removing duplicates, and optimizing memory usage. The preprocessing pipeline ensures that the data is clean and ready for feature extraction and model training.

### Feature Engineering
Feature engineering is crucial for improving model performance. We create new features based on domain knowledge and data exploration. This includes aggregating statistics, and encoding categorical variables. Advanced feature selection methods are also employed to retain the most relevant features for the model.

### Model Building & Training
We implement and train several machine learning models, including:
- **LightGBM**: A gradient boosting framework that uses tree-based learning algorithms.
- **CatBoost**: A gradient boosting algorithm that handles categorical features efficiently.

These models are trained using cross-validation to ensure robust performance and to prevent overfitting.

### Ensemble Learning
To further improve prediction accuracy and model stability, we use ensemble learning techniques. Our custom Voting Model combines the predictions of LightGBM and CatBoost models. By averaging the predictions, the ensemble model often outperforms individual models in terms of accuracy and stability.

### Inference
In the inference phase, we use the trained ensemble model to make predictions on the test set. The final output is a set of predictions that can be submitted for evaluation.

## Conclusion
This project demonstrates a full pipeline for developing a robust credit risk model. By focusing on data preprocessing, feature engineering, model training, and ensemble learning, we achieve high accuracy and model stability. This approach is essential for effective credit risk assessment and can be adapted to other domains requiring reliable predictive modeling.

**Competition link** - https://www.kaggle.com/competitions/home-credit-credit-risk-model-stability 
