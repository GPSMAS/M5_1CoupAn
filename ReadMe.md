# Context
Imagine driving through town and a coupon is delivered to your cell phone for a restaraunt near where you are driving. Would you accept that coupon and take a short detour to the restaraunt? Would you accept the coupon but use it on a sunbsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaraunt? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?

Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?

# Data

This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’. There are five different types of coupons -- less expensive restaurants (under $20), coffee houses, carry out & take away, bar, and more expensive restaurants ($20 - $50).

## Data Description
Keep in mind that these values mentioned below are average values.

The attributes of this data set include:

User attributes

Gender: male, female
Age: below 21, 21 to 25, 26 to 30, etc.
Marital Status: single, married partner, unmarried partner, or widowed
Number of children: 0, 1, or more than 1
Education: high school, bachelors degree, associates degree, or graduate degree
Occupation: architecture & engineering, business & financial, etc.
Annual income: less than $12500, $12500 - $24999, $25000 - $37499, etc.
Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Number of times that he/she buys takeaway food: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Number of times that he/she goes to a coffee house: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Number of times that he/she eats at a restaurant with average expense less than $20 per person: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Contextual attributes

Driving destination: home, work, or no urgent destination
Location of user, coupon and destination: we provide a map to show the geographical location of the user, destination, and the venue, and we mark the distance between each two places with time of driving. The user can see whether the venue is in the same direction as the destination.
Weather: sunny, rainy, or snowy
Temperature: 30F, 55F, or 80F
Time: 10AM, 2PM, or 6PM
Passenger: alone, partner, kid(s), or friend(s)
Coupon attributes

time before it expires: 2 hours or one day



# General Descpritcion of repository

**This repository contains the project for Module 5 --- AI course.**

It is based on the analysis of a provided file, coupons.csv, with the objective of determining whether drivers will use the coupons.
The project includes:

A data folder with the aforementioned file.
An img folder with the generated image files.
An output folder with the Excel files generated as results of the analysis.

Il file notebook è al seguente link: [view the notebook](WCAC_v2.ipynb)

Il progetto si trova anche su github: **https://github.com/radema/Controllo-CUP.git**

The analysis consists of several sections (described in more detail directly in the file WCAC_v2), which are:

### Investigate the dataset

Section where we analyze the DataFrame and make some changes to the data in the file to facilitate future operations.

### Changing data


Section of the code where the changes to the data, analyzed and described in the first section, are applied.

### General Analysis

Section where we perform analyses and general considerations. It specifically emerges that temperature is not a significant variable, whereas the variable weather appears to be more significant both in terms of the data present in the DataFrame and the results. Additionally, it is noted that the most accepted coupon categories are take away and cheap restaurant.

You can view the related image [Coupon Frequency](img/coupon_frequency.png)


### Detailed Analysis - Investigating the Bar Coupons

In this section, only coupons categorized as bar are analyzed. Calculations and groupings are performed within this category, and some results are reported in:

- immagine: [Percentuali per Categorie individuate](img/percent_bar_cat_ass4.png)
- file dati: [Percentuali per Categorie individuate](output/BarCouponAnalysis.xlsx)
- descrizione nella specifica sezione del file notebook di cui il link all'inizio

### Detailed Analysis - IInvestigating the "Restaurant(<20) Coupons "

In this section, only coupons categorized as bar are analyzed. Calculations and groupings are performed within this category, and some results are reported in:

- immagine: [Percentuali per Categorie individuate](img/PercentChRest_Cat_GR_ChpRest.png)
- file dati: [Percentuali per Categorie individuate](output/CheapRestaurantCouponAnalysis.xlsx)
- descrizione nella specifica sezione del file notebook di cui il link all'inizio
