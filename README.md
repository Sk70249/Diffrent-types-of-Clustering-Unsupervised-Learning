# Diffrent types of Clustering: Unsupervised-Learning &nbsp;&nbsp;[![license](https://img.shields.io/github/license/ajaymache/travis-ci-with-github.svg)](https://opensource.org/licenses/MIT)

## [1. KMeans Clustering](https://github.com/Sk70249/Diffrent-types-of-Clustering-Unsupervised-Learning/tree/master/KMeans%20Clustering)

## Introduction

There are many models for **clustering** out there. In this notebook, we will be presenting the model that is considered one of the simplest models amongst them. Despite its simplicity, the **K-means** is vastly used for clustering in many data science applications, especially useful if you need to quickly discover insights from **unlabeled data**. In this notebook, you will learn how to use k-Means for customer segmentation.

Some real-world applications of k-means:
- Customer segmentation
- Understand what the visitors of a website are trying to accomplish
- Pattern recognition
- Machine learning
- Data compression


In this notebook we practice k-means clustering with 2 examples:
- k-means on a random generated dataset
- Using k-means for customer segmentation

[<h1 id="customer_segmentation_K_means">Customer Segmentation with K-Means</h1>](https://github.com/Sk70249/Diffrent-types-of-Clustering-Unsupervised-Learning/blob/master/KMeans%20Clustering/K-Means-Customer-Segmentation.ipynb)
Imagine that you have a customer dataset, and you need to apply customer segmentation on this historical data.
Customer segmentation is the practice of partitioning a customer base into groups of individuals that have similar characteristics. It is a significant strategy as a business can target these specific groups of customers and effectively allocate marketing resources. For example, one group might contain customers who are high-profit and low-risk, that is, more likely to purchase products, or subscribe for a service. A business task is to retaining those customers. Another group might include customers from non-profit organizations. And so on.

### Now, lets look at the distribution of customers based on their - Age and Income:

![download (9)](https://user-images.githubusercontent.com/48255425/84578325-d6ba4580-ade1-11ea-8d6e-cf440de20c32.png)

### Now, lets look at the distribution of customers based on their - Education, Age and Income:

![download (10)](https://user-images.githubusercontent.com/48255425/84578334-e76abb80-ade1-11ea-8510-1c2846cc78db.png)

## [2. Hirarchical Clutering](https://github.com/Sk70249/Diffrent-types-of-Clustering-Unsupervised-Learning/tree/master/Hirarchical%20Clustering)

[<h1 id="hierarchical_agglomerative">Hierarchical Clustering - Agglomerative</h1>](https://github.com/Sk70249/Diffrent-types-of-Clustering-Unsupervised-Learning/blob/master/Hirarchical%20Clustering/Hierarchical-Clustering-Vehicle-Dataset.ipynb)


We will be looking at a clustering technique, which is <b>Agglomerative Hierarchical Clustering</b>. Remember that agglomerative is the bottom up approach. <br> <br>
In this lab, we will be looking at Agglomerative clustering, which is more popular than Divisive clustering. <br> <br>
We will also be using Complete Linkage as the Linkage Criteria. <br>
<b> <i> NOTE: You can also try using Average Linkage wherever Complete Linkage would be used to see the difference! </i> </b>

<h3 id="dendrogram">Dendrogram Associated for the Agglomerative Hierarchical Clustering</h3>
Remember that a <b>distance matrix</b> contains the <b> distance from each point to every other point of a dataset </b>. <br>
Use the function <b> distance_matrix, </b> which requires <b>two inputs</b>. Use the Feature Matrix, <b> X2 </b> as both inputs and save the distance matrix to a variable called <b> dist_matrix </b> <br> <br>
Remember that the distance values are symmetric, with a diagonal of 0's. This is one way of making sure your matrix is correct. <br> (print out dist_matrix to make sure it's correct)

A Hierarchical clustering is typically visualized as a dendrogram as shown in the following cell. Each merge is represented by a horizontal line. The y-coordinate of the horizontal line is the similarity of the two clusters that were merged, where cities are viewed as singleton clusters. 
By moving up from the bottom layer to the top node, a dendrogram allows us to reconstruct the history of merges that resulted in the depicted clustering. 

Next, we will save the dendrogram to a variable called <b>dendro</b>. In doing this, the dendrogram will also be displayed.
Using the <b> dendrogram </b> class from hierarchy, pass in the parameter:
<ul> <li> Z </li> </ul>

![download (7)](https://user-images.githubusercontent.com/48255425/84578253-509dff00-ade1-11ea-84f6-4a0baf9eec87.png)

<h1 id="clustering_vehicle_dataset">Clustering on Vehicle dataset</h1>
Imagine that an automobile manufacturer has developed prototypes for a new vehicle. Before introducing the new model into its range, the manufacturer wants to determine which existing vehicles on the market are most like the prototypes--that is, how vehicles can be grouped, which group is the most similar with the model, and therefore which models they will be competing against.

Our objective here, is to use clustering methods, to find the most distinctive clusters of vehicles. It will summarize the existing vehicles and help manufacturers to make decision about the supply of new models.

## Final Output:

![download (8)](https://user-images.githubusercontent.com/48255425/84578263-6d3a3700-ade1-11ea-900d-dc6b04e5daf8.png)


## [3. Density Based Clustering (DBSCAN)](https://github.com/Sk70249/Diffrent-types-of-Clustering-Unsupervised-Learning/tree/master/Density%20Based%20Clustering%20(DBSCAN))
Most of the traditional clustering techniques, such as k-means, hierarchical and fuzzy clustering, can be used to group data without supervision. 

However, when applied to tasks with arbitrary shape clusters, or clusters within cluster, the traditional techniques might be unable to achieve good results. That is, elements in the same cluster might not share enough similarity or the performance may be poor.
Additionally, Density-based Clustering locates regions of high density that are separated from one another by regions of low density. Density, in this context, is defined as the number of points within a specified radius.




[<h1 align=center> Weather Station Clustering using DBSCAN & scikit-learn </h1>](https://github.com/Sk70249/Diffrent-types-of-Clustering-Unsupervised-Learning/blob/master/Density%20Based%20Clustering%20(DBSCAN)/Clustering-DBSCN-on-weather.ipynb)
<hr>

DBSCAN is specially very good for tasks like class identification on a spatial context. The wonderful attribute of DBSCAN algorithm is that it can find out any arbitrary shape cluster without getting affected by noise. For example, this following example cluster the location of weather stations in Canada.
<Click 1>
DBSCAN can be used here, for instance, to find the group of stations which show the same weather condition. As you can see, it not only finds different arbitrary shaped clusters, can find the denser part of data-centered samples by ignoring less-dense areas or noises.

let's start playing with the data. We will be working according to the following workflow: </font>
1. Loading data
- Overview data
- Data cleaning
- Data selection
- Clusteing

### About the dataset

Environment Canada    
Monthly Values for July - 2015	
</head>
<body>

<table>
  <tr>
    <th>Name in the table</th>
    <th>Meaning</th>
  </tr>
  <tr>
    <td><font color = "green"><strong>Stn_Name</font></td>
    <td><font color = "green"><strong>Station Name</font</td>
  </tr>
  <tr>
    <td><font color = "green"><strong>Lat</font></td>
    <td><font color = "green"><strong>Latitude (North+, degrees)</font></td>
  </tr>
  <tr>
    <td><font color = "green"><strong>Long</font></td>
    <td><font color = "green"><strong>Longitude (West - , degrees)</font></td>
  </tr>
  <tr>
    <td>Prov</td>
    <td>Province</td>
  </tr>
  <tr>
    <td>Tm</td>
    <td>Mean Temperature (°C)</td>
  </tr>
  <tr>
    <td>DwTm</td>
    <td>Days without Valid Mean Temperature</td>
  </tr>
  <tr>
    <td>D</td>
    <td>Mean Temperature difference from Normal (1981-2010) (°C)</td>
  </tr>
  <tr>
    <td><font color = "black">Tx</font></td>
    <td><font color = "black">Highest Monthly Maximum Temperature (°C)</font></td>
  </tr>
  <tr>
    <td>DwTx</td>
    <td>Days without Valid Maximum Temperature</td>
  </tr>
  <tr>
    <td><font color = "black">Tn</font></td>
    <td><font color = "black">Lowest Monthly Minimum Temperature (°C)</font></td>
  </tr>
  <tr>
    <td>DwTn</td>
    <td>Days without Valid Minimum Temperature</td>
  </tr>
  <tr>
    <td>S</td>
    <td>Snowfall (cm)</td>
  </tr>
  <tr>
    <td>DwS</td>
    <td>Days without Valid Snowfall</td>
  </tr>
  <tr>
    <td>S%N</td>
    <td>Percent of Normal (1981-2010) Snowfall</td>
  </tr>
  <tr>
    <td><font color = "green"><strong>P</font></td>
    <td><font color = "green"><strong>Total Precipitation (mm)</font></td>
  </tr>
  <tr>
    <td>DwP</td>
    <td>Days without Valid Precipitation</td>
  </tr>
  <tr>
    <td>P%N</td>
    <td>Percent of Normal (1981-2010) Precipitation</td>
  </tr>
  <tr>
    <td>S_G</td>
    <td>Snow on the ground at the end of the month (cm)</td>
  </tr>
  <tr>
    <td>Pd</td>
    <td>Number of days with Precipitation 1.0 mm or more</td>
  </tr>
  <tr>
    <td>BS</td>
    <td>Bright Sunshine (hours)</td>
  </tr>
  <tr>
    <td>DwBS</td>
    <td>Days without Valid Bright Sunshine</td>
  </tr>
  <tr>
    <td>BS%</td>
    <td>Percent of Normal (1981-2010) Bright Sunshine</td>
  </tr>
  <tr>
    <td>HDD</td>
    <td>Degree Days below 18 °C</td>
  </tr>
  <tr>
    <td>CDD</td>
    <td>Degree Days above 18 °C</td>
  </tr>
  <tr>
    <td>Stn_No</td>
    <td>Climate station identifier (first 3 digits indicate   drainage basin, last 4 characters are for sorting alphabetically).</td>
  </tr>
  <tr>
    <td>NA</td>
    <td>Not Available</td>
  </tr>


</table>

</body>
</html>

 ### Visualization
Visualization of stations on map using basemap package. The matplotlib basemap toolkit is a library for plotting 2D data on maps in Python. Basemap does not do any plotting on it’s own, but provides the facilities to transform coordinates to a map projections. 

Please notice that the size of each data points represents the average of maximum temperature for each station in a year:

![download (11)](https://user-images.githubusercontent.com/48255425/84578482-4f6dd180-ade3-11ea-893d-52778e88b432.png)

### Clustering of stations based on their location i.e. Lat & Lon

__DBSCAN__ form sklearn library can runs DBSCAN clustering from vector array or distance matrix. In our case, we pass it the Numpy array Clus_dataSet to find core samples of high density and expands clusters from them. 
  Cluster 0, Avg Temp: -5.538747553816051
  Cluster 1, Avg Temp: 1.9526315789473685
  Cluster 2, Avg Temp: -9.195652173913045
  Cluster 3, Avg Temp: -15.300833333333333
  Cluster 4, Avg Temp: -7.769047619047619
![download (12)](https://user-images.githubusercontent.com/48255425/84578516-a5427980-ade3-11ea-851d-7b292d060789.png)


### Visualization of clusters based on location and Temperture:
  Cluster 0, Avg Temp: 6.2211920529801334
  Cluster 1, Avg Temp: 6.790000000000001
  Cluster 2, Avg Temp: -0.49411764705882355
  Cluster 3, Avg Temp: -13.877209302325586
  Cluster 4, Avg Temp: -4.186274509803922
  Cluster 5, Avg Temp: -16.301503759398482
  Cluster 6, Avg Temp: -13.599999999999998
  Cluster 7, Avg Temp: -9.753333333333334
  Cluster 8, Avg Temp: -4.258333333333334

![download (13)](https://user-images.githubusercontent.com/48255425/84578558-04a08980-ade4-11ea-95fb-0579b680c51f.png)



### Thanks for reading for more such content visit my profile [Sk70249](https://github.com/Sk70249)







