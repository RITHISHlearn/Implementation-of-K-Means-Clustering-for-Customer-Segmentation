# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages using import statement.

2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

3.Import KMeans and use for loop to cluster the data.

4.Predict the cluster and plot data graphs.

5.Print the output and end the program.

   
## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: RITHISH P
RegisterNumber:  212223230173


import numpy as np

import pandas as pd


import matplotlib.pyplot as plt

data=pd.read_csv("Mall_Customers.csv")


data.head()


data.info()


data.isnull().sum()


from sklearn.cluster import KMeans

wcss=[]


for i in range (1,11):

kmeans=KMeans(n_clusters = i,init="k-means++")

kmeans.fit(data.iloc[:,3:])

wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)

plt.xlabel("No. of clusters")

plt.ylabel("wcss")

plt.title("Elbow matter")

km=KMeans(n_clusters=5)

km.fit(data.iloc[:,3:])

y_pred=km.predict(data.iloc[:,3:])

y_pred


data["cluster"]=y_pred

df0=data[data["cluster"]==0]

df1=data[data["cluster"]==1]

df2=data[data["cluster"]==2]

df3=data[data["cluster"]==3]

df4=data[data["cluster"]==4]

plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-

100)"],c="red",label="cluster0")

plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-

100)"],c="black",label="cluster1")

plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-

100)"],c="blue",label="cluster2")

plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-

100)"],c="green",label="cluster3")

plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-

100)"],c="magenta",label="cluster4")



plt.legend()

plt.title("Customer Segmets")

*/
```

## Output:
## DATASET:

![Screenshot 2024-04-17 040154](https://github.com/RITHISHlearn/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145446645/b977b18f-1b23-482c-a864-64727f609557)


## data.head():

![Screenshot 2024-04-17 040206](https://github.com/RITHISHlearn/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145446645/763edb6d-1ab6-4228-a21c-11c7934bf2ca)


## data.info():

![Screenshot 2024-04-17 040218](https://github.com/RITHISHlearn/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145446645/3c331df5-833b-4b74-ac98-c638cb3ce36b)


## data.isnull() & sum():

![Screenshot 2024-04-17 040230](https://github.com/RITHISHlearn/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145446645/42cfa1ef-ef73-409f-ac02-0e7a63f47b6c)


## Elbow method graph:

![Screenshot 2024-04-17 040243](https://github.com/RITHISHlearn/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145446645/b3a124bd-d2b0-4efc-b4a6-f7a5f122c04d)


## K means cluster:

![Screenshot 2024-04-17 040253](https://github.com/RITHISHlearn/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145446645/4567f9f3-66db-4aa8-82e6-6318af2e7280)


## Y_prediction value:

![Screenshot 2024-04-17 040306](https://github.com/RITHISHlearn/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145446645/79ea12f0-7528-46fc-96d4-498f3677200f)


## Customers Segments Graph:

![Screenshot 2024-04-17 040316](https://github.com/RITHISHlearn/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145446645/30be0f92-52c9-4f45-8dfe-8a5deabe7e6f)



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
