# Airlines User Satisfaction Analytics
This repository contains my work for 2 major assignments 2 and 3 of the Fundamental of Data Analytics subject at the University of Technology Sydney (UTS) taught by Dr. Maoying Qiao. Each assignment is done using mostly scikit-learn along with a notebook and a pdf, which includes a detailed explanation of the concepts and implementations involved.

# Project Scenario
A global airlines has collected the data from customer survey to analyze their satisfy for the flight. In this project, the Head of the Analytics Unit want to use the collected dataset to do a user satisfaction classification to help understand the factors highly correlated with passengers experience. It will be devided into 2 calssification: Satisfied and Neutral/ Disatisfied.

# Assignment 2: Data Exploration and Visualisation

1. Identify the attribute type of each attribute in the dataset.
2. For each attribute, identify the values of the summarising properties for the attributes, including frequency, location and spread.
3. Using Python, explore multiple attributes relationship of the dataset, and identify any outliers, clusters of similar instances, "interesting" attributes and specific values of those attributes.
  <img width="965" height="876" alt="image" src="https://github.com/user-attachments/assets/2c463d46-ebc1-4943-9012-723c5f38e3d9" />

5. Data Preprocessing:
- Equi-width binning and Equi-depth binning
- Min-max normalization and Z-score normalization
- Discretise
- Binarise

# Assignment 3: Data Preprocessing and Stellar Classification
A practical data analytics project that follows on from the data exploration in Assignment 2. Here, you will make a correct prediction on the dataset after employing a sophisticated process of exploring the problem very thoroughly, preprocessing the data, looking at different methods, choosing their best parameter settings, and identifying the best classifier in a principled and explainable way.

1. Data Preprocessing and Transformations:
- Encoding the target
- Splitting the dataset
- Handling Missing Values
- Handling outlier (Delay)
- Normalization (Flight Distance)
- Standardization (Age)
- Encoding categorical variables

2. Cross-validation on Base Classifiers for Initial Testing:
To establish baseline performance, seven classification models were first trained using their default parameters: Logistic Regression, Decision Tree, Random Forest, XGBoost, LightGBM, CatBoost, AdaBoost.
<img width="752" height="367" alt="image" src="https://github.com/user-attachments/assets/fa95c02b-94a8-40f5-8a20-793f20d9c8b0" />
Each model was evaluated using Cross-Validation to ensure balanced class representation across folds. Stratified k-fold cross-validation (5 folds) was used in this case to ensure each fold maintains the 57%–43% class ratio of the target variable.

4. Hyperparameter Tuning of Potential Classifiers
The purpose of this step is to find the best hyperparameters and best performance for 3 potential classifiers which were identified in the Initial Testing before: CatBoost, LightGBM, and XGBoost by using RandomSearch. Random Search was chosen because it is computationally more efficient and can explore a broader range of hyperparameter combinations within the same time budget. 

5. Evaluation for Best Estimator from each Search
The F1-score was selected as the primary evaluation metric for this classification task. This decision is based on the nature of the target variable: customer satisfaction, while not extremely imbalanced, still requires careful attention to both precision (correctly identifying satisfied or dissatisfied customers) and recall (capturing as many true instances as possible). The F1-score represents the harmonic mean of precision and recall, providing a balanced measure that penalizes extreme differences between the two. To provide a more comprehensive evaluation, additional metrics were also used to support and interpret the model’s performance, including Accuracy, Precision, Recall, ROC - AUC.
   <img width="1007" height="849" alt="image" src="https://github.com/user-attachments/assets/9bd41d4a-74ed-4203-a956-0305265c9960" />
   <img width="667" height="469" alt="image" src="https://github.com/user-attachments/assets/6dc2f573-ade5-4f8b-ae50-76d3dc668aa4" />


