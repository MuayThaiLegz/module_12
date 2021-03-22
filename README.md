# Module 12 Challenge

# Explination

* In this Challenge, you’ll use various techniques to train and evaluate models with imbalanced classes. Use a logistic regression model to compare two versions of the dataset. First, you’ll use the original dataset. Second, you’ll resample the data by using the RandomOverSampler module from the imbalanced-learn library.

---

* Technologies 

# Pandas
We used Pandas

* We read the CSV file into a Pandas DataFrame. `pd.read_csv`.
* We manipulated dataframes with Pandas methods. `X_features = panda_df.drop(columns=['loan_status'])`.
* Using Pandas methods on our dataframes. `y_labels.value_counts()`.

* Pandas Examples 
---
```
# Read the CSV file from the Resources folder into a Pandas DataFrame
panda_df = pd.read_csv('./Resources/lending_data.csv')
# YOUR CODE HERE!

# Review the DataFrame
# YOUR CODE HERE!
panda_df.head()

---

# Separate the X variable, the features
# YOUR CODE HERE!
X_features = panda_df.drop(columns=['loan_status'])

---

# Rename the columns
importances_df = importances_df.rename(columns={0: 'Feature', 1: 'Importance'})

# Set the index
importances_df = importances_df.set_index('Feature')

# Sort the dataframe by feature importance
importances_df = importances_df.sort_values(by='Importance',ascending=False)

```
---
https://pandas.pydata.org/
Package overview
pandas is a Python package providing fast, flexible, and expressive data structures designed to make working with “relational” or “labeled” data both easy and intuitive. It aims to be the fundamental high-level building block for doing practical, real-world data analysis in Python. Additionally, it has the broader goal of becoming the most powerful and flexible open source data analysis/manipulation tool available in any language. It is already well on its way toward this goal.

![Pandas](https://miro.medium.com/max/819/1*Dss7A8Z-M4x8LD9ccgw7pQ.png)

---
# Scikit-learn
We used Scikit-learn 

* We created a `LogisticRegression` with the Original Data
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

---

# Import the LogisticRegression module from SKLearn
from sklearn.linear_model import LogisticRegression

# Instantiate the Logistic Regression model
# Assign a random_state parameter of 1 to the model
# YOUR CODE HERE!

lr = LogisticRegression(random_state=1)
lr

# Fit the model using training data
# YOUR CODE HERE!
lr.fit(X_train, y_train)

y_pred = lr.predict(X_test)

---

# Generate a confusion matrix for the model
# YOUR CODE HERE!
confusion_matrix(model_prediction,y_test)

# Print the classification report for the model
# YOUR CODE HERE!
print(classification_report(model_prediction,y_test))
```
---

https://scikit-learn.org/stable/
Scikit-learn provides a range of supervised and unsupervised learning algorithms via a consistent interface in Python.

![Scikit](https://miro.medium.com/max/866/1*1ouD8HMkmJffNSAMfvBSkw.png)

---
