# toy_nlp_sentiment_django
NLP sentiment analyser for toy brands on Amzon with Django.

## requirements:
Django,
NLTK,
Pandas,
pickle,
!Depreciated: Matplotlib

![sentapp](https://user-images.githubusercontent.com/82896854/184564366-d66e1de8-50ed-4a10-98b4-fe692ca8f1dd.png)

# Introduction
This is a sentiment analyer for toy brands. Powered by data scraped from Amazon, with plans to implement Twitter data later.
Users can querey their favourite toy brands, as well as the products from these companies.

# How?
The back-end is implemented with Django, the front end is powered by plugins such as Bootstrap and Graph.js, and the data is scraped from Amazon.co.uk from ParseHub, as well as datasets found from Kaggle.

# File information
within the root directory you will find the following files:
1. toys_and_games.csv -> A massive dataset regarding the toys and games category found on Amazon
2. top.pkl !depreciated -> A list of top 10 toy brands found within my dataset
3. tomy_toys.csv -> data I have personally scraped from Amazon.co.uk via ParseHub. This CSV is merged into the master CSV in sentiment.py
4. test.csv !DEBUG -> an output CSV generated in PANDAS based on user queries
5. master.csv !IMPLEMENTING_CURRENTLY -> a master data lake of all data scraped from various sources
6. sentiment.py -> a python script which will determine sentiment of reviews found in the various data sets and serve this to Django for a sentiment:time graph to be displayed. It is also responsible for the caching of recent outputs.
7. run_results.json !NEED_TO_MOVE -> the raw data parsed about Tomy via ParseHub in JSON
8. run_results.json !NEED_TO_MOVE -> the raw data parsed about Tomy via ParseHub in CSV
9. my_classifier.pickle -> my classifier made in NLTK and trained on amazon reviews pulled from Kaggle. The training portion of this project can be found in /historical_ipyb
10. meta_toys_and_Games.csv -> the meta data about toys and brands on amazon via ASIN lookup
11. merge.py !IGNORE
12. manage.py -> how the server is run: $python3 manage.py runserver (ip:port)
13. freq.ipynb !IGNORE
14. clean_scraped.ipynb and cleaned_tomy.csv -> Files used to clean the raw datasets scraped
