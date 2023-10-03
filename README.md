# Stroke Prediction
- Author: Deshan Pillay
### Stakeholders:
- The Health and Life Insurance sector
### Business problem:
- The World Health Organization (WHO) have identified that 'Strokes' are the 2nd leading cause of death globally and responsible for 11% of total deaths.
- The Health and Life insurance sectors have provided a dataset of clients information and requires for this data to be analysed, cleaned an build a model to predict the possibility of a client having a stroke based on their information.
- This will allow the business to make an informed decision for calculating a clients Health and Life premiums as well as assisting the client to live a healthier life as a value added benefit.
### Data: The data contains the below information about a client:
- Source: www.kaggle.com
 1   Gender ('M' or 'F')               
 2   Age         
 3   Hypertension (does the client have hypertension 'Y' or 'N')         
 4   Heart disease  (does the client have heart disease 'Y' or 'N')             
 5   Ever married  ('Y' or 'N')               
 6   Work Type ('Self-employes','Private','Government job', 'Never worked', 'children'        
 7   Residence Type ('Rural', 'Urban')
 8   Average glucose level  (average glucose levels in blood)             
 9   BMI  (Body mass index)
 10  Smoking Status (Smokes, never smoked, formerly smoked or Unknown status)             
 11  Stroke ( did the client previously have a stroke)

## Methods
* Load,inspect and clean the data
   - Import required numpy and pandas libaries
   - Check how many rows and columns
   - Verify the datatypes
   - Check for duplicates
   - Identify missing values and address by using a place holder
   - Find and fix inconsistent categories of data
   - Obtain statistics for numerical columns
   - Drop unwanted coloums
     
* Exploratory Data Analysis
   - Use the below statistical analyses to help understand the data
   - Histograms to view the distribution of numerical features
   - Boxplots to view statitical summaries of numerical features
   - Countplots to view the frequency of each class of categorial features
   - Heatmap to view the correlation between features.

* Explanatory Data Analysis
  - Item stroke was used as the target
  - Use univariate visualization to show the distribution of values/categories
  - Use multivariate visualization plotting each feature vs the target

![image](https://github.com/Desh86/Project2/assets/138576166/1c53619a-54a6-4c29-a186-6f2ca4b607ca)
This graph indicates the correlation between having heart disease and smoking.
Its clear that people which have never smoked have a less chance of having heart disease.

Surprisingly people who used to smoke and stopped have heart disease as compared to people who are active smokers.

We also have a number of people on our dataset which we do not have a smoking status data for.

![image](https://github.com/Desh86/Project2/assets/138576166/eb8e4b8f-a1f4-4af9-ad99-da3eaf777385)
The heat map indicates that the onlyfeature  correlation is a patients age, all the other features have a very small to almost no correlation.


* Modeling
  - Decision Tree Classifier 
  - Random Forest Classifier 
  - Baggings Classifier 

* Use GridSearchCV to Hypertune the Three models

* Best tuned model results using Accuracy Metrics:
      Decision Tree Classifier - 0.94% with hypertuning
      Randon Forest Classifier - 0.94% without hypertuning
      Bagging Classifier - 0.937% with hypertuning

* Apply with and without PCA to determine the best model.
  Random Forest and Baggings provided the best results accuracy metrics


* Final production model to be used and recommendations:

  - The PCA models poduced a higher accuracy result as compared to the hypertune models.

  -Two of the 3 PCA models produced high accuracy and were almost identical in results. These PCA models were the Random Forest and Baggings Classifier Models.

  -However even though the Baggings Classifier produced a higher speed vs the Random Forest, the Random Forest Model produced a precsion of 100% as compared to 0.99% of the Baggings Classifier.

  -Since this model will be predicting the possiblities of having a stroke we require the best results therefore I would recommend the PCA Random Forest Classifier Model.
















 
