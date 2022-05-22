# Country_data_clustering

**The objective of this project was the categorisation of the countries using socio-economic and health factors that indicate the overall development of the country.**

The dataset was taken from here https://www.kaggle.com/datasets/rohan0301/unsupervised-learning-on-country-data.

Data from 167 countries were given in `csv` format  [Country_data_clustering
](https://github.com/Iron486/Country_data_clustering/blob/main/Country-data.csv) with the following features:


**country**	Name of the country;

**child_mot**	Death of children under 5 years of age per 1000 live births;

**exports**	Exports of goods and services per capita. Given as %age of the GDP per capita;

**health**	Total health spending per capita. Given as %age of GDP per capita;

**imports**	Imports of goods and services per capita. Given as %age of the GDP per capita;

**Income**	Net income per person;

**Inflation**:	The measurement of the annual growth rate of the Total GDP;

**life_expec**:	The average number of years a new born child would live if the current mortality pattern remains the same;

**total_fer**:	The number of children that would be born to each woman if the current age-fertility rate remains the same;

**gdpp**:	The GDP per capita. Calculated as the Total GDP divided by the total population.

In the notebook called [Country_data_clustering_kmeans.ipynb](https://github.com/Iron486/Country_data_clustering/blob/main/Country_data_clustering_kmeans.ipynb), I applied k-means algorithm, while in this one [Country_data_clustering_DBSCAN_Birch.ipynb](https://github.com/Iron486/Country_data_clustering/blob/main/Country_data_clustering_DBSCAN_Birch.ipynb) I applied DBSCAN and Birch to the dataset.

Firstly, I imported the libraries and read the dataset.
Then, I explored the datasets looking at the main statistical parameters and calculating che correlation matrix for all the numerical features.

<p align="center"> <img src="https://user-images.githubusercontent.com/62444785/163285107-3513a2e4-3c83-43ed-bec7-9324afbc2cd7.png" width="870" height="670"/>   </p>()



I plotted the countries in the World and in Europe with their respective value for each feature. The interactive plots can be found at the following links:


 [Interactive-plots_Europe_child_mort](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_child_mort.html), [Interactive-plots_Europe_exports](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_exports.html), [Interactive-plots_Europe_gdpp](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_gdpp.html), [Interactive-plots_Europe_health](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_health.html), [Interactive-plots_Europe_imports](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_imports.html), [Interactive-plots_Europe_income](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_income.html), [Interactive-plots_Europe_inflation](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_inflation.html), [Interactive-plots_Europe_life_expec](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_life_expec.html), [Interactive-plots_Europe_total_fer](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_total_fer.html), [Interactive-plots_World_child_mort](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_child_mort.html), [Interactive-plots_World_exports](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_exports.html), [Interactive-plots_World_gdpp](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_gdpp.html), [Interactive-plots_World_health](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_health.html), [Interactive-plots_World_imports](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_imports.html), [Interactive-plots_World_income](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_income.html), [Interactive-plots_World_inflation](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_inflation.html), [Interactive-plots_World_life_expec](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_life_expec.html), [Interactive-plots_World_total_fer](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_total_fer.html)

Then, I plotted a violin plot to represent the frequency of the values for each feature. I scaled the data and I applied the K-means algorithm, plotting the inertia and the silhouette score per cluster:

<p align="center"> <img src="https://user-images.githubusercontent.com/62444785/163286827-c440c389-a1d5-4045-84db-d9bdbbbd4db0.png" width="850" height="400"/>   </p>

According to the plot of inertia, the optimal number of cluster is 4 since the curve has an "elbow" at 4 cluster. Even the silhouette score indicates a high value at 4 clusters.
In this case, instead, I decided  to choose 3 clusters since the algorithm isolates better the countries that need more help.

Then, I plotted an interactive plot that is able to visualize better the clusters (represented with 3 different colors). 
Below, it's possible to check the plot and also to check the interactive plot (click on the link below the figure). 

Each feature can be restrained to some particular range values, clicking on the bar associated with each feature and unclicking when the user is satisfied with the range of values. 

## **<p align="center"> Features vs Labels Kmeans: Interactive Plot </p>**

![features_and_labels_plot_interactive](https://user-images.githubusercontent.com/62444785/163291008-5610d12b-3e8b-4b45-83a6-392c34ad5acd.png)

### Click here to check the interactive plot --> [Features vs Labels Kmeans: Interactive Plot](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/features_and_labels_plot_interactive.html)

Below, instead, I plotted the different clusters on the globe. Each cluster can be associated with countries that have a similar development conditions.

## **<p align="center"> Kmeans: Needed Help Per Country </p>**

![NeededHelpPerCountry(World)kmeans](https://user-images.githubusercontent.com/62444785/163290746-c7bd9e14-fce6-4e24-9784-bf127e8b8c2f.png)

### Click here to check the interactive plot --> [Kmeans: Needed Help Per Country](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/NeededHelpPerCountry%28World%29kmeans.html)

At the end, a correlation plot was plotted enhancing the 3 different clusters and showing how they were separated in the feature hyperspace.
## **<p align="center"> Kmeans clustering scatterplots </p>**


![Kmeans clustering scatterplots](https://user-images.githubusercontent.com/62444785/163288199-3b8af812-26b8-4930-850a-35d622eef6d1.png)

### Click here to download the plot --> [Kmeans: scatterplots](https://github.com/Iron486/Country_data_clustering/blob/main/Kmeans%20clustering%20scatterplots.png)


DBDSCAN and Birch were also applied (check the following notebook [Country_data_clustering_DBSCAN_Birch.ipynb](https://github.com/Iron486/Country_data_clustering/blob/main/Country_data_clustering_DBSCAN_Birch.ipynb)), showing the following results:

## **<p align="center"> DBSCAN: Needed Help Per Country </p>**

![Needed Help Per Country (World)](https://user-images.githubusercontent.com/62444785/163290834-27fd510c-155c-49e6-9578-5977f3cecbcd.png)

## **<p align="center"> Birch: clustering scatterplots </p>**

![NeededHelpPerCountry(World)_birch](https://user-images.githubusercontent.com/62444785/163291120-5de5b926-5fe9-4413-a9a1-aa41d1faf650.png)

<ins>Note</ins>: The interactive plots and the other graphs used for Kmeans with the other algorithms, can be found in the Notebook.

``  
``  

It can be observed that **DBSCAN found a consistent number of outliers**, even though different hyperparameters were tested. 

Using **Birch** the result is **similar to Kmeans**, with the exception that some countries are not considered in the same class as in Kmeans.























