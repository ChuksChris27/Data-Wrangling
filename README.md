# Data-Wrangling
This shows the wrangling of data for tweets gotten from the Twitter archive of WeRateDogs

# WRANGLING DATA REPORT
The twitter project as I call it was a very challenging one. First of all, in trying to wrangle I encountered so many problems. Not that they will become a problem in the future as I have learnt from them, it is also important to note this.

# GATHERING THE DATA
I started the wrangling process by importing the libraries I’d need and began gathering my data. I used the ‘twitter_archive_enhanced.csv’ file provided by udacity, and read it into a pandas dataframe. I then read the ‘image_prediction.tsv’ by using the response library to get a response from the url provided by Udacity, and then reading the content to a dataframe. The response.get gave me a 200 which is an indication that it was read successfully.

Then came the hard part. To get the third data needed to wrangle from the twitter API. I applied for developer access from twitter and got elevated access. But I was unable to fetch the tweets from the API. I used the twitter.py code provided by Udacity and it returned an empty file after so many failures from the tweepy.tweepyException function.

I resolved to use the collated data from Udacity and after so many attempts, I finally had my third data with the desired column - retweets and favourite counts.

# ASSESSING THE DATA
- I assessed the data visually and programmatically, well, in a 10%-90% ratio, because it is easier that way to assess.
- I identified eight(8) quality issues and two(2) tidiness issues

# QUALITY ISSUES
- The tweet_id has dtype 'int64' in all datasets

- There are so many NaN values in the 'in_reply_to_status_id', 'in_reply_to_user_id', 'retweeted_status_id', 'retweeted_status_user_id','retweeted_status_timestamp' columns

- The timestamp is dtype 'object'

- There are duplicates in the 'jpg_url' column

- Names have invalid entries such as 'None', 'a','an' etc

- There's date and time in the timestamp column. It can be separated into their individual columns

- The source has urls. Extract the source to have the strings and not the url

- P1, P2, P3 have underscores(_) in their str instead of spaces

# TIDINESS ISSUES
- Some dogs are doggo, floofer, puppo, pupper in the twitter_archive data. These are unnecesary columns

- All the data set have some columns in common

# CLEANING THE DATA
I used the Define-Code-Test method to clean each of the identified quality and tidiness issues and the codes were successfully run.

# SUMMARY
The data wrangling process was hectic and challenging, but it was educational personally as I learnt from the many researches I made to clean my data and wrangle it successfully
