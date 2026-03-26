# BLENDED LEARNING
# Implementation of Principal Component Analysis (PCA) for Dimensionality Reduction on Energy Data

## AIM:
To implement Principal Component Analysis (PCA) to reduce the dimensionality of the energy data.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement Principal Component Analysis (PCA) for dimensionality reduction on the energy data.
Developed by: PRARTHANA D
RegisterNumber:  212225230213
# Import necessary libraries
import pandas as pd
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA
import matplotlib.pyplot as plt
import seaborn as sns

# Step 1: Load the dataset
data = pd.read_csv("HeightsWeights.csv")

# Step 2: Display first few rows
print("First 5 rows of the dataset:")
print(data.head())

# Step 3: Select features
X = data[['Height(Inches)', 'Weight(Pounds)']]

# Step 4: Visualize original data
plt.figure(figsize=(8, 5))
sns.scatterplot(x='Height(Inches)', y="Weight(Pounds)", data=data)
plt.title("Original Data Distribution")
plt.show()

# Step 5: Standardize the data
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

# Step 6: Apply PCA
pca = PCA(n_components=2)
X_pca = pca.fit_transform(X_scaled)

# Step 7: Explained variance
print("Explained Variance Ratio:", pca.explained_variance_ratio_)

# Step 8: Create PCA Dataframe
pca_df = pd.DataFrame(X_pca, columns=['PC1', 'PC2'])

# Step 9: Plot PCA result
plt.figure(figsize=(6,5))
sns.scatterplot(x='PC1', y='PC2', data=pca_df)
plt.title("PCA Projection of Height and Weight")
plt.xlabel("Principal Component 1")
plt.ylabel("Principal Component 2")
plt.show()
*/
```

## Output:
![simple linear regression model for predicting the marks scored](sam.png)
<img width="1140" height="773" alt="image" src="https://github.com/user-attachments/assets/d69eb526-ae66-4552-99bf-9d4a097d2e27" />

<img width="990" height="650" alt="image" src="https://github.com/user-attachments/assets/c8ecbf78-d24b-43e5-a289-29b2e674fc4f" />


## Result:
Thus, Principal Component Analysis (PCA) was successfully implemented to reduce the dimensionality of the energy dataset.
