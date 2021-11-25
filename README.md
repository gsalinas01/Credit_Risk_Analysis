# Credit_Risk_Analysis
## Overview
The purpose of this analysis was to create and analyze different machine learning models to assess individual credit risk. In this analysis, we employed different techniques to train and evaluate models with unbalanced classes. We used imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

## Results
The results of this analysis are mainly highlighted by the Balanced Accuracy Score and the Imbalanced Classification Reports (ICR).
I will begin with the model that gave us the worst score, and resume with the next in ascending order to the model that performed best. 
  * **Undersampling** - undersampling the data using the Cluster Centroids algorithm generated the worst performance. With a balanced accuracy score of about 0.53, this model is hardly ideal in assessing credit risk. Additionally, in the ICR, an average f1 score of about 0.56 is equally underperforming and could be improved with different techniques.
![UndersamplingBAS](https://user-images.githubusercontent.com/60943801/143492817-9b432143-f649-4f84-9c05-d9008d57eb0d.png)
![UndersamplingICR](https://user-images.githubusercontent.com/60943801/143492829-e3a5403e-b1f5-434b-917e-8346cdbf5f09.png)
  * **Combination (Over and Under) Sampling** - testing a combination over- and under-sampling algorithms using the SMOTEENN algorithm gave better scores than the Undersampling method above. With a balanced accuracy score of about 0.649 and average f1 score of about 0.72, the combination sampling method is second best in this overall analysis.
![CombinationBAS](https://user-images.githubusercontent.com/60943801/143493598-766d5a41-1de5-4f03-ba5a-394835a2a952.png)
![CombinationICR](https://user-images.githubusercontent.com/60943801/143493608-213c6f9a-5ac5-4287-bc51-b862d0913489.png)
  * **SMOTE Oversampling** - Oversampling the data using the SMOTE algorithm came in third. This method returned a balanced accuracy score of about 0.654, slightly better than the combination sampling, and an f1 score of 0.81.
![SMOTEOversampling](https://user-images.githubusercontent.com/60943801/143494159-4b49ed5b-7973-4bbb-8dd9-0a723994ee07.png)
![SMOTEOversamplingICR](https://user-images.githubusercontent.com/60943801/143494170-89f976b4-4dcd-4b6d-9492-76bd48f86869.png)
  * **Naive Random Oversampling** - using the naive random oversampling algorithm generated better results. With a balanced accuracy score of 0.687, it was the best BAS of the previous methods. Still, it could be improved to more accurately predict credit risk. 
![NaiveOverBAC](https://user-images.githubusercontent.com/60943801/143494530-457a65d5-d3cf-4fc9-bf23-e62a77b5b00d.png)
![NaiveOverICR](https://user-images.githubusercontent.com/60943801/143494535-e1b5c6cb-9a29-40c2-899c-4ebb51395d0c.png)
  * **Balanced Random Forest Classifier** - using ensemble algorithms generated the best models for this analysis overall. Training a Balanced Random Forest Classifier gave us a BAS of 0.779, and an f1 score of about 0.93, which means it was about 77% accurate in predicting credit risk.
![BRFC-BAS](https://user-images.githubusercontent.com/60943801/143494991-46ea250b-bd94-431f-a2de-646900d13d24.png)
![BRFC-ICR](https://user-images.githubusercontent.com/60943801/143494994-68c763b1-206a-43c9-9053-60922dbeaae1.png)
  * **Easy Ensemble AdaBoost classifier** - the best performing model was the Easy Ensemble AdaBoost classifier, which generated a BAS of 0.93 and an f1 score of 0.97. 
![EAB-BAS](https://user-images.githubusercontent.com/60943801/143495224-32c0d77c-3ab4-4382-9267-72b417d3ee24.png)
![EAB-ICR](https://user-images.githubusercontent.com/60943801/143495230-f96cc71c-a39b-45ed-97ec-eb31e05ce8ac.png)

## Summary
This analysis was very challenging to complete. The methods utilized gave me the opportunity to learn about different techniques that a company might use to assess credit risk. While the best performing model was the Easy Ensemble AdaBoost Classifier, I am unsure of whether this would function in a real-world example as there was a limited amount of data in this example, and a company with investors and stakeholders to consider might require the use of methods with higher accuracy scores. 
