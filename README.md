## The Seattle Airbnb Dataset
#### **Context**
Since 2008, guests and hosts have used Airbnb to travel in a more unique, personalized way. As part of the Airbnb Inside initiative, this dataset describes the listing activity of homestays in Seattle, WA.

### **Content**
This project shows my attempt at cleaning, wrangling, exploring, analysing and modelling the data for seattles Airbnb listings in order to gain insights into trends and answer the questions listed below. The dataset obtained from kaggle open dataset contains the following Airbnb activity:

* **1. Listings.csv:** including full descriptions of listings and average review score:
    > some of the features in the listing data are: 
    > **id , listing_url , scrape_id , last_scraped , name , summary , space , description , experiences_offered , neighborhood_overview ,  notes , transit , thumbnail_url , medium_url , picture_url , xl_picture_url , host_id , host_url , host_name , host_since , host_location , host_about , host_response_time , host_response_rate , host_acceptance_rate , host_is_superhost , host_thumbnail_url , host_picture_url , host_neighbourhood , host_listings_count , host_total_listings_count , host_verifications , host_has_profile_pic , host_identity_verified , street , neighbourhood , neighbourhood_cleansed , neighbourhood_group_cleansed , city , state , zipcode , market , smart_location , country_code , country , latitude , longitude , is_location_exact , property_type , room_type , accommodates , bathrooms , bedrooms , beds , bed_type , amenities , square_feet , price , weekly_price , monthly_price , security_deposit , cleaning_fee , guests_included , extra_people ,minimum_nights , maximum_nights , calendar_updated , has_availability , availability_30 , availability_60 , availability_90 , availability_365 , calendar_last_scraped , number_of_reviews , first_review , last_review , review_scores_rating , review_scores_accuracy , review_scores_cleanliness , review_scores_checkin , review_scores_communication , review_scores_location , review_scores_value , requires_license , license , jurisdiction_names , instant_bookable , cancellation_policy , require_guest_profile_picture , require_guest_phone_verification , calculated_host_listings_count , reviews_per_month**

- **2. Reviews.csv:**  including unique id, date for each reviewer and detailed comments

- **3. Calendar.csv:** including listing id and the price and availability for that day

The dataset is cleaned, wrangled and then explored using matplotlib and finally modelled using Logistic regression and Random forest Regressor from Sklearn to predict price. important features that help in price prediction are obtained using feature_importance_ from random forest model.

### **Questions**
This project carries out cleaning, wrangling, exploring, analysing and modelling to answer questions like: 
- What are the types of properties available in seattle s listings? What are thier prices on average?
- What are the neighbourhood trends? What neighbourhoods have the most expensive and cheapest listings?
- What are the busiest times of the year to visit Seattle? By how much do prices spike?
- Is there a general upward trend of both new Airbnb listings and total Airbnb visitors to Seattle?
- What are the important features that predict price.

### **Features and Missing Data:**
 Some of the Features in the dataset are in the wrong datatype.
 - Price is type object instead of float
 - Some features that should be Boolean types are also entered as type string
 - In this project features missing a good number of their entries are dropped. The missing entries in the price column is filled using the average price for that particular month period.
 - Count vectorizer is used to extract categorical data from the amenities feature

 - Other categorical features remaining where converted to dummy variables.

### **Acknowledgement**
This dataset is obtained from kaggle open dataset part of Airbnb Inside, and the original source can be found [here](http://insideairbnb.com/get-the-data.html).