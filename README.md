# Credit-Card-Fraud-Detection

## The Dataset :

The data was taken from Kaggle site : https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud .

The Columns do not have physical significance directly visible since as per the source (Kaggle) , the data was compressed using Principle Component Analysis (PCA) in order to protect the privacy of the individuals while making a realistic secnario dataset availaible to public . 

## Data Preprocessing and Visualisation :

### Univariate distribution of classes

<img width="505" alt="Screenshot 2023-08-18 225519" src="https://github.com/soham583/Credit-Card-Fraud-Detection/assets/66030548/e80aee9a-fb50-4a7c-ab68-af5b71695241">

### Normalization

distribution before normalization

<img width="503" alt="Screenshot 2023-08-18 225552" src="https://github.com/soham583/Credit-Card-Fraud-Detection/assets/66030548/13273208-4fe0-4c9d-8eca-7f438d738517">

distribution after normalization

<img width="513" alt="Screenshot 2023-08-18 230004" src="https://github.com/soham583/Credit-Card-Fraud-Detection/assets/66030548/ad8be7fe-5719-497c-a9d0-9d03f8b1b475">

###  Correlation

correlation matrix

<img width="424" alt="Screenshot 2023-08-18 225454" src="https://github.com/soham583/Credit-Card-Fraud-Detection/assets/66030548/87545733-0ab7-4803-a886-b2d8cb274bec">


classes arranged in ascending order of correlation with target class:

<img width="341" alt="Screenshot 2023-08-18 230021" src="https://github.com/soham583/Credit-Card-Fraud-Detection/assets/66030548/0d62231a-e677-40ef-97f8-e661ce0a4a77">


## Class imbalance in dataset

Dataset we ae using is highly imbalanced with very free transaction labeled as Fraud. To handle such dataset we mainly use two techniques\
first, Undersampling and second Oversampling.\
For Undersampling we are using "Tomek Links" method and for Oversampling we are using "SMOTE" method

<img width="173" alt="Screenshot 2023-08-18 234426" src="https://github.com/soham583/Credit-Card-Fraud-Detection/assets/66030548/07a0c714-596c-48cc-8ed0-c10b67aed70a">

## Model selection

For model we are using four algorithms:
1. Random Forest
2. Logistic Regression
3. Decision Tree
4. Gradient Boosting

combining with Tomek, SMOTE and combination of both

Results are as follows:

<img width="324" alt="Screenshot 2023-08-18 230509" src="https://github.com/soham583/Credit-Card-Fraud-Detection/assets/66030548/5a5c85fb-f772-4b17-80c2-078196fc8ca2"> \

<img width="351" alt="Screenshot 2023-08-18 230521" src="https://github.com/soham583/Credit-Card-Fraud-Detection/assets/66030548/b9ec61a9-dcde-490c-95ec-e6a7b198140f"> \

<img width="354" alt="Screenshot 2023-08-18 230529" src="https://github.com/soham583/Credit-Card-Fraud-Detection/assets/66030548/f5ebb1d9-603c-4a17-ad20-31ce9ab6235a"> \

<img width="374" alt="Screenshot 2023-08-18 230540" src="https://github.com/soham583/Credit-Card-Fraud-Detection/assets/66030548/5b97ef68-2aa6-4f75-82e1-74ac003bafab"> \

"Accuracy" matrix is not relevant as random guess have prob of more than 99% to be "not Fraud"\

For selecting model we are using "Recall" value rather than "Accuracy" or "Precision" as we don't want to leave any "fraud" transaction to label as "not fraud". \
Therefore we will select model with high recall value which is result of low "False Negative"\ and Decent "Precision"

So final model is following:

<img width="342" alt="Screenshot 2023-08-18 230551" src="https://github.com/soham583/Credit-Card-Fraud-Detection/assets/66030548/fe0f10da-c6a9-4103-8615-b4881fa8e574">

