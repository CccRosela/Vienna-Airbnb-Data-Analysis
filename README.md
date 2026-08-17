# Vienna Airbnb Data Analysis
## Project Overview
The aim of this project is to analyse and study which characteristics are most important to Airbnb listing prices in Vienna and to use different statistical models to predict the price of a listing.

The guiding research question:
    <p style='margin-left: 30px;'>"Through exploratory analysis, how can Airbnb listing prices in Vienna be understood and explained using the variables below, and how effectively can they be predicted, by using and comparing the performance of Lasso Regression and Random Forest on the test data?" </p>

The analysis consists of three main stages:
1. *Data Preparation* – cleaning and preparing the raw Airbnb dataset for analysis. This includes handling missing values, converting variables into suitable formats (numerical, categorical, boolean), removing or capping extreme outliers where necessary, and selecting relevant variables that will be used in the EDA and regression models.
2. *Exploratory Data Analysis (EDA)* – investigating the distribution of prices and other variables, examining relationships between price and listing characteristics (room type, property type, superhost status, capacity, amenities), and analysing how prices and listing density vary across Vienna's neighbourhoods. 
######## To be done: This stage also includes correlation and multicollinearity checks (how the predictor variables relate to one another before modelling) as well as interactive geographic visualisations to capture pricing patterns across the city.
3. *Predictive Modelling* – To do:

## Project Structure
* `data/` – contains the Airbnb dataset
* `Graphs/` – contains the graphs generated during the EDA.
* `notebook/` – contains the Jupyter notebook with the complete analysis (main file + interactive_map)
* `requirements.txt` – lists the Python packages required to run the analysis. Run this command in your terminal:
    `python -m pip install -r requirements.txt`
* `README.md` – overview and documentation of the project.

## Dataset
Analyzing Vienna's Airbnb dataset (data from https://insideairbnb.com/get-the-data/, `listings.csv.gz`).<br>
The file (coverted to csv) is also inside the `data` folder.

### Variables
The dependent variable is the `price` of the listing: the nightly price of the Airbnb listing (using local currency).<br>
The selected predictor variables are: 
* `superhost_status`: indicates whether the host has Airbnb Superhost status. 
* `neighbourhood`: the Vienna neighbourhood in which the listing is located. 
* `property_type`: the type of property, such as an apartment, house or hotel. 
* `room_type`: indicates whether the listing is an entire home, private room, shared room or hotel room. 
* `accommodates`: the maximum number of guests that can stay in the listing. 
* `description_length`: length of the (detailed) description of the listing.
* `amenities`: features and conveniences each listing offers to guests.
* `bathrooms`: the number of bathrooms available in the listing. 
* `bedrooms`: the number of bedrooms in the listing. 
* `min_nights`: the minimum number of nights required for a booking.
* `availability_365`: the number of days during the following year on which the listing is available.
* `num_reviews`: the total number of reviews received by the listing.
* `rating`: the overall rating received by the listing.