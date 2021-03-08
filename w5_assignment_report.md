# Applied Data Science Capstone Report
  ___Open a Coffee Shop in Seattle, WA___

![Seattle](/images/seattle.jpg)

## Introduction
Someone is looking to open a coffee shop, as with any business decision, it requires serious consideration. 
Opening a new coffee shop is a lot more complicated than it seems. However, considering the location of the shop, 
we can simply determine whether the shop will be a success or a failure since the location is the most important factor in this business.

### Problem
The project aims to find an optimal neighborhood for opening a coffee shop in Seattle, WA.

### Target Audience
This project is particularly useful to investors looking to open or invest a new coffee shop in Seattle, WA.

## Data
To solve this problem, the Foursquare API will be used. To explore neighborhoods in Seattle, 
I'll use the explore function to get the most common venue categories in each neighborhood.

The data will be used to compare the density of venues and coffee shops. Finally, 
we will find the best location with the smallest number of competitors.

### Data Resources
- We scrap the list of neighborhoods in Seattle from the [Wikipedia page](https://en.wikipedia.org/wiki/Category:Neighborhoods_in_Seattle).
- We get the geographical coordinates of the neighborhoods using [Geocoder](https://geocoding.geo.census.gov/).
- We explore the neignborhoods using the [Foursquare API](https://developer.foursquare.com/).

## Methodology
1. Get the list of neighborhoods in Seattle from the Wikipedia page.
2. Convent address into geographical coordinates.
3. Populate the data into a Pandas DataFrame.
4. Visulize the neighborhoods in a map using Folium package.
5. Register a Foursquare Develop Account to obtain the venues data.
6. Prepare the data for using in clustering.
7. Filter the "Coffee Shop" as venue category for the neighborhoods.
8. Cluster on the data by using k-means clustering.
9. Answer the question based on the occurrence of coffee shops in different neighborhoods.

## Results

![Seattle Clusters](/images/seattle_clusters.png)

We categorize the neighborhoods into 5 clusters based on the frequency of occurence for "Coffee Shop":

| Cluster | Color | Coffee Shop |
| ------- | ----- | ------------ |
| 0 | <span style="color: red">Red</span> | 0.0005 |
| 1 | <span style="color: purple">Purple</span> | 0.0616 |
| 2 | <span style="color: blue">Blue</span> | 0.1289 |
| 3 | <span style="color: green">Green</span> | 0.0329 |
| 4 | <span style="color: orange">Orange</span> | 0.0854 |

## Discussion & Conclusion
As observed from the result, coffee shops with the highest number in Cluster 2, 
meanwhile Cluster 0 has a very low number to no coffee shop in the neighborhoods. 
It represents a great opportunity to open a new coffee shop in Cluster 0 since there's very little competition from existing shops. 
On the other hand, coffee shops in Cluster 2 are likely suffering from intense competition due to oversupply and high concentration of coffee shops. 
Therefore, this project recommends opening new coffee shops in neighborhoods in Cluster 0 for avoiding competition.

## Future Research
In this project, we only consider one factor — the frequency of occurence of coffee shops,
there are other factors such as income of residents and population that could influence the decision.
Future research can use such data to determine the optimal neighborhood for opening a coffee shop in Seattle, WA.

In addition, we can upgrade Foursquare developer account to obtain more data.
