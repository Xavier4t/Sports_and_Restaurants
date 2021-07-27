

![enter image description here](https://github.com/Xavier4t/Sports-league_Restaurants/blob/main/Images/sports&restaurants2.png?raw=True)
 ## Sports & Restaurants
 
### Restaurants around the Stadiums and Arenas of professional major sports leagues.

#### About the Data
For each franchise in the MLB, MLS, NBA, NFL and NHL, a **JSON** file (per team, per league) containing all**¹** the restaurants information in a 3000 meters (1.86 miles) radius around the team stadium.  
Two datasets are generated:
1.  The **General**  dataset, no category has been specified, thus resulting in all kind of restaurants in the 3000 meters radius around the stadiums.
2.  The  **Category** dataset , results for the following categories only: sports bars, pubs, wine bars and cocktail bars.


The data has been obtained using the Yelp Fusion API, requesting the information of restaurants in a 3000 meters (1.86 miles) radius centered in the teams stadiums/arenas.   

Yelp Fusion API only returns a max of 50 of business results per request, but it can be offset to return up to a maximum of 1000 businesses.  
Then, the offset results were cleaned and merged with some of the team information in one single JSON file per team, per sport league.

### The Data
A typical **JSON** file contains the following information:

	league: the sport league  
	team: the name of the team  
	stadium: the name of the stadium/arena  
	stadium latitude: latitude of the stadium/arena  
	stadium longitude: longitude of the stadium/arena  
	radius: radius of the circle around the stadium/arena  
	city: the city where the team is based  
	state: US State where the city is.  
	businesses: all the restaurants and their information found in the radius centered in the stadium latitude and longitude.

	-   For each business:  
	    id: business/restaurant Yelp id  
	    alias: business/restaurant alias  
	    name: business/restaurant name  
	    image url: image of the business/restaurant  
	    is closed: boolean indicating if the business/restaurant is closed (True) or not closed (False)  
	    url: business/restaurant webpage  
	    review_count: number of Yelp reviews  
	    categories: categories that the business/restaurant identifies itself  
	    rating: business/restaurant Yelp rating  
	    coordinates: business/restaurant location  
	    transactions: if business/restaurant delivers, pickup food, etc.  
	    price: Yelp price identification system using "$"  
	    location: business/restaurant address  
	    phone: business/restaurant phone number  
	    distance: business/restaurant distance from the Stadium/Arena coordinates.

	absolute total: the total number of businesses (restaurants, food places, etc.) found inside the search radius  
	total²: the total number of businesses in the JSON file, up to 1000.





The dataset has been published in Kaggle here: [Sports and Restaurants](https://www.kaggle.com/xavier4t/sports-and-restaurants).


**¹** The data is limited to Yelp results (so restaurants not registered on Yelp would not appear in the dataset).

**²** Yelp Fusion API only returns up to a maximum of 1000 businesses, although it returns the value of the total amount of restaurants found.  The total amount returned has been renamed to "absolute total" whilst the key "total" indicates the number of businesses included in the JSON file (up to  1000)
