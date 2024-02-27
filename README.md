# Coupon Acceptance: Will a Customer Accept the Coupon?

# Project Overview

The project aims to analyze the data collected from an Amazon Mechanical Turk survey. Various driving scenarios are described in the survey, including the destination, current time, weather, and passengers. Using visualizations and data science techniques, we need to determine whether a customer accepted the driving coupon or not.

## Data

The data used in this project is from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’.  There are five different types of coupons -- less expensive restaurants (under \\$20), coffee houses, carry out & take away, bar, and more expensive restaurants (\\$20 - \\$50). .

## Data Description
Keep in mind that these values mentioned below are average values.

The attributes of this data set include:

1. User attributes
    -  Gender: male, female
    -  Age: below 21, 21 to 25, 26 to 30, etc.
    -  Marital Status: single, married partner, unmarried partner, or widowed
    -  Number of children: 0, 1, or more than 1
    -  Education: high school, bachelors degree, associates degree, or graduate degree
    -  Occupation: architecture & engineering, business & financial, etc.
    -  Annual income: less than \\$12500, \\$12500 - \\$24999, \\$25000 - \\$37499, etc.
    -  Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    -  Number of times that he/she buys takeaway food: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    -  Number of times that he/she goes to a coffee house: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    -  Number of times that he/she eats at a restaurant with average expense less than \\$20 per
    person: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    -  Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    

2. Contextual attributes
    - Driving destination: home, work, or no urgent destination
    - Location of user, coupon and destination: we provide a map to show the geographical
    location of the user, destination, and the venue, and we mark the distance between each
    two places with time of driving. The user can see whether the venue is in the same
    direction as the destination.
    - Weather: sunny, rainy, or snowy
    - Temperature: 30F, 55F, or 80F
    - Time: 10AM, 2PM, or 6PM
    - Passenger: alone, partner, kid(s), or friend(s)


3. Coupon attributes
    - time before it expires: 2 hours or one day

## Observation

- Carryout and Take Away and Restaurant(<20) coupons get used the most while Bar coupons get used the least.

- You are twice as likely to accept a Bar coupon if you are:
    - frequent the bar more than three times a month, or
    - above 25 years of age and frequent the bar more than once a month
    - frequent the bar more than once a month, and are not employed in the Farming, Fishing, or Forestry industry, and also happen to not be travelling with kids as passengers.
    - frequent cheap resturants more than 4 times a month and earn less than 50K
- Overall, there seems to be strong correlation between the number of times you visit a bar and your likelihood of accepting a bar coupon

![Coupon Acceptance Bar Plot Image](https://github.com/AtulTrikha/CouponAcceptance/blob/main/images/coupon_acceptance.png "Coupon Acceptance Bar Plot")

### Additional Plots:

**Using a bar plot to visualize the coupon column:**\
![Problem 1 Visualization](https://github.com/AtulTrikha/CouponAcceptance/blob/main/images/Visualize_Coupon_Using_Barplot.png "Problem 1 Visualization")
<br />

**Using a histogram to visualize the temperature column:**\
![Problem 2 Visualization](https://github.com/AtulTrikha/CouponAcceptance/blob/main/images/Visualize_Temprature_Using_Histogram.png "Problem 2 Visualization")
<br />

 **Acceptance rate between those who went to a bar 3 or fewer times a month to those who went more:**\
![Acceptance Rate Problem 3](https://github.com/AtulTrikha/CouponAcceptance/blob/main/images/Visualizing_Bar_Coupon_Acceptance_3_or_Fewer_or_More_Than_3.png "Acceptance Rate Problem 3")
<br />

**Acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to the all others:**\
![Acceptance Rate Problem 4](https://github.com/AtulTrikha/CouponAcceptance/blob/main/images/Visualizing_Bar_Coupon_Acceptance_Visited_Bar_More_Than_Once_Over_25.png "Acceptance Rate Problem 4")
<br />

**Acceptance rate between drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry:**\
![Acceptance Rate Problem 5](https://github.com/AtulTrikha/CouponAcceptance/blob/main/images/Visualizing_Bar_Coupon_Acceptance_Once_A_Month_Not_Farming_Fishing_Forestry_No_Kid_Passengers.png "Acceptance Rate Problem 5")
<br />

**Compare the acceptance rates between those drivers who:**\
 - go to bars more than once a month, had passengers that were not a kid, and were not widowed OR
 - go to bars more than once a month and are under the age of 30 OR
 - go to cheap restaurants more than 4 times a month and income is less than 50K.
![Acceptance Rate Problem 6](https://github.com/AtulTrikha/CouponAcceptance/blob/main/images/Visualizing_Bar_Coupon_Acceptance_Based_On_Criteria_6.png "Acceptance Rate Problem 6")
<br />

## Link

- Data: https://github.com/AtulTrikha/CouponAcceptance/blob/main/data/coupons.csv

- Notebook: https://github.com/AtulTrikha/CouponAcceptance/blob/main/WillCustomerAcceptCoupon.ipynb
