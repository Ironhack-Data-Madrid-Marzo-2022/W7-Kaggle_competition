# W7-Kaggle_competition

![portada](https://github.com/Ironhack-Data-Madrid-Marzo-2022/W7-Kaggle_competition/blob/main/img/Airbnb-inventory-travel-vaccinations2.jpg)

## Description

- Find the best machine learning model and params for the given dataset. 

## Instructions

Find the Kaggle competition [here](https://www.kaggle.com/t/0375f29ef60545b9bd2182109d1ea333).

### Data
#### train.csv
1. **Processing/cleaning** the dataset: this should be later modularized in functions.
2. **Train** a model (fit & predict) with the data in `train.csv`. This file does contain a **y**.
    - Do *train, test, split* on `train.csv` if necessary.
    - Choose the best model regarding the metrics. In this case, the lowest RMSE (error).

    2.1 **Export** the model: we don't want to invest time/RAM resources on training the model again in the future.

#### test.csv
3. Apply the same **cleaning** to `test.csv`. This files does NOT contain a **y**.
4. We'll apply the already **trained model** from step 2 to the `text.csv` file. With this we'lñl generate a new column with the predicted values.  

#### my_submission.csv
5. Generate a `submission.csv` file with only two columns: the **ID** of the diamond & the predicted **price** (y).


## Deliverables

- **Jupyter notebooks** where you show the process you followed to get to your submissions.

- A **slide** (.ppt, ipynb, etc) with a summary of the metrics you obtained and the rationale behind it. 
    - Why do those params work better than others?

## Deadline

+ Monday 9th May 2022 23:59

+ Project presentations will be held on Thursday 10th May 2022.

## Tips
- Take advantage of the daily submissions. Try at least one today!


## Data description

| Field 	| Type 	| Description 	|
|---	|---	|---	|
| id 	| integer 	| Airbnb's unique identifier for the listing 	|
| listing_url 	| text 	|  	|
| scrape_id 	| bigint 	| Inside Airbnb "Scrape" this was part of 	|
| last_scraped 	| datetime 	| UTC. The date and time this listing was "scraped". 	|
| name 	| text 	| Name of the listing 	|
| description 	| text 	| Detailed description of the listing 	|
| neighborhood_overview 	| text 	| Host's description of the neighbourhood 	|
| picture_url 	| text 	| URL to the Airbnb hosted regular sized image for the listing 	|
| host_id 	| integer 	| Airbnb's unique identifier for the host/user 	|
| host_url 	| text 	| The Airbnb page for the host 	|
| host_name 	| text 	| Name of the host. Usually just the first name(s). 	|
| host_since 	| date 	| The date the host/user was created. For hosts that are Airbnb guests this could be the date they registered as a guest. 	|
| host_location 	| text 	| The host's self reported location 	|
| host_about 	| text 	| Description about the host 	|
| host_response_time 	|  	|  	|
| host_response_rate 	|  	|  	|
| host_acceptance_rate 	|  	| That rate at which a host accepts booking requests. 	|
| host_is_superhost 	| boolean [t=true; f=false] 	|  	|
| host_thumbnail_url 	| text 	|  	|
| host_picture_url 	| text 	|  	|
| host_neighbourhood 	| text 	|  	|
| host_listings_count 	| text 	| The number of listings the host has (per Airbnb calculations) 	|
| host_total_listings_count 	| text 	| The number of listings the host has (per Airbnb calculations) 	|
| host_verifications 	|  	|  	|
| host_has_profile_pic 	| boolean [t=true; f=false] 	|  	|
| host_identity_verified 	| boolean [t=true; f=false] 	|  	|
| neighbourhood 	| text 	|  	|
| neighbourhood_cleansed 	| text 	| The neighbourhood as geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles. 	|
| neighbourhood_group_cleansed 	| text 	| The neighbourhood group as geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles. 	|
| latitude 	| numeric 	| Uses the World Geodetic System (WGS84) projection for latitude and longitude. 	|
| longitude 	| numeric 	| Uses the World Geodetic System (WGS84) projection for latitude and longitude. 	|
| property_type 	| text 	| Self selected property type. Hotels and Bed and Breakfasts are described as such by their hosts in this field 	|
| room_type 	| text 	| [Entire home/apt\|Private room\|Shared room\|Hotel]  All homes are grouped into the following three room types:  Entire place Private room Shared room Entire place Entire places are best if you're seeking a home away from home. With an entire place, you'll have the whole space to yourself. This usually includes a bedroom, a bathroom, a kitchen, and a separate, dedicated entrance. Hosts should note in the description if they'll be on the property or not (ex: "Host occupies first floor of the home"), and provide further details on the listing.  Private rooms Private rooms are great for when you prefer a little privacy, and still value a local connection. When you book a private room, you'll have your own private room for sleeping and may share some spaces with others. You might need to walk through indoor spaces that another host or guest may occupy to get to your room.  Shared rooms Shared rooms are for when you don't mind sharing a space with others. When you book a shared room, you'll be sleeping in a space that is shared with others and share the entire space with other people. Shared rooms are popular among flexible travelers looking for new friends and budget-friendly stays. 	|
| accommodates 	| integer 	| The maximum capacity of the listing 	|
| bathrooms 	| numeric 	| The number of bathrooms in the listing 	|
| bathrooms_text 	| string 	| The number of bathrooms in the listing.  On the Airbnb web-site, the bathrooms field has evolved from a number to a textual description. For older scrapes, bathrooms is used. 	|
| bedrooms 	| integer 	| The number of bedrooms 	|
| beds 	| integer 	| The number of bed(s) 	|
| amenities 	| json 	|  	|
| price 	| currency 	| daily price in local currency 	|
| minimum_nights 	| integer 	| minimum number of night stay for the listing (calendar rules may be different) 	|
| maximum_nights 	| integer 	| maximum number of night stay for the listing (calendar rules may be different) 	|
| minimum_minimum_nights 	| integer 	| the smallest minimum_night value from the calender (looking 365 nights in the future) 	|
| maximum_minimum_nights 	| integer 	| the largest minimum_night value from the calender (looking 365 nights in the future) 	|
| minimum_maximum_nights 	| integer 	| the smallest maximum_night value from the calender (looking 365 nights in the future) 	|
| maximum_maximum_nights 	| integer 	| the largest maximum_night value from the calender (looking 365 nights in the future) 	|
| minimum_nights_avg_ntm 	| numeric 	| the average minimum_night value from the calender (looking 365 nights in the future) 	|
| maximum_nights_avg_ntm 	| numeric 	| the average maximum_night value from the calender (looking 365 nights in the future) 	|
| calendar_updated 	| date 	|  	|
| has_availability 	| boolean 	| [t=true; f=false] 	|
| availability_30 	| integer 	| avaliability_x. The availability of the listing x days in the future as determined by the calendar. Note a listing may not be available because it has been booked by a guest or blocked by the host. 	|
| availability_60 	| integer 	| avaliability_x. The availability of the listing x days in the future as determined by the calendar. Note a listing may not be available because it has been booked by a guest or blocked by the host. 	|
| availability_90 	| integer 	| avaliability_x. The availability of the listing x days in the future as determined by the calendar. Note a listing may not be available because it has been booked by a guest or blocked by the host. 	|
| availability_365 	| integer 	| avaliability_x. The availability of the listing x days in the future as determined by the calendar. Note a listing may not be available because it has been booked by a guest or blocked by the host. 	|
| calendar_last_scraped 	| date 	|  	|
| number_of_reviews 	| integer 	| The number of reviews the listing has 	|
| number_of_reviews_ltm 	| integer 	| The number of reviews the listing has (in the last 12 months) 	|
| number_of_reviews_l30d 	| integer 	| The number of reviews the listing has (in the last 30 days) 	|
| first_review 	| date 	| The date of the first/oldest review 	|
| last_review 	| date 	| The date of the last/newest review 	|
| review_scores_rating 	|  	|  	|
| review_scores_accuracy 	|  	|  	|
| review_scores_cleanliness 	|  	|  	|
| review_scores_checkin 	|  	|  	|
| review_scores_communication 	|  	|  	|
| review_scores_location 	|  	|  	|
| review_scores_value 	|  	|  	|
| license 	| text 	| The licence/permit/registration number 	|
| instant_bookable 	| boolean 	| [t=true; f=false]. Whether the guest can automatically book the listing without the host requiring to accept their booking request. An indicator of a commercial listing. 	|
| calculated_host_listings_count 	| integer 	| The number of listings the host has in the current scrape, in the city/region geography. 	|
| calculated_host_listings_count_entire_homes 	| integer 	| The number of Entire home/apt listings the host has in the current scrape, in the city/region geography 	|
| calculated_host_listings_count_private_rooms 	| integer 	| The number of Private room listings the host has in the current scrape, in the city/region geography 	|
| calculated_host_listings_count_shared_rooms 	| integer 	| The number of Shared room listings the host has in the current scrape, in the city/region geography 	|
| reviews_per_month 	| numeric 	| The number of reviews the listing has over the lifetime of the listing 	|