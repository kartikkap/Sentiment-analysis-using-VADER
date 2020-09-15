# Sentiment-analysis-using-VADER
In this project the process of sentiment analysis of live tweets is explored using the VADER library in python. For demonstration sentiments around the Indian economy during COVID-19 has been performed along with reception of government initiatives and the sentiments of two dominant e-commerce players in India is explored.

Pre-requsites : 
Twitter API licsence 
Tweety
VADER
matplotlib

Python code walkthrough

Step 1 :
With the objective to analyze the sentiment of live tweets from twitter, the twitter API was
used to stream the live tweets. To use the twitter API we first need to request twitter for
access and post that we get authentication keys from twitter to connect to the API. Once
we get the authentication keys from twitter we use the tweepy library to connect with the
API. Tweepy can be downloaded by pip install tweepy. It supports OAuth authentication.
Authentication is handled by the tweepy.OAuthHandler class.
 

Step 2 :
After authentication we need to gather the live tweets based on a particular search creteria
using tweepy. For this we invoke tweey.coursor and use the api.search method and pass
our search parameters through the cursor. For testing our connection user.api method is
used which will display the connected user’s name if a successful connection is established
with the twitter API.
 
Step 3 :
Now we import the VADER library and pass each tweet searched based on our search
parameter into the method polarity_scores to get its sentiment score. The overall
sentiment of each tweet is calculated by analyzing the compound score returned from the
method and based on the following if conditions the search term is categorized as positive,
negative or neutral. The compound score of each tweet is accumulated in the pos, neg,
neutral variables and at the end a bar graph is plotted using matplotlib to show the overall
sentiment score of the searched term.
The object SentimentIntensityAnalyser is called and the method polarity_scores is used to
get the positive, negative, neutral and compound score of the sentence.
