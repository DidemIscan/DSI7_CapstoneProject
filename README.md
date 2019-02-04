# Heart Disease Prediction with highest accuracy

The aim of this project is to predict Heart Disease with the highest accuracy by using machine learning methods.

For the project I combined 4 different datasets, which are from Cleveland, Switzerland, LongBeach, and Hungary. While the datasets were from different places, there were missing values in some features. Thus after joining the datasets, and cleaning the data, I made an assumption to increase the disease prediction. My assumption was by predicting the missing values my heart disease prediction accuracy can increase. To test this I build two different data frames, one with dropped missing values and another by predicting the missing values.

You can find the more detailed analysis and report of the project on Jupyter Notebook File. 


## Data Description

In the dataset I have 2 different types of variables:
- Continuous Variables: suject id, age, trestpbs, chol, thalach, oldpeak
- Categorical Variables: sex, cp, fbs, restecg, exang, slop, ca, thal, pred_attribute, origin

    - subject_id: Id number of the subject
    - age: Age in years
    - sex: Female = 0, Male = 1 
    - cp: Chest pain type (value1:Typical angina, value2: Atypical angina, value3: Non-anginal pain, value4: Asymptomatic)
    - trestbps: Resting blood pressure (in mm Hg on admission to the hospital)
    - chol: Serum cholestoral in mg/dl
    - fbs: fasting blood sugar (1 = True, 0 = False)
    - restecg: Resting electrocardiographic results (value0: Normal, value1: Having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV), value2: Showing probable or definite left ventricular hypertrophy by Estes' criteria)
    - thalach: Maximum heart rate achieved
    - exang: Exercise induced angina (1 = Yes, 0  = No)
    - oldpeak: ST depression induced by exercise relative to rest
    - slop: The slope of the peak exercise ST segment (value1: Upsloping, value2: flat, value3: Downsloping)
    - ca: Number of major vessels (0-3) colored by flourosopy
    - thal: Thalium heart scan (3 = normal (no cold spots), 6 = fixed defect (cold spots during rest and exercise), 7 = reversible defect (when cold spots only appear during exercise))
    - pred_attribute: The predicted attribute, diagnosis of heart disease (angiographic disease status) (value0: < 50% diameter narrowing, value1: > 50% diameter narrowing (in any major vessel: attributes 59 through 68 are vessels))
    - origin: The origin place of the subject

## Predicting Missing Values

After cleaning the data I predicted the missing values, by building a small dataset with the non-null columns. I started predicting the smallest number of missing valued column and each step I added the new column to my data frame. 

I did the predictions by using GridSearch method, where I checked which model is giving me the best score 


## Finding the Best Model 

To predict the heart disease, I used approximately 18 different classification models and compared their results to find the best prediction. 

### Imporving the Prediction Accuracy

After modelling I tested my 2 assumptions. 
- By choosing the most related columns, we can the prediction scores can increase
- Dropping vs Predicting Missing Values


1. Choosing the Related Columns

    After the modelling I made my second assumption, by decreasing the number of columns, and only using the most related features the disease prediction accuracy may increase. To find that out, I checked the correlation between each column, and checked the feature importance by using decision tree, random forest, and bagging models. As a result I picked 6 columns (oldpeak, exang, slop, cp, thalach, chol) with the best relation, and ran my model again. This assumption was a fail, while the prediction accuracy scores decreased. The reason of this can be because in each model they check every feature seperately and give them different importance value, even the relationship is low they all can have an affect on the prediction. Thus choosing the related columns did not help to increase the disease prediction accuracy. 

2. Comparison 

    Before comparing the scores for both data frames, first I needed to select the best model. To find that first I chose the highest 5 models then did GridSearch to see by changing the parameters can we increase the score and also find best model. The models that I picked were Support Vector Machine, Multilayer Perceptron, RBF SVM, k-Nearest Neighbors, Bagging Classifier, and Logistic Regression. 
    
    The analysis showed that Multilayer Perceptron (neural network analysis) was the best model to predict a heart disease. After picking the best model I compared both the datasets, and my second assumption was correct. By predicting the missing values the prediction accuracy increased. 
    
    
## Conclusion

From the analysis, we can see that predicting the missing values can slightly increases the disease prediction accuracy. On the other hand using different modelling for the dataset will help us see different methods and increase the accuracy of our analysis at the end. 



### Next Steps

All in all the project was a success. Next I am planning to increase the accuracy by changing the method of my predicting missing values. I will do the missing value prediction by seperating the data frame into sex, age range, and diseased categories. By that the missing values of each column will be compared in its own category, which can predict the missing values more accuractely.

Additionally if I can collect more data from new subjects I can improve my analysis and predict more specific heart diseases. After the disease prediction I can give recommendations for each subject, such as work out, do a diet, see a doctor, take some tests & see the doctor, get medicine, etc. Additionally I can add decsriptions, where subject can understand what these diseases are and how they can proceed in the future. 

### Risks

- Small dataset.
- The correlation between the columns are not very high, while there were many missing values.

To solve these risks, we can collect more data and increase our number of subject. The prediction accuracy can increase very easily. 


## Author

* **Didem Iscan** - *Data Scientist* - [DidemIscan](https://github.com/DidemIscan)

## Acknowledgments

I found this dataset from dataworld (link: https://data.world/xprizeai-health/heart-disease). 
During my analysis, I found different models that I can use for my modelling on Kaggle(link: https://www.kaggle.com/danimal/heartdiseaseensembleclassifier).
