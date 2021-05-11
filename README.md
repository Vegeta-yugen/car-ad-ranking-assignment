# Assignment Details
All the questions will be self-explanatory, however, if you have any doubts/queries, you can write to us at **foundersdesk@yugen.ai** about it.
We would prefer receiving your solutions within **5 days (including Saturday and Sunday)**, however, if you need more time, please write to us at **foundersdesk@yugen.ai** and let us know in advance

## Context to Data
The data was scraped over a period of more than a year from Car Classified websites (think OLX or CarBazaar.com etc.). The scrapers were tuned slowly over the course of the year and some of the sources were completely unstructured, so as a result the data is dirty, there are missing values and some values are very obviously wrong (e.g. `phone numbers` scraped as `mileage` etc.). The data is for the years `2015-2017`. 
The complete dataset can be found in the `assignment.zip` zipped file in the repository.
There are 3 files in the dataset:
1. `Historical Dataset` - The dataset contains `~686k` rows related to different advertisements for cars.It contains the following columns:
    - `maker` - normalized all lowercase, manufacturer of the car
    - `model` - normalized all lowercase, model name of the car
    - `mileage` - in KM
    - `Manufacture_year` - The year of when the car was manufactured
    - `engine_displacement` - in ccm
    - `engine_power` - in kW
    - `body_type` - type of the car’s body, only personal cars, no motorcycles or utility vehicles
    - `color_slug` - colour of the car
    - `stk_year` - year of the last emission control
    - `transmission` - automatic or manual
    - `Door_count` - Number of doors in the car
    - `Seat_count` - Number of persons which can fit in the car
    - `fuel_type` - gasoline, diesel, cng, lpg, electric
    - `date_created` - when the ad was created
    - `date_last_seen` - when the ad was last seen. If sold_flag=1, this is also the date when the car was sold.
    - `price_eur` - list price converted to EUR
    - `Sold_flag` - Whether the car was sold through the platform or not. The company will earn a commission only on the cars sold through the platform
    - `Height_of_picture` - height of the picture used in the advertisements 
    - `Width_of_picture` - width of the picture used in the advertisements 
    - `Aspect_ratio` - aspect ratio of the picture used in the advertisements 
    - `Number of pictures` - Number of pictures of the car uploaded

2. `Current_inventory_data` - The dataset contains `~25k` rows related to the advertisements currently active (in the inventory) that can be displayed. There might be some cars which might be sold but their advertisement is still in the inventory so they need not be shown to users. The columns in this dataset are the same as the columns in the Historical Dataset.

3. `Commission data` - There are `~139` rows and the following columns in the dataset:
    - `Maker` - normalized all lowercase, manufacturer of the car
    - `Year` - The year where the slab was valid
    - `Commission` - the percentage commission earned by the company on a successful sale
    - `PS` - There is too much variance even within individual models with respect to pricing

## Questions (Assume Current Month -  April, 2017)

Suppose we are dealing with a second hand car sales platform like OLX or Car Bazaar.com. Where anyone who wants to sell his/her car can post an advertisement. Other users can browse different advertisements and buy a second hand car. The company will generate revenue based on commission from sales of cars. The company currently has `~25k` advertisements in the inventory data. **The end objective of the exercise is to create a ranked list of car advertisements in the current inventory which would optimize revenue for the company. **

### Please note:
1. Quality of answers is very important to us. Writing optimized codes is a key parameter in evaluation.
2. In your solution file/script, please mention the relevant question & question number as a heading/comment above the different sections in your codebase.
3. If you are taking an assumption in a certain question, please mention the same along with your solution
4. Some questions can be answered by simple EDA (exploratory data analysis), please share supporting data/ visualization wherever needed.
5. The assignment is to help us evaluate your grasp on the topic, so providing details into your thought process in a crisp & precise manner will help us understand your approach better.

### Questions:
1. Which body type has the highest demand in different seasons (Summer, Winter, rainy)?
2. In the current inventory, how many cars are highly overpriced? Create your own criteria and explain your approach.
3. Estimate how many new listings we can expect per month on the platform over the next 6 months.
4. How does uploading more photos impact the chance of a car getting sold? 
5. As a quick win, can you create rule-sets using advertisement heuristics which could be applied to filter out Ads which are bad in quality?
6. What are the top 3 features that you have created using the columns given in the data? What is your criteria of choosing Top 3 features?
7. Create a Deep Learning Model (using architecture, platform & framework of your choice), to create a ranked list of advertisements in the current inventory which could help the company maximize their revenue.
8. How did you measure the accuracy of your model? How did you identify that your model didn’t under/ over fit? Please share some visualizations and your interpretation/findings from the same.
9. Suppose, till now, the company was ranking the advertisements in a descending order on the basis of date_last_seen, so can you demonstrate the lift in performance of your model as compared to the current ranking criteria?
10. Can you explain in a step-by-step manner, how you performed various iterations and what impact did it have on the model accuracy?

**Please upload your analysis notebooks/scripts in a Github repository and email us the link to your repo at foundersdesk@yugen.ai with the subject `Assignment_solutions_yourname`.**
