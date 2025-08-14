# DataCleaning-MachineLeaning

## Reflection
On 8/13/25 I have completed cleaning the life-expentacy csv file. This process was based on the video <a href="https://youtu.be/GP-2634exqA?si=N3yL0FToekCeZ6SL">🚀 Data Cleaning/Data Preprocessing Before Building a Model - A Comprehensive Guide</a>.
From that video I learned that there's a system when cleaning data. Or rather what should I be looking for in that dataset. For one is that I shouldn't dive into the dataset, and just "clean up" because what am I "cleaning up"? My last attempt on the machine learning project under <a href="https://github.com/ProjectJerryLucasArguello/Machine-Learning-Experiential.git">Machine Learning Experimental</a> I wasn't cleaning up the data with a clear goal in mind for my machine learning model. Like the whole purpose of cleaning data from what I understand is to isolate certain variables and look at certain target variables. Here it was me looking at this nyc housing price dataset and was like "Okay I want to look at this! No! That! This and that this and this and..!" It was just me going about it with no clear answer. The video taht I followed showed me there are multiple things to consider when cleaning data. For instance what is the shape of the data? Are there any outliers? Is there some encoding we should add for the sake of our model? Though tedious these question are quite important to ask ones self when building a machine learning model. Not just that when actually looking at the data and making well-educated conclusions.

## What I Learned

### One Hot-Encoding
One-hot encoding is a data preprocessing technique in machine learning used to convert categorical variables into a numerical format that algorithms can interpret without introducing unintended ordinal relationships. In this method, each unique category in a feature is represented as a separate binary vector (array) of length equal to the total number of categories. Within this vector, all positions are set to 0 except for the position corresponding to the category being represented, which is set to 1. For example, if a “color” feature contains the values {Red, Green, Blue}, one-hot encoding would transform “Red” into [1, 0, 0], “Green” into [0, 1, 0], and “Blue” into [0, 0, 1]. This avoids the issue that would arise if categories were simply assigned numeric labels like 0, 1, 2, which could imply a false ordinal relationship (e.g., that Green is somehow “greater” than Red). One-hot encoding is especially important for algorithms like logistic regression, k-nearest neighbors, and neural networks, which assume numerical values have meaningful distance relationships. However, it increases the dimensionality of the dataset, particularly when a feature has many unique categories, which can lead to higher memory usage and longer training times — a challenge sometimes addressed by alternative encoding methods like target encoding or embeddings. 

This video best sumamrizes the idea of one-hot encoding and dummy variables: <a href="https://youtu.be/9yl6-HEY7_s?si=dtSZ2s_PWehTwvNQ">One Hot-Encoding and Dummy Variables on Youtube</a>

### 1.5×IQR Rule for Outlier Detection

The **1.5×IQR rule** is a statistical method for detecting outliers in a dataset.

---

#### Steps

1. **Find Q1 and Q3**  
   - **Q1** (first quartile): value below which 25% of the data falls  
   - **Q3** (third quartile): value below which 75% of the data falls  

2. **Calculate the IQR**  
      IQR = Q3 - Q1
