## Predicting Apple Quality
This project focuses on predicting the quality of an apple based on different features of the fruit. The dataset used in this project comes from Kaggle and was provided by an American agriculture company. The data has been scaled and cleaned for ease of use. The potential use cases of the data are fruit classification and quality prediction.

### Getting Started - Business Understanding
The first step was to read and understand the data. Dataset comes from Kaggle [link](https://www.kaggle.com/datasets/nelgiriyewithana/apple-quality/data). This dataset was provided by an American agriculture company. Data has been scaled and cleaned for ease of use. The dataset contains 4000 entries with 9 columns, including the unique identifier for each fruit, size, weight, sweetness, crunchiness, juiciness, ripeness, acidity, and quality. The quality column contains binary values of good and bad.

Index: 4000 entries, 0 to 3999
Data columns (total 9 columns):
 #   Column       Non-Null Count  Dtype  
---  ------       --------------  -----  
 0   A_id         4000 non-null   float64
 1   Size         4000 non-null   float64
 2   Weight       4000 non-null   float64
 3   Sweetness    4000 non-null   float64
 4   Crunchiness  4000 non-null   float64
 5   Juiciness    4000 non-null   float64
 6   Ripeness     4000 non-null   float64
 7   Acidity      4000 non-null   float64
 8   Quality      4000 non-null   object 
dtypes: float64(8), object(1)

Potential use cases of the data are:

Fruit Classification: Classifying fruits based on given features.
Quality Prediction: Predict the quality of the fruit based on given features.


### Exploratory Data Analysis

- There were no null values in the dataset. Then looked for duplicates, there were none.
- Ran different plots to analyze all features in the dataset. Heatmap highlighted some of the correlation between Quality feature and other features. Subsequently I ran bar charts as well as normal distributions for each of the features against quality, which gave a high level overview of all the features.

### Data Preperation
- As the data was already scaled and cleaned there was not much from a data preperation perspective.
- Dropped A_Id field as it was just a unique identifier for each of the apple and had no impact on the quality of the fruit.
- Converted Quality values of good and bad to 1 and 0 respectively to make them numeric for data modelilng.
- For modeling purposes, split the data into a training and test set with a 70/30 split.

## Modeling
- Once final dataset is ready, ran different classification models on the training dataset and calculated accuracy, precision, recall, and F1 scores for each model. We also found the best parameters for each model using Grid Search. Finally, we computed and printed the confusion matrix for each model. Plotted the graphs to understand visually.
The following models were used in this analysis:
* Logistic Regression
* KNN
* Decision Trees
* SVM

The results of the classification models are as follows:
Model	Accuracy	Precision	Recall	F1 Score
Logistic Regression	0.7525	0.753268	0.759473	0.756358
KNN	0.901667	0.902801	0.902801	0.902801
Decision Tree	0.798333	0.761087	0.876442	0.814701
SVM	0.914167	0.930034	0.897858	0.913663

### Evaluation of Models
Based on these results, we can conclude that the SVM model performs the best with an accuracy of 91.4%, precision of 93%, recall of 89.8%, and F1 score of 91.4%. The KNN model also performs well with an accuracy of 90.2% and consistent precision, recall, and F1 scores. The Logistic Regression and Decision Tree models have lower accuracy and F1 scores compared to SVM and KNN models.

### Improving the Model using Hyperparameters
To further improve the model, we can consider adding more features or exploring different algorithms. We can also collect more data to improve the accuracy of the model.

## Final Results & Recommendations
In conclusion, this analysis provides a good starting point for predicting the quality of apples based on their features. The SVM model performs the best in predicting apple quality based on the given features. Sweetness, juiciness, and acidity are the most important features in determining the quality of the fruit. The size, weight, crunchiness, and ripeness of the fruit also have some impact on the quality.