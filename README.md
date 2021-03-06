# Twitter-NLP-SNA
This is the code used in my MPhil project at the University of Cambridge, analysing political behaviour and communication on Twitter using Social Network Analysis and Natural Language Processing. 

Note: 
All code is executed in IPython, hence executing a line such as '>>> list_name' prints out the entire list titled 'list_name', without requiring a 'print(list_name)' statement. 

## This collection of code does the following: 
  1. parse in a pre-made csv file of elites and their Twitter accounts, as of March 2020 (elites include UK MPs, MEPs, and Political Party accounts) 
  2. connect to the Twitter API (using a private set of keys, which will need to be re-created if this code were to be replicated), collect all followers_IDs of each of the elites, saving them in separate files titled 'fillowers_{elite}.csv'
  3. build a network of elites and their followers, split the network up into LEFT and RIGHT (remove overlapping/central nodes); store side for main analysis
  4. 
  5. 
  6. randomly sample 100,000 user_ids from LEFT and 100,000 user_ids from RIGHT network 
  7. collect 200 most recent tweets from each of the users in LEFT and RIGHT networks, saving into MongoDB database 
  8. filter the users in each sample by activity 
  9. apply POS tagging to find nouns, proper nouns etc. in Tweets; calculate noun proportions for main analysis 
  10. calculate network centrality values for all nodes; store values for main analysis 
  11. draw the networks 
  12. clean words in tweets (lowercase, drop 's etc.), find most frequently used ones and visualise
  13. repeat word analysis after excluding pronouns 
  
## Packages required: 
- import pymongo
- from pymongo import MongoClient
- import json 
- import keys -- #this is a file with my keys for the Twitter API - will need to be re-created by anyone willing to replicate API access, and their own keys will need to be obtained from the Twitter developers website
- import pandas as pd
- import tweepy
- import timeit
- import time
- import pprint
- import datetime
- from datetime import datetime, timedelta
- from email.utils import parsedate_tz
