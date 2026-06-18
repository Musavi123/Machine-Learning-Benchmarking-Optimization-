# Machine-Learning-Benchmarking-Optimization-
This collaborative repository showcases joint research focused on evaluating, benchmarking, and optimizing diverse machine learning models

Evaluation of the Compressive Strength of Concrete
Authors: Syed Ahmed H. Musavi, Clayton Durst  

Concrete plays a key role in modern construction, and its compressive strength is essential for ensuring structural integrity. The goal of this study is to examine the relationship between concrete mixture components and compressive strength. By exploring both linear and nonlinear regression models, the project aims to optimize concrete mixtures for maximum strength while balancing interpretability and accuracy.  
Dataset

    Sourced from the UC Irvine Machine Learning Repository.  

    Contains 8 numeric predictor variables, consisting of up to 7 ingredients recorded in kilograms per cubic meter and an age component measured in days.  

    The target variable is the compressive strength of the resulting concrete, measured in megapascals.  

Methodology

    Exploratory Data Analysis (EDA): Evaluated variable distributions via histograms and performed Principal Components Analysis (PCA) to attempt dimensional reduction.  

    Linear Regression Modeling: Tested multiple linear regression models, including a full 8-predictor model, best subset selection, ridge regression, and lasso regression.  

    Non-Linear Regression Modeling: Evaluated generalized additive models using polynomial, cubic spline, natural spline, and local regression basis functions.  

    Advanced Extensions: Tested support vector machine (Polynomial and Radial kernels) and random forest regression.  

Key Findings

    Non-linear models demonstrated superior performance over linear models, indicating that the relationship between predictors and the target variable is complex and non-linear.  

    Local Regression emerged as the top-performing model, achieving a cross-validation MSE of 30.03.  

    Random forest variable importance plots revealed that the age and cement variables are the two most important factors in determining concrete strength.  

    The analysis indicated that multicollinearity and correlation did not pose any significant issues among the predictors.  

Benchmarking Classification Methods
Authors: Matthew Clifford, Fatima Daher, Clayton Durst, Noah Greco, Syed Ahmed H. Musavi, Rohit Vempati  

This study conducts a comprehensive benchmarking analysis of diverse classification methods available within the Comprehensive R Archive Network (CRAN). The primary goal is to compare the performance of six different algorithms to provide clarity on their strengths, weaknesses, and real-world tradeoffs.  
Dataset

    Utilized 20 diverse, publicly acquired datasets (e.g., breast cancer, diabetes, penguins, titanic) containing a combination of numerical and categorical variables.  

    Datasets were carefully preprocessed for binary classification, including handling missing values and target variable recording.  

    Implemented a 70% training and 30% validation split for the analysis.  

Methodology

    Benchmarking: Built models using logistic regression, support vector machine (SVM), linear discriminant analysis (LDA), rpart (decision trees), naïve Bayes, and random forest.  

    Metrics Tracked: Calculated the training time, validation set accuracy, and AUC for each model.  

    Statistical Validity: Repeated the training and evaluation process 20 times for each dataset to calculate average performance metrics.  

    Hyperparameter Tuning: Developed custom tuning functions to optimize SVM (exploring linear, polynomial, and radial kernels) and LDA (tuning the shrinkage parameter).  

Key Findings

    No singular model type consistently outperformed the others across all 20 datasets, proving that model selection should be an experimental process tailored to the specific dataset.  

    Random forest and SVM were generally strong methods in terms of accuracy and AUC, with both models tying for the highest accuracy across seven different datasets.  

    A distinct tradeoff was observed between speed and accuracy: SVM was the slowest of all tested methods, while naïve Bayes was the fastest computationally.  

    Hyperparameter tuning for LDA and SVM resulted in a modest average accuracy increase, though it drove significant accuracy improvements for specific datasets like "fires" and "heart".
