# Country_data_clustering

The objective of this project was the categorisation of the countries using socio-economic and health factors that indicate the overall development of the country.
The dataset was taken from here https://www.kaggle.com/datasets/rohan0301/unsupervised-learning-on-country-data.

Data from 167 countries were given in `csv` format  [Country_data_clustering
](https://github.com/Iron486/Country_data_clustering/blob/main/Country-data.csv) with the following features:


**country**	Name of the country

**child_mot**	Death of children under 5 years of age per 1000 live births

**exports**	Exports of goods and services per capita. Given as %age of the GDP per capita

**health**	Total health spending per capita. Given as %age of GDP per capita

**imports**	Imports of goods and services per capita. Given as %age of the GDP per capita

**Income**	Net income per person

**Inflation**:	The measurement of the annual growth rate of the Total GDP

**life_expec**:	The average number of years a new born child would live if the current mortality patterns are to remain the same

**total_fer**:	The number of children that would be born to each woman if the current age-fertility rates remain the same.

**gdpp**:	The GDP per capita. Calculated as the Total GDP divided by the total population.

In the notebook called [Country_data_clustering_kmeans.ipynb](https://github.com/Iron486/Country_data_clustering/blob/main/Country_data_clustering_kmeans.ipynb) I applied k-means algorithm, while in this one [Country_data_clustering_DBSCAN_Birch.ipynb](https://github.com/Iron486/Country_data_clustering/blob/main/Country_data_clustering_DBSCAN_Birch.ipynb), I applied DBSCAN and Birch to the dataset.

Firstly, I imported the libraries and read the dataset.
Then, I explored the datasets looking at the main statistical parameters and calculating che correlation matrix for all the numerical features -->![correlation](https://user-images.githubusercontent.com/62444785/163285107-3513a2e4-3c83-43ed-bec7-9324afbc2cd7.png)



I plotted the countries in the World and in Europe with their respective value for each feature. The interactive plots can be found at the following links:


 [Interactive-plots_Europe_child_mort](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_child_mort.html), [Interactive-plots_Europe_exports](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_exports.html), [Interactive-plots_Europe_gdpp](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_gdpp.html), [Interactive-plots_Europe_health](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_health.html), [Interactive-plots_Europe_imports](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_imports.html), [Interactive-plots_Europe_income](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_income.html), [Interactive-plots_Europe_inflation](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_inflation.html), [Interactive-plots_Europe_life_expec](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_life_expec.html), [Interactive-plots_Europe_total_fer](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_total_fer.html), [Interactive-plots_World_child_mort](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_child_mort.html), [Interactive-plots_World_exports](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_exports.html), [Interactive-plots_World_gdpp](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_gdpp.html), [Interactive-plots_World_health](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_health.html), [Interactive-plots_World_imports](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_imports.html), [Interactive-plots_World_income](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_income.html), [Interactive-plots_World_inflation](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_inflation.html), [Interactive-plots_World_life_expec](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_life_expec.html), [Interactive-plots_World_total_fer](https://nbviewer.org/github/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_World_total_fer.html)

Then, I plotted a violin plot to represent the frequency of the values for each feature.



















































https://github.com/Iron486/Country_data_clustering/blob/main/interactive_plots/Interactive-plots_Europe_child_mort.html



![image](https://user-images.githubusercontent.com/62444785/163264343-629e1df8-102f-4493-95dd-b2fff3dee0e6.png)



