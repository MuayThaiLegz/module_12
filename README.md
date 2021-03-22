# Module 12 Challenge

* In this Challenge, you’ll use various techniques to train and evaluate models with imbalanced classes. Use a logistic regression model to compare two versions of the dataset. First, you’ll use the original dataset. Second, you’ll resample the data by using the RandomOverSampler module from the imbalanced-learn library.

---

* Technologies 

# Pandas
We used Pandas

Importing the data.
Creating dataframes with Pandas methods.
Using Pandas methods on our dataframes.
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
# Seaborn
We used Seaborn 

In creating statistical graphics 
The heatmap to display correlations in our data. To plot detail 
It help fortifine our inital ideas in visual form.
---
```
sns.catplot(
    x='Total Liabilities',
    y= "Total Current Assets",
    hue="Ticker",
    kind="bar",
    data=isolated_companies_full_data.reset_index(),
    aspect=4)
```
---
https://seaborn.pydata.org/
Seaborn is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.

![seaborn](https://livecodestream.dev/post/how-to-build-beautiful-plots-with-python-and-seaborn/featured_hue585f61b28a74a671118de43150c5d63_166173_680x0_resize_q75_box.jpg)

---

# Scikit-learn
We used Scikit-learn 

* We created a `Logistic Regression Model` with the Original Data
* We split the data into training and testing datasets by using `train_test_split`.
* Printed `classification_report & confusion_matrix`.
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
