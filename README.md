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
the United States.  We would like to find if there are differences in prices based on location and look into the impact of product reviews. We have randomly selected five zipcodes in five different states (Alaska, Virginia, California, Florida, and Texas).  A random list of items will be used to compare prices among the desginated stores.  We pulled information to create a product table, a review table and a trending table.  We will find the top 20 trending items for Walmart and search to see which, if any, of our randomly selected products are one of the top 20 trending products at Walmart.  

### Purpose of the Analysis

* The primary purpose is to examine if a relationship exists between product price and location (zipcode) of Walmart stores. 
* The secondary purpose is to identify which, if any, of our randomly selected products are one of the top 20 trending products at Walmart. 


### Key Documents

The following data sets were used throughout the project.

*Product Table
*Review Table
*Trending Table


### Findings

*

### Walmart Location

[![INSERT YOUR GRAPHIC HERE]()]()

### Coding Style

Jupyter notebooks was used. The list of dependencies are as follows:

```sh
import pandas as pd
import json
import requests
from sqlalchemy import create_engine
from config import wlm_api
```

### API Calls

<!-- [City of los Angeles](https://data.lacity.org/resource/8yfh-4gug.json)-->

## Authors


Lori Brady- Initial Work - [SMU Data ETLTeam 5](https://github.com/loribeth18)

Mabel Gutierrez- Initial Work - [SMU Data ETLTeam 5](https://github.com/mabel912)

Velindia Lucas - Initial Work - [SMU Data ETLTeam 5](https://github.com/chele0630)

Sisay Teketele - Initial Work - [SMU Data ETLTeam 5](https://github.com/sisayyt)

Ka-Ri Walker - Initial Work - [SMU Data ETLTeam 5](https://github.com/ButtonWalker)
