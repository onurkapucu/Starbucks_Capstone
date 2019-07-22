# Starbucks Capstone Project
This repository holds the data and the jupyter notebook of my work for Udacity Datascience Nanodegree's Starbucks Capstone Project

## Project Overview
Starbucks periodically makes offers to it's customers to promote sales and award loyalty. Customers receive offers in 3 forms: BOGO, Discount and some informational offers with no reward value. Each offer type has a difficulty and reward value and validity period. 
Offer information can be found under "portfolio.json" file in "/data" folder.

Starbucks targets to drive customers to purchase products via these offers yet doesn't want to lose money on customers who were already going to make a purchase. In order to do so, we are asked to make an analysis on a simulated transaction history file called "transcript.json" under "/data" folder as well. This file contains the list of events with dates.

In order to analyse the customers we also have a customer database called "profile.json". This file contains information such as customer age, gender, income, membership date. My analysis targets to find the customer demographics that Starbucks gets the best outcome when an offer is sent to.

## Notebook

My work and explanations for each step can be found on the jupyter notebook file called "Starbucks_Capstone_notebook". In this notebook, I first investigated the the databases, cleaned the outliers and did the necessary warping for data types and formats. 
Then I started analyzing the data asking several business questions. I investigated the gender, income, age relations together with performance of offer types. 

I grouped offer completions into 2 groups: Intentional and Non-Intentional.
Intentional completes are the ones where user viewed the offer before completing it. This means that user was aware of the offer and either made the purchase intentionally to complete the offer or knew that he/she is awarded for loyalty. 
Non-Intentional completes, on the other hand; are the ones where user completed the offer without even knowing about it. In this case not only Starbucks lost money, but also customer didn't feel rewarded.

Notebook uses kernel for Python 3. 

## Outcome

My notebook consists of my study with graphs and analysis. You can find comments and my thought process written in between each analysis. 
I also wrote a summary on Medium,https://medium.com/@onurkpc/how-would-you-like-your-coffee-offers-a535cdba3198.
