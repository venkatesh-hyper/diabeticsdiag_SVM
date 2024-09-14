# diabeticsdiag_SVM

import pandas as pd 
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.svm import SVC
from sklearn.metrics import accuracy_score, classification_report

# testing using 
    # New patient's data (input should be in the same order as the dataset's columns)
      new_data = [[5, 160, 60, 30, 60, 38.5, 0.9, 40]]
      new_data_scaled = scaler.transform(new_data)
      new_prediction = svm_model.predict(new_data_scaled)
      if new_prediction[0] == 1:
          print("The model predicts that the patient has diabetes.")
      else:
          print("The model predicts that the patient does not have diabetes.")

  
replace new data with testing patient data based on this category 
new data =[[ Pregnancies , Glucose , BloodPressure , SkinThickness , Insulin , BMI ,  DiabetesPedigreeFunction , Age ]]

# two type of split 
     80 20 split
     60 40 split

# 80 20 split 
        Accuracy: 76.95%
                    Classification Report:
              precision    recall  f1-score   support
                       0       0.81      0.85      0.83       206
                       1       0.67      0.60      0.63       102
                accuracy                           0.77       308
               macro avg       0.74      0.73      0.73       308
            weighted avg       0.76      0.77      0.77       308
              Training Accuracy: 82.17%
              Testing Accuracy: 76.95%

# 60 40 split 
      Accuracy: 75.32%
                Classification Report:
                      precision    recall  f1-score   support
                   0       0.79      0.85      0.82        99
                   1       0.68      0.58      0.63        55
            accuracy                           0.75       154
           macro avg       0.73      0.72      0.72       154
        weighted avg       0.75      0.75      0.75       154
                    Training Accuracy: 82.57%
                    Testing Accuracy: 75.32%

# Decision Tree
        Decision Tree Training Accuracy: 100.00%
        Decision Tree Testing Accuracy: 70.45%
        Classification Report for Decision Tree:
                      precision    recall  f1-score   support
                   0       0.81      0.73      0.77       206
                   1       0.55      0.65      0.59       102
            accuracy                           0.70       308
           macro avg       0.68      0.69      0.68       308
        weighted avg       0.72      0.70      0.71       308
