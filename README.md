# Team 5 ETL Project- Shop Smarter
[![INSERT YOUR GRAPHIC HERE](https://www.bkacontent.com/wp-content/uploads/2017/10/walmart-cart.jpg)]()


<!-- TABLE OF CONTENTS -->
## Table of Contents

* [Team 5 ETL Project](#team-5-ETL-project)
* [Purpose of the Analysis](#purpose-of-the-analysis)
* [Key Documents](#key-documents)
* [Findings](#findings)
* [Coding Style](#coding-style)
* [API Calls](#api-calls)
* [Coding Documentation](#coding-documentation)
* [Authors](#authors)
* [Acknowledgments](#acknowledgments)


# Team 5 ETL Project- Shop Smarter

Team 5 chose a project that would examine the prices of a set list of items and compare these items across various zip codes across
the United States.  We would like to find if there are differences in prices based on location and look into the impact of product reviews. We have randomly selected five zipcodes in five different states (Alaska, Virginia, California, Florida, and Texas).  A random list of items will be used to compare prices among the desginated stores.  The two primary considerations for shopper when considering a purchase are value and quality.  Using data from the Walmart API, we will create a product information table, a product review table, a product review stat table and a trending products table.  We will merge information from these various tables into one in order to create a data display that is easy to reference for the purpose of deciding which products to purchase.  We will find the top 20 trending products for Walmart and search to see which, if any, of our randomly selected products are one of the top 20 trending products at Walmart.  


## Purpose of the Analysis

We have two primary purposes:

* Our primary purpose is to gather data using the Walmart API to determine if the random items that were selected should be purchased by the consumer.  Shoppers look for a good value (we will information on prices/sales) and quality (we will use information on consumer product reviews).  This data will provide the pertinent information to the shopper when determining if they will make the purchase of the item. 
* The other purpose is to identify which, if any, of our randomly selected products are one of the top 20 trending products at Walmart. 


## Key Documents

The following data sets were used throughout the project.

### Product Identification Table
[![INSERT YOUR GRAPHIC HERE](https://github.com/mabel912/ETL-Project-Shop-Smarter/blob/master/ProductList.png)]()


### Product Review Table
[![INSERT YOUR GRAPHIC HERE](https://github.com/mabel912/ETL-Project-Shop-Smarter/blob/master/ReviewStats.png)]()


### Overall Product Ratings Table
[![INSERT YOUR GRAPHIC HERE](https://github.com/mabel912/ETL-Project-Shop-Smarter/blob/master/OverallProductRating.png)]()


### Megrged Product Information Table
[![INSERT YOUR GRAPHIC HERE](https://github.com/mabel912/ETL-Project-Shop-Smarter/blob/master/MergedProductInfo.png)]()



## Findings

* After doing research on prices across various zipcodes, we found that Walmart offers a 2 day ship to store meaning that no store has to have everything in stock.  The products are available online and can be shipped to any other Walmart stores within 2 days, if needed.  This makes the location of the store irrelevant as far as price comparison.  Therefore, we shifted the focus on pulling data from three sources (product information, product reviews & )into one table. The merged table gives the shopper a comprehensive overview of the selected item.  It indicates the price, the review score and the number of reviews for each item.  As a shopper, this information is vital in terms of making a determination if you would like to buy a product. 


## Coding Style

Jupyter notebooks was used. The list of dependencies are as follows:

```sh
import pandas as pd
import json
import requests
from sqlalchemy import create_engine
from config import wlm_api, myPass
from pandas.io.json import json_normalize
import time
```

## API Calls

* Products API call:
	http://api.walmartlabs.com/v1/items/12417832?apiKey={apiKey}&lsPublisherId={Your LinkShare Publisher Id}&format=json
* Product Review API call:
	http://api.walmartlabs.com/v1/reviews/33093101?apiKey={apiKey}&lsPublisherId={Your LinkShare Publisher Id}&format=json
* Trending API call:
	http://api.walmartlabs.com/v1/trends?apiKey={apiKey}&lsPublisherId=xyz&format=json


## Authors


Lori Brady- Initial Work - [SMU Data ETLTeam 5](https://github.com/loribeth18)

Mabel Gutierrez- Initial Work - [SMU Data ETLTeam 5](https://github.com/mabel912)

Velindia Lucas - Initial Work - [SMU Data ETLTeam 5](https://github.com/chele0630)

Sisay Teketele - Initial Work - [SMU Data ETLTeam 5](https://github.com/sisayyt)

Ka-Ri Walker - Initial Work - [SMU Data ETLTeam 5](https://github.com/ButtonWalker)
