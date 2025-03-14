# Credit-Card-capstone

The dataset can be download using this link: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
# Problem statement
The objective of this project is to predict fraudulent credit card transactions using machine learning models.  

We will analyze customer-level data collected through a research collaboration between Worldline and the Machine Learning Group.  

The dataset, sourced from the Kaggle website, contains 284,807 transactions, with 492 identified as fraudulent. Given the significant class imbalance, appropriate techniques must be applied to address it before building the model.

### Business Problem Overview  

For banks, retaining highly profitable customers is a top priority. However, banking fraud presents a major challenge, leading to significant financial losses and damaging both trust and credibility for financial institutions and their customers.  

According to the Nilson Report, banking fraud was projected to reach $30 billion worldwide by 2020. With the increasing adoption of digital payment channels, fraudulent transactions are also rising, employing more sophisticated methods.  

In the banking sector, credit card fraud detection using machine learning is no longer just a trend—it has become essential. Machine learning enables proactive fraud monitoring and prevention, helping financial institutions minimize time-consuming manual reviews, costly chargebacks, fees, and the rejection of legitimate transactions.

**Understanding and Defining Fraud** 
Credit card fraud is any dishonest act and behaviour to obtain information without the proper authorization from the account holder for financial gain. Among different ways of frauds, Skimming is the most common one, which is the way of duplicating of information located on the magnetic strip of the card. Apart from this, the other ways are:

# Manipulation/alteration of genuine cards
# Creation of counterfeit cards
# Stolen/lost credit cards
# Fraudulent telemarketing
# Data Dictionary


### Data Overview and Processing Steps

The dataset consists of credit card transactions made by European cardholders over a two-day period in **September 2013**. Out of **284,807** total transactions, only **492** were identified as fraudulent, making up just **0.172%** of the data. Given this extreme imbalance, special handling is required before model development.  

To maintain confidentiality, **Principal Component Analysis (PCA)** was applied to transform most features. Except for **‘time’** and **‘amount’**, all other features (**V1 to V28**) represent principal components derived through PCA. The **‘time’** feature records the elapsed seconds between the first transaction and subsequent transactions, while **‘amount’** indicates the transaction value. The **‘class’** feature serves as the target variable, where **1** denotes fraudulent transactions and **0** represents non-fraudulent ones.  

---

### Data Understanding  
The first step involves loading the dataset and gaining insights into its features. This understanding will help in selecting the most relevant features for model training.  

---

### Exploratory Data Analysis (EDA)  
EDA involves **univariate and bivariate analysis** to explore data distributions, correlations, and patterns. Since the dataset consists of Gaussian variables, **Z-scaling is not required**. However, checking for skewness and addressing it, if present, is essential to ensure effective model performance.  

---

### **Train/Test Split**  
To evaluate model performance on unseen data, we will split the dataset into **training and testing sets**. **k-fold cross-validation** will be used for validation, ensuring that the minority class (fraud cases) is adequately represented in each test fold.  

---

### Model Building & Hyperparameter Tuning 
In this phase, different machine learning models will be tested, and their hyperparameters will be fine-tuned to achieve optimal performance. Various **sampling techniques** may also be explored to handle data imbalance and improve fraud detection accuracy.  

---

### Model Evaluation
Choosing the right evaluation metric is crucial due to the imbalanced nature of the dataset. Since identifying fraudulent transactions accurately is more critical than detecting non-fraudulent ones, we must select a metric that effectively reflects this business goal. **Precision, recall, F1-score, and AUC-ROC** are potential evaluation metrics to assess the model’s effectiveness.
