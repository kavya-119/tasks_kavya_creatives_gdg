🐚 Crab Age Prediction — EDA + Regression

This repository contains a Google Colab notebook for exploratory data analysis (EDA) and regression modeling to predict the age of crabs based on morphological features.

📂 What’s inside

Notebook (.ipynb) — Data cleaning, EDA, feature engineering, encoding, scaling and regression modeling

Data source description — Details of the crab dataset, preprocessing, and feature transformations

Modeling section — Building and evaluating regression models (e.g., Support Vector Regressor, XGBoost, etc.)

Evaluation metrics — R², MAE, MSE/RMSE and other performance metrics

🚀 How to use

Open the notebook in Google Colab (click “Open in Colab” or paste the notebook link).

Mount your Google Drive to access the dataset.

Run all the cells in order — from data loading → cleaning → encoding → modeling → evaluation.

Feel free to modify and experiment with different models or hyperparameters.

🔧 Dependencies

Major Python libraries used:

pandas, numpy — data manipulation

scikit-learn — preprocessing, encoding, scaling, model building

matplotlib, seaborn — visualization

(Optional) ydata-profiling — automated EDA reports

To replicate the environment, you can install dependencies with:

pip install pandas numpy scikit-learn matplotlib seaborn ydata-profiling

📖 What you’ll learn

How to perform a full data pipeline: cleaning, encoding & scaling

Handling imbalanced / noisy data (e.g. removing invalid rows)

Building and comparing regression models for age prediction

Evaluating model performance using MAE, MSE, RMSE, R²

✨ Next steps / Ideas

Try out more regression models (e.g., Random Forest, XGBoost, Ridge)

Perform hyperparameter tuning for better results

Add feature importance analysis or visualizations

Deploy a simple web interface/API to predict crab age
