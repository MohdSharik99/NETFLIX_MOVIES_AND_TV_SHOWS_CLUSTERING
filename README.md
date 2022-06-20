# NETFLIX_MOVIES_AND_TV_SHOWS_CLUSTERING
Unsupervised ML project


This dataset consists of tv shows and movies available on Netflix as of 2019. The dataset is collected from Flixable which is a third-party Netflix search engine.

In 2018, they released an interesting report which shows that the number of TV shows on Netflix has nearly tripled since 2010. The streaming service’s number of movies has decreased by more than 2,000 titles since 2010, while its number of TV shows has nearly tripled. It will be interesting to explore what all other insights can be obtained from the same dataset.

Integrating this dataset with other external datasets such as IMDB ratings, rotten tomatoes can also provide many interesting findings.

:::## In this project, you are required to do

Exploratory Data Analysis

Understanding what type content is available in different countries

Is Netflix has increasingly focusing on TV rather than movies in recent years.

Clustering similar content by matching text-based features.



Approach taken:
This project is divided into multiple section where each section will have it's own importance towards our problem statements. the approach that we will be following in this project is given as-

Section 1: In this section we will simply loading our dataset into google colab and will explore the basic information about data.

Section 2: In section 2 we will be dealing with missing values of this dataset and will impute the values into missing places.

Section 3: In this section We fill focus on Exploratory data analysis of the dataset using various methods and visualization plot and will be extracting the information from this dataset as much as we can.

Section 4: In this section we will be dealing with outliers in out dataset and will see how to define our outlier criteria and deal with outliers.

Section 5: In this Section we will be applying NLP in order to get most similer contents like most similer movies.

Section 6: In this section we will be perform various clustering methods to find out best no. of clusters and for validation we will be using Silhouette score and elbow curve where ever it is applicable.

Section 7: In this section we will be giving a quick summary of entire notebook.





## Libraries used: 
UMAP
Prince
Numpy
Pandas
Seaborn
Matplotlib
Sklearn
Kmodes



Clustering :

we will be performing Clustering over the cleaned dataset i.e updated_dataset as we already have gone thorugh our data and seen that the data contains a lot of categorigal features and hence we will be using Kmodes clustering method as this method is the most suitable available method for clustering for categorical data. Also we know that most of the algorithms can not be applied on the dataset that has categorical features as they do not yield good resluts and and will will be applying require some transformations from categorical features to numerical features. Although this task can be performed manually with help of encoding and PCA( principal component analysis) but we also have well defined algorithm to perform the same transformation named `UMAP', MCA [ ( Uniform Manifold Approximation and Projection), (multiple correspondense analysis ) ] which comes under Prince library.

The steps that are involved in this section will be as follows: 1 - Apply K-modes clustering on categorical data and find out the best value of K using albow method

2 - Apply MCA and get the intuition wheather this is a write choice plotting it in two dimensions.

3 - implimenting UMAP and converting it to a dataframe.

4 - implimenting Clustering models on transformed data say X and find out best no. of clusters. in this process we will be using a couple of clustering model- a) DBSCAN

b) Hierarchical

c) Spectral clustering

d) K means and validation using Silhouette score

Uniform Manifold Approximation and Projection for Dimension Reduction (UMAP)
UMAP is a dimensionality reduction technique predicated upon manifold learning & ideas from topological data analysis. It provides a general framework for applying dimensionality reduction and is an incredibly powerful tool in any data scientist’s arsenal. In order to apply UMAP to mixed data we must create two separate manifolds one for each data type, as UMAP still needs to compute distances between points. These two manifolds are then combined either by computing the Union which preserves the categorical embedding more, or by calculating the intersection which will cause the embedding to more closely resemble the numerical manifold.





This project was divided into 7 sections where each section.

Section 1: In this section we have simply loaded our dataset into google colab and explored the basic information about data.

Section 2: In section 2 we have dealt with missing values and imputed the missing values depending on the certain assumption so that we do not miss out important information of the data.

Section 3: In this section We have foused on the EDA part where we have performed a detailed EDA on all the possible columns we have drawn a lot of insights even though the data in some columns was not in appropriate format such as cast, listed_in etc.

Section 4: in this section we have dealt with outliers where we have used general way remove categorical outliers and then we have used isolation forest to remove numeric outliers and visualise out data before and after the process.

Section 5: In this section we have performed NLP to find out which are the top 10 similar movies and TV shows

Section 6: In this section we have perform various clustering methods to find out best no. of clusters and for validation we have used Silhouette score and elbow curve where ever it is applicable.

finally we have reached to the conclusion that the optimal no. of clusters that can be formed using the given data is 3
