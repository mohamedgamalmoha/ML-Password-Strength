# Password Strength

## Project Description:
Passwords are an essential part of system security. Though there are many alternatives to passwords for access control,
in many applications, the password is the more compellingly authenticating the identity. 
Password strength meters provide quick and easy visual feedback on what makes a strong password. A small meter indicates 
how strong a proposed password is when creating a new account or changing passwords.\
Our abroach aims to develop a password strength checker that determines the strength of a password. Some popular 
password strength algorithms predict the strength of password using machine learning algorithms. A password strength 
checker analyzes the combination of digits, letters, and special symbols in your password. It is generated by training a 
machine learning model on a labelled dataset of different password combinations of letters and special symbols.\
The model learns from data which combinations of letters and symbols are considered strong or weak passwords. So, to 
create an application that checks the strength of passwords, we need a labelled dataset containing various combinations 
of letters and symbols.\
Our dataset is from Kaggle, it is used for training a machine learning model to predict the strength of a password. We can use that information for this task. What distinguishes our 
approach from other strength meters? To begin with, it is completely based on machine learning rather than rules. Second, 
It is only saved passwords that were marked as weak “0”, medium “1”, or strong “2” by all three strength meters. 
This implies that all the passwords were either weak, medium, or strong.

## Data Source
The passwords used in our analysis are from the 000webhost leak that is available online. A tool called PARS by Georgia 
Tech university has all the commercial password meters integrated into it and is used to determine the strength of the 
passwords. [Data Link](https://www.kaggle.com/datasets/bhavikbb/password-strength-classifier-dataset)

## Data Info

Dataset has the following columns:
- **password**:   String contains sequence of letters, numbers, and special characters ... etc. 
- **strength**:   A categorical column that has a value form 0 to 2, 0 for weak, 1 for medium, 2 for strong.

Here is a snapshot of the data

|  password   | strength |
|:-----------:|:--------:|
|  kzde5577   |    1     |
|  kino3434   |    1     |
|  visi7k1yr  |    1     | 
|  megzy123   |    1     |
| lamborghin1 |    1     |

The data is **incorrect** format, so it needs some modification to process easily. Here is a snapshot after modifications: 

|  password   | strength | length | small | capital | special | numeric |
|:-----------:|:--------:|:------:|:-----:|:-------:|:-------:|:-------:|
|  kzde5577   |    1     |   8    |   4   |    0    |    0    |    4    |
|  kino3434   |    1     |   8    |   4   |    0    |    0    |    4    |
|  visi7k1yr  |    1     |   9    |   7   |    0    |    0    |    2    |
|  megzy123   |    1     |   8    |   5   |    0    |    0    |    3    |
| lamborghin1 |    1     |   11   |  10   |    0    |    0    |    1    |

## Data Exploration
To explore more about data, the following questions need to be answered:
  - What is the distribution of strength column?
  - What is the distribution of length column?
  - What is the distribution of small column?
  - What is the distribution of capital column?
  - What is the distribution of special column?
  - What is the distribution of numeric column?

## Data Preprocessing
  - Set up the data with required columns
  - Split data into train set & test set
  - Scaling using standard scaler

## Applying ML Methods  
### Decision Tree Classifier
   1. Fitting DecisionTreeClassifier Model
   2. Plotting the tree
   3. Classification report (precision, recall, f1-score)
   4. Confusion matrix & Heatmap
### Logistic Regression
   1. Fitting DecisionTreeClassifier Model
   2. Plotting the tree
   3. Classification report (precision, recall, f1-score)
   4. Confusion matrix & Heatmap
### Linear Support Vector Classifier
   1. Fitting DecisionTreeClassifier Model
   2. Plotting the tree
   3. Classification report (precision, recall, f1-score)
   4. Confusion matrix & Heatmap

## References
  - [link 1](https://www.ijitee.org/wp-content/uploads/papers/v11i8/H91190711822.pdf )
  - [link 2](https://www.researchgate.net/publication/232653407_Password_Strength_Prediction_Using_Supervised_Machine_Learning_Techniques)
  - [link 3](https://www.academia.edu/44786310/IJERT_Real_Time_Password_Strength_Analysis_on_a_Web_Application_Using_Multiple_Machine_Learning_Approaches)
  - [link 4](https://www.ijert.org/real-time-password-strength-analysis-on-a-web-application-using-multiple-machine-learning-approaches )
  - [link 5](https://www.blaseur.com/papers/login2017-better-passwords.pdf)


