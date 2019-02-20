# Heart Disease Prediction with highest accuracy

<img align="right" src="/DSI7_CapstoneProject/Datasets/image.png" width="180">
      
The aim of this project is to predict Heart Disease with the highest accuracy by using different machine learning methods.

For the project I combined 4 different datasets, which are from Cleveland, Switzerland, LongBeach, and Hungary. While the datasets were from different places, there were missing values in some features. Thus, after joining the datasets, and cleaning the data, I made an assumption to increase the disease prediction. My assumption was by predicting the missing values my heart disease prediction accuracy can increase. To test this, I build two different data frames, one with dropped missing values and another by predicting the missing values.

You can find the more detailed analysis and report of the project on Jupyter Notebook Files. 
- [Data Cleaning, Missing Value Prediction and EDA](https://github.com/DidemIscan/DSI7_CapstoneProject/blob/master/DataCleaning%26MissingValuePrediction%26EDA.ipynb)
- [Modelling, Heart Disease Prediciton, Comparison and Conslusion](https://github.com/DidemIscan/DSI7_CapstoneProject/blob/master/Modelling%26HeartDiseasePrediction.ipynb)


## Predicting Missing Values

After cleaning the data, I predicted the missing values. I did two different approaches to predict the missing values:
1.	Predicting the missing values by using the whole dataset.
2.	Predicting the missing values by splitting the dataset into four different data frames; healthy female, unhealthy female, healthy male, unhealthy male.

For both approaches, I started predicting the smallest number of missing valued column and each step I added the new column to my data frame. For each missing value prediction, I used GridSearch, and chose the best scored model to do the prediction.

For both approaches, I predicted heart disease and chose the highest accurate disease prediction. As a result, predicting missing values by separating the dataset into four categories was a better approach to predict missing values, which increased the accuracy of heart disease prediction at the end. On Jupyter Notebook you can find the analysis of the second approach. 


## Finding the Best Model to Predict Heart Disease

To predict the heart disease, I used approximately 18 different classification models and compared their results to find the best prediction. 


### Improving the Prediction Accuracy

After modelling I tested two different assumptions. 
- Choosing the most related columns will increase the prediction accuracy scores 
- Dropping vs Predicting Missing Values  
  
  
## Conclusion

As a result, predicting the missing values do increase the disease prediction accuracy. Additionally, using different modelling for the dataset will help us see different methods and increase the accuracy of our analysis at the end.


### Next Steps

All in all, the project was a success. 

If I can collect more data from new subjects, I can improve my analysis and predict more specific heart diseases. After the disease prediction I can give recommendations for each subject, such as work out or diet plans, medicine, doctor or more test recommendation. Additionally, I can add descriptions, where subject can understand which disease they have and know how to proceed in the future. 


### Risks

- Small dataset.
- The correlation between the columns are not very high, while there were many missing values.

To solve these risks, we can collect more data and increase our number of subjects. The prediction accuracy can increase very easily. 


## Why heart disease prediction? 

This project got my interest because of my passion in healthcare and making an impact on people. One day this project can have an impact on people’s life which makes me proud. People are suffering from heart disease all around the world, and I believe this project has a future. It can be improved even more by working with doctors and enhance the work environment. It can increase the time efficiency and decrease wrong diagnosis, which can help many people. 


## Author

* **Didem Iscan** - *Data Scientist* - [DidemIscan](https://github.com/DidemIscan)

## Acknowledgments

I found this dataset from dataworld (link: https://data.world/xprizeai-health/heart-disease). 
During my analysis, I found different models that I can use for my modelling on Kaggle(link: https://www.kaggle.com/danimal/heartdiseaseensembleclassifier).


