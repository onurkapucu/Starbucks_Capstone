# Starbucks Capstone Project
This repository holds the data and the jupyter notebook of my work for Udacity Datascience Nanodegree's Starbucks Capstone Project

## Project Overview
Starbucks periodically makes offers to it's customers to promote sales and award loyalty. Customers receive offers in 3 forms:

BOGO, Discount and some informational offers with no reward value. Each offer type has a difficulty and reward value and validity period. 

Offer information can be found under "portfolio.json" file in "/data" folder.

Starbucks targets to drive customers to purchase products via these offers yet doesn't want to lose money on customers who were already going to make a purchase. In order to do so, we are asked to make an analysis on a simulated transaction history file called "transcript.json" under "/data" folder as well. This file contains the list of events with dates.

In order to analyse the customers we also have a customer database called "profile.json". This file contains information such as customer age, gender, income, membership date. My analysis targets to find the customer demographics that Starbucks gets the best outcome when an offer is sent to.

## Files

### \data

Holds the databases used in the analysis. Namely;

**portfolio.json-** Starbucks' offer types, rewards, validity durations, difficulty 
**profile.json-** Simulated customer database with membership start time, age, gender, income
**transcript.json** Simulated transaction log. Logs when offers are received viewed and completed by users and spendings made by users during the given 720 hours.


### Notebook - Starbucks_Capstone_notebook

My work and explanations for each step can be found on the jupyter notebook file called "Starbucks_Capstone_notebook". In this notebook, I first investigated the the databases, cleaned the outliers and did the necessary warping for data types and formats. 
Then I started analyzing the data asking several business questions. I investigated the gender, income, age relations together with performance of offer types. 

I grouped offer completions into 2 groups: Intentional and Non-Intentional.

Intentional completes are the ones where user viewed the offer before completing it. This means that user was aware of the offer and either made the purchase intentionally to complete the offer or knew that he/she is awarded for loyalty. 

Non-Intentional completes, on the other hand; are the ones where user completed the offer without even knowing about it. In this case not only Starbucks lost money, but also customer didn't feel rewarded.

Notebook uses kernel for Python 3.

#### Libraries

Throughout the analysis I have used following python libraries

**Pandas:** To load the given databases into a dataframe format. It also allowed us to select, transform, clean, process, analyze the data easily.

**Numpy:** To run numerical calculations such as offer start and end times etc...

**json:** To load json data that we are given

**matplotlib.pyplot:** To visualize plots mostly in histograms, bar plots and scatter

**Axes3D of mpl_toolkits.mplot3d:** To see multidimensional 3D scatter relations

**datetime, timedelta:** To convert dates in dataframes to date format for easier calculations

**tqdm:** To track for loop process state

### Pickle(pkl) Files

One can find two pickle files in the repo; namely, intentional_completes.pkl and values.pkl. These files are saved seperately to eliminate process repition if notebook needed to be run again. 

**intentional_completes** holds the information for offers that are intentionally completed in the transcript file. Columns are user_id,	start_time,	offer_id,	end_time,	time_viewed,	time_completed.

**values** is the dataframe created from the value column of the transcript database. In order to create values dataframe, value column is treated as a dictionary.

## Outcome

My notebook consists of my study with graphs and analysis. You can find comments and my thought process written in between each analysis. 

### Main Points

I made conclusions in 3 different areas: Gender Based, Offer Based and Income Based

#### 1- Gender

- Looking at all of the plots, we can say that we need a larger dataset gender group Other to make any decisive conclusions. Gender “O” consists around 1/60th of our dataset.

- We can say that female customers complete offers more than male customers. However, a good portion of them is nonintentional. In order to increase our offer performance, I decided to look into each offer seperately

#### 2- Offers

- Intentional offer complete ratio is higher for female between ages 35-55. This is valid both for bogo and discount offers. For male customers, we see larger variation in ratios within very small age differences. Making it harder to make a conclusion.

-Offer ‘0b1e1539f2cc45b7b9fa7c272da2e1d7’ has significantly less completion compared to other offers. This is the hardest offer and intentional completes average around %20 both for male and female customers.

- Offer ‘fafdcd668e3743c1bb461111dcafc2a4’ has the highest completion rate both for female and male customers. 3/4 of female customers who received this offer, completed it at least once.

#### 3- Income

Based on our scatter plot in CRISP-DM analysis, there was a very significant behaviour for consumers with income below $45,000 and above $100,000.

This is one of the most obvious patterns in the whole analysis. Offer performance peaks for customers with incomes between these levels.

## Medium Article
I also wrote a summary on Medium,https://medium.com/@onurkpc/how-would-you-like-your-coffee-offers-a535cdba3198.
