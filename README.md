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
balance_sheet_tanglibles.groupby(level=0).plot.bar(
    title= ('Displays[balance_sheet_tanglibles] per Company'),
    figsize=(17,13),
    rot =360, 
    grid =True, 
    fontsize = 13)
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

We used StandardScaler to scale our data as needed.
We used PCA to decompose our data down in dimensions. 
We used Kmeans as our ML Algo.
---
```
# Initialize the K-Means model

second_model4 = KMeans(n_clusters=4, random_state=1)

# Fit the model

second_model4.fit(scaled_data_pca_data)

# Predict clusters
second_model4 = second_model4.predict(scaled_data_pca_data)

# View the resulting array
second_model4
```
---


https://scikit-learn.org/stable/
Scikit-learn provides a range of supervised and unsupervised learning algorithms via a consistent interface in Python.

![Scikit](https://miro.medium.com/max/866/1*1ouD8HMkmJffNSAMfvBSkw.png)

---
