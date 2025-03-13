# Market Segmentation in Insurance

### Objective  :

This case requires to develop a customer segmentation to give recommendations like saving plans, loans, wealth management, etc. on target customer groups.

### Data Description : 

The sample Dataset summarizes the usage behavior of about 9000 active credit card holders during the last 6 months. The file is at a customer level with 18 behavioral variables.

### Exploratory Data Analysis

#### Dimensionality Reduction

###### How does PCA work? 

1.  Looks at an $n$ -dimensional dataset and breaks it down into "general trends" or **components**

```
- When we say "$n$-dimensional", we mean the data has $n$ features.
```

2.  The components are then **sorted by how much of the explained variance they account for** (*eigenvalues* provide this information)

```
- This means if a component is highly-uncorrelated with all others, it's a "strong" component and provides useful information that is very hard to infer from all other components.
```

3.  Then, given some parameter (usually chosen by the data engineer), the new dimension of the data is decided. Let this be $k$.

```
- Note $k$ is always $k \leq n$ because we're only trying to reduce the dimension of our data.
```

4.  Finally, the original $n$ dimensional dataset is projected onto the $k$-dimensional plane chosen by our **top-$k$ components that take care of the most explained variance**.

```
- These top- $k$ components are now used 
```

Because principle components span an (at most) $k$-dimensional surface, we have successfully reduced our data to at least $k \leq n$ dimensions!




### Predictive models
 
In this dataset i've used five clustering algorithm to perform segmentation.These algorithms are given below.
 - KMeans     
 - DBSCAN
 - Meanshift
 - Hierarchical (Agglomerative)

### Final Model  :

We have created a Streamlit Application based on this clustering technique, where we are taking the customer details & identifying which cluster the custoemr belongs to.

### Key Clusters

Cluster 1: **"Low-Volume Pragmatists"**
* Characterized by low financial activity and low credit utilization.
* Tend to maintain low balances and engage in minimal transactions, focusing on stability rather than volume.

Cluster 2: **"High-Volume Power Users"**
* Exhibit high transaction volumes and significant variability in credit limits.
* These are likely the heavy users of financial services, actively engaging with their accounts.

Cluster 3: **"Diverse Low-Volume Users"**
* Similar to Cluster 1 but with greater variability in their financial behavior.
* May indicate a mix of sporadic or inconsistent usage patterns.

Cluster 4: **"Frequent Spenders"**
* Resemble Cluster 2 but with a distinct focus on frequent purchases, particularly installment-based transactions.
* High variability in payment behaviors suggests a mix of disciplined and opportunistic spending habits.
