# Melbourne-Housing-Market-and-Venues-Analysis
With Melbourne housing market data coupled with data science techniques, one can derive useful insights and information about current pricing in different suburbs of Melbourne while considering other factors of his/her choice.


### 1.  Business Problem
People of all kinds from across the globe flock to Melbourne, Australia for various reasons, with some of them aspiring to make this incredible place a home of their own. With varying budgets and needs, people find find it very hard to discover a suitable place and neighborhood to accomodate them and their loved ones. Due to high cost of living, Melbourne housing can be a nightmare for most. Melbourne is currently experiencing a housing bubble (some experts say it may burst soon). A potential client aspiring to buy a suitable property would like to become knowledgeable about the ongoing pricing to make a conscious decision. Furthermore, he/she would like to consider several factors like proximity to schools, medical care, restuarants, other liesure amenities to accomodate his/her familial needs.
With Melbourne housing market data coupled with data science techniques, one can derive useful insights and information about current pricing in different suburbs of Melbourne while considering other factors of his/her choice. This would help a potential client to make an informed decision about owning a property in a suitable location in Melbourne.

**Target audience**
Potential clients who are looking to buy property in Melbourne, but are sceptical due to lacking knowledge and volatile market conditions.

**Stakeholders**
1. Government of Australia
2. Real estate agents
3. Property sellers
4. Property buyers


### 2. Data
Following are the sources of data/datasets used for this data analysis project:

**Mebourne Housing Dataset**
This data was scraped from publicly available results posted every week from Domain.com.au. The dataset has been cleaned, and now it available for us folks (data analysts) to do some data analysis magic.
**Author:** Tony Pino
**License:** [Attribution-NonCommercial-ShareAlike 4.0 (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
**Description:**
Suburb: Suburb, Address: Address, Rooms: Number of rooms, Price: Price in Australian dollars, Method: S - property sold; SP - property sold prior; PI - property passed in; PN - sold prior not disclosed; SN - sold not disclosed; NB - no bid; VB - vendor bid; W - withdrawn prior to auction; SA - sold after auction; SS - sold after auction price not disclosed; N/A - price or highest bid not available, Type: br - bedroom(s); h - house,cottage,villa, semi,terrace; u - unit, duplex; t - townhouse; dev site - development site; o res - other residential, SellerG: Real Estate Agent, Date: Date sold, Distance: Distance from CBD in Kilometres, Regionname: General Region (West, North West, North, North east ...etc), Propertycount: Number of properties that exist in the suburb, Bedroom2 : Scraped # of Bedrooms (from different source), Bathroom: Number of Bathrooms, Car: Number of carspots, Landsize: Land Size in Metres, BuildingArea: Building Size in Metres, YearBuilt: Year the house was built, CouncilArea: Governing council for the area, Lattitude: Self explanitory, Longtitude: Self explanitory
**Duration:** January 2016 - October 2018
**Link:** [Kaggle link](https://www.kaggle.com/anthonypino/melbourne-housing-market#Melbourne_housing_FULL.csv)


**Foursquare Locatation Data**
**Description:** To determine the various amenities in the proximity of a desired location, Foursquare location data is used.
**Link:** [Foursquare website](https://foursquare.com/)

### 3. Methodology
This data analysis project is focused on investigating the recent (from January 2016 to October 2018) housing market prices of residential properties in the city of Melbourne and recommend various potential locations where the prospective client can buy a property based on his/her own budget.
The automated script developed as a part of this project does the following:

1. Clean, filter and transform the data obtained from the Melbourne Housing Market dataset which includes the transactions in the period from 2016 to 2018
2. Unique "street names" in the city of Melbourne in each suburb where recent transactions for sale of property were done are filtered from the dataset
3. The average price of property on each of those streets is determined by taking a mean on recent transactions of sale of property on respective streets
4. Based on the budget of the prospective client, the current average prices are compared and all recommendations for the locations are made by plotting them on map of Melbourne. The location popups are labelled with the respective street names and their average property price
5. Location coordinates i.e. latitude and longitudes of the streets are fetched from the Melbourne Housing Market dataset
6. These recommended locations determined based on average pricing are further fed into Foursquare API calls to discover various amenities in proximity to them. All reported venues are then tabulated, analysed thoroughly and presented to the user
7. Important facilities like Hospitals, Grocery stores, Schools and Universities, Pharmacies, etc. are then searched for in vicinity of each of those locations and then based on these outcomes, the locations are further filtered

In order to conduct a similar analysis for any other city in Melbourne, the automated script has been written to accommodate a change in:
1. City/Town
2. Budget of the client

Such changes can be made with minimal effort and would generate the recommended locations to buy a property in the city of Melbourne.

### 4. Results
Upon running the exploratory data analysis for city of Melbourne with a hypothetical client budget of 0.3 Million, the algorithm recommends 26 streets in Melbourne, among which top 15 streets are selected (on basis of total number of nearby amenities) where the prospective client can buy the property as per the current market housing prices.

A list of such locations is presented to the user with location coordinates and most recent average prices. Total number of significant amenties are also presented to the user in a tabulated format to take care of his familial needs.
![image](https://github.com/PatelKeviin/Melbourne-Housing-Market-and-Venues-Analysis/blob/master/img/1.PNG)

These recommended street names are plotted on the map of Melbourne with the best possible locations, based on budget and nearby neighborhood amenities.
![image](https://github.com/PatelKeviin/Melbourne-Housing-Market-and-Venues-Analysis/blob/master/img/2.PNG)

Furthermore, following venues are enlisted for the user to make an informed decision while choosing a location.
![image](https://github.com/PatelKeviin/Melbourne-Housing-Market-and-Venues-Analysis/blob/master/img/3.PNG)

### 5. Discussion
Based on the findings in the results section, the user can take a conscious decision about choosing a street i.e. location based upon his/her specific requirements.
The results section enlists 26 locations where a prospective client can buy a property based on his needs and choices. Such choices would be affected by the venues and facilities which are close to the property which match against his familial needs.

Few possible use-cases are:
1. A prospective client with elders in the family would be inclinded to choose a location where hospitals and grocery stores are located in close proximity
2. A prospective client with kids in the family would be choosing a location where elementary and high schools are nearby. He would also like to choose a place with parks and other venues in the close vicinity
3. A bachelor would be inclined to choose a property which has pubs, bars, entertainment, etc. close to the property

### 6. Conclusion
The decision of a buyer is influenced by the familial needs, personal biases and so on. So, based on the findings summarized in the results and discussion sections, following conclusions can be made:
1. While making recommendations to a prospective client, it is imperative to know his/her requirements besides the budget, which dictates his/her decision of buying the property largely. This would help to catch his/her attention
2. Knowledge about the most recent market prices can be very helpful for the client and can help him take an informed decision

Thank you for your time!