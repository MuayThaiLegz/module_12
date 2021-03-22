# Module 12 Challenge

# Explination

* In this Challenge, you’ll use various techniques to train and evaluate models with imbalanced classes. Use a logistic regression model to compare two versions of the dataset. First, you’ll use the original dataset. Second, you’ll resample the data by using the RandomOverSampler module from the imbalanced-learn library.

---

* Technologies 

# Pandas
We used Pandas

Importing the data.
Creating dataframes with Pandas methods.
Using Pandas methods on our dataframes.

* Pandas Examples 
---
```
# Read the CSV file from the Resources folder into a Pandas DataFrame
panda_df = pd.read_csv('./Resources/lending_data.csv')
# YOUR CODE HERE!

# Review the DataFrame
# YOUR CODE HERE!
panda_df.head()
```
---
https://pandas.pydata.org/
Package overview
pandas is a Python package providing fast, flexible, and expressive data structures designed to make working with “relational” or “labeled” data both easy and intuitive. It aims to be the fundamental high-level building block for doing practical, real-world data analysis in Python. Additionally, it has the broader goal of becoming the most powerful and flexible open source data analysis/manipulation tool available in any language. It is already well on its way toward this goal.

![Pandas](https://miro.medium.com/max/819/1*Dss7A8Z-M4x8LD9ccgw7pQ.png)

---
# Scikit-learn
We used Scikit-learn 

* We created a `Logistic Regression Model` with the Original Data
* We split the data into training and testing datasets by using `train_test_split`.
* Printed `classification_report & confusion_matrix`.

* Scikit-learn Examples
 ---
```
# Import the train_test_learn module
from sklearn.model_selection import train_test_split

# Split the data using train_test_split
# Assign a random_state of 1 to the function
# YOUR CODE HERE!
X_train, X_test, y_train, y_test = train_test_split(X_features, y_labels, random_state=1)
```
---

https://scikit-learn.org/stable/
Scikit-learn provides a range of supervised and unsupervised learning algorithms via a consistent interface in Python.

![Scikit](https://miro.medium.com/max/866/1*1ouD8HMkmJffNSAMfvBSkw.png)

---
