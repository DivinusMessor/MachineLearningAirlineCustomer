# What Makes a Happy Airline Passenger?

# Introduction
  By BayTech
- Warren Ngoun (wngoun@csumb.edu)
- Yukio Rivera (yrivera@csumb.edu)
- Jennah Yasin (jyasin@csumb.edu)
- Luis Jimenez Barrios (ljimenezbarrios@csumb.edu) 
Note: We all worked collaboratively with VS Code Live Share and only had one person commit the changes.

---
# Intro

**Objective:** The objective of our research project is to investigate the factors that are most relevant and most correlated to passenger satisfaction in airline travel. We chose to utilize the Airline Passenger Satisfaction dataset due to our shared interest in creating positive flight experiences and our belief that airlines should value their passengers' reviews.

**Research Question:** What are the key features that determine a flight passengers overall satisfaction?

**Importance:** Advising airlines with passenger’s reviews in order to maximize satisfaction 

**Project Plan:** 
  - Predicting which factors are most relevant to passenger’s satisfaction.
  - Dropping features that aren’t significant
  - Using “satisfaction” feature as target variable
  - Finding top features using forward feature search

**Hypothesis:**
Based on our personal preferences and past experience as passengers, we believe that the most important features that affect satisfaction would be:     Seat comfort, in-flight entertainment, cleanliness, and food & drinks.



# Selection of Data

**Source of dataset:** https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction

**Characteristics of data:**

  - Gender: Gender of the passengers (Female, Male)
  - Customer Type: The customer type (Loyal customer, disloyal customer)
  - Age: The actual age of the passengers
  - Type of Travel: Purpose of the flight of the passengers (Personal Travel, Business Travel)
  - Class: Travel class in the plane of the passengers (Business, Eco, Eco Plus)
  - Flight distance: The flight distance of this journey
  - Inflight wifi service: Satisfaction level of the inflight wifi service (0: Not Applicable; 1-5 stars)
  - Departure/Arrival time convenient: Satisfaction level of Departure/Arrival time convenient
  - Ease of Online booking: Satisfaction level of online booking
  - Gate location: Satisfaction level of Gate location
  - Food and drink: Satisfaction level of Food and drink
  - Online boarding: Satisfaction level of online boarding
  - Seat comfort: Satisfaction level of Seat comfort
  - Inflight entertainment: Satisfaction level of inflight entertainment
  - On-board service: Satisfaction level of On-board service
  - Leg room service: Satisfaction level of Leg room service
  - Baggage handling: Satisfaction level of baggage handling
  - Check-in service: Satisfaction level of Check-in service
  - Inflight service: Satisfaction level of inflight service
  - Cleanliness: Satisfaction level of Cleanliness
  - Departure Delay in Minutes: Minutes delayed when departure
  - Arrival Delay in Minutes: Minutes delayed when Arrival
  - Satisfaction: Airline satisfaction level(Satisfaction or `0`, neutral/dissatisfied or `1`)

**Feature Engineering:** The feature engineering that we implemented was using the One-Hot Encoding technique in order to convert any features that contain categorical data into numerical values in order to be able to use this data for machine learning later on. 




# Methods

**Materials and Tools:**

- First, we gathered our data set from a Kaggle repo on Airline passenger satisfaction, it was a cleaned up data set from another Kaggle repo, but the source of the data from that repo was unknown.
- Once we had the data, a lot of the pre-processing was already done, but we still had to do some cleanup and encoding. After combing through the potential Classifier models and parameters, we ended up using Decision Trees and Forward Feature Selection to answer our question.
- Kaggle to find the Airline Passenger Satisfaction data set
- VS Code & GitHub
- Pandas, NumPy, SciKit-Learn for implementation of project
- Course materials: Previous labs & assignments
- Machine Learning
- Decision Trees 
- Forward Feature Selection
# Decision Tree Representing Final Model
![Our Decision Tree](https://github.com/BayTech-CSUMB/CST383Final/blob/main/decisionTree.png?raw=true)

# Results

Based on our data analysis and manipulation, we were able to find the top 10 most effective features of our data set. The top 10 features were found to be: 

   - Online boarding
   - Type of Travel_Business travel
   - Inflight wifi service
   - Gate location
   - Baggage handling
   - Customer Type_disloyal Customer
   - Class_Business
   - Inflight Service
   - Seat comfort
   - Customer Type_Loyal Customer
 
 
**However, from these top 10 features, we decided to use the first top 5 as our predictors since the overall accuracy didn’t significantly increase when we added more of them.**

**Hypthesis Analysis:** We realized that our hypothesis was actually not completely correct as the top features differed from our expectations. 

# Top feature - Online Boarding:

This countplot represents how effective the Online Boarding feature is in terms of determining whether a passenger is satisfied or not. 
The countplot provides valuable insights into the efficiency of the Online Boarding feature as a determinant of passenger satisfaction. 

![A Graph of Satisfaction](https://github.com/BayTech-CSUMB/CST383Final/blob/main/satisfactionBoarding.png?raw=true)


As is evident from the plot, there is a clear positive correlation between passenger satisfaction and the rating assigned to the Online Boarding feature, with the number of satisfied passengers increasing significantly as the rating increases from 1 to 5. Conversely, passengers who rated the feature below 3 are generally found to be dissatisfied. Overall, this analysis underscores the critical role of Online Boarding in shaping passenger satisfaction and highlights the need for airlines to ensure that this feature is optimized to provide a seamless and satisfactory boarding experience for passengers.

# Confusion Matrix

![Our Confusion Matrix](https://github.com/BayTech-CSUMB/CST383Final/blob/main/confusion.png?raw=true)

Our model ended up having an around 88% accuracy which our confusion matrix results showcase. 
With 1541 false positives that were predicted satisfied but actually dissatisfied and 1481 false negatives which were actually satisfied customers but predicted as dissatisfied for a total of 3022 incorrect predictions out of 25976 customers.

# Discussion

**Significance of findings:**

   - The answer from the project implies that Decision Trees can provide a quick and accurate prediction for customer satisfaction with air travel based
     on a set of predictors. 
   - This is significant because it provides airlines valuable insights into which factors are most critical for customer satisfaction, allowing them to     
     allocate resources accordingly. 
   - For future researchers, our findings of top predictors, such as Online boarding and Inflight Wifi, are strong indicators of customer satisfaction.
   - The identification of the best 5 features from a larger list of 26 is a unique contribution to the field.
   - In terms of tools, the project investigated the use of Python libraries such as Pandas, NumPy, Scikit-learn, and Matplotlib, which are widely used in
     data analysis and machine learning. 


# Summary

**Throughout the process of the project, from finding a dataset all the way down to hyper-parameter tuning of our model, we learned and practiced a great deal of machine learning fundamentals like:**
   - The importance of cleaning up and tweaking features in your data
   - How visualizations help with understanding your data and your model results
   - Experimenting with different potential models and hyper-parameters like kNN and Decision Trees
   - Seeing how to compute and determine effective predictors

**Conclusion:** Lastly what we found most surprising were that the most important features of overall satisfaction were things like Online Boarding and gate location, which we had not expected as from our personal preferences and experiences we preferred comforts like or good food & drink or high cleanliness on our flights.  

