# WeRateDogs
This is a project report for the steps I followed throughout my wrangling journey.
Gathering:
Here the needed data is collected, for WeRateDogs project I had three sources of data and information:
1.	Twitter_archive_enhanced.csv was downloaded manually as it was attached in Udacity platform and imported to my workspace using pandas function pd.read_csv.
2.	Image_prediction.tsv is the second file that was downloaded from webserver using requests library get function and pd.read_csv to import URL. This file has been created using machine learning to provide predictions for shared dogs’ photo.
3.	The third file was imported from twitter API using tweepy library. This file has retweet and favorite counts for each tweet.
Assessing:
For this step we inspect the imported datasets visually and programmatically and check for quality and tidiness issue.
1.	First, the data was inspected visually and messy data has been highlighted using Excel and also jupyter notebook for some.
2.	Second, datasets was checked also programmatically using jupyter notebook.
The assessment addressed points were as following:
Quality Aspects
a.	`archive_df` Dataset
1.	Data types(consistency issues):
- Some tweets are retweets and replies.
- Coulmns with almost all NaN values 'in_reply_to_status_id', 'in_reply_to_user_id', 'retweeted_status_id', 'retweeted_status_user_id'.
- `tweet_id` is not in appropriate format.
- 'timestamp' not in datetime format.
2.	Completeness issues:
- Defected names in 'name' column.
3.	Accuracy issues:
- 'rating_numerator' column has suspected values.
- 'rating_denominator' column has wrong values.

b.	`image_predictions_df` Dataset
4.	Completeness issues:
- Some tweets don't have photos.
Tidiness Aspects
a.	`archive_df` Dataset
- Values are column names 'doggo', 'floofer', 'pupper', 'puppo'.
b.	`image_predictions_df` Dataset
- Values are column names 'p1', 'p2', 'p3', etc.. .
c.	`api_df` Dataset
- `api_df` not in the same table with `archive_df`.
Cleaning:
Here the step where we filter the data and clean it according to the addressed issues in the assessment.
Three basic steps were followed for each assessed issue which are: Define, Code and Test.
Tidiness Aspects
a.	`archive_df` Dataset
- Values are column names 'doggo', 'floofer', 'pupper', 'puppo'.
Define
switch the column headers to be values not variables using pd.melt inquiry.
code
put a cod to clean the issue here.
Test
Check and make sure that the problem is clear.
This was the form I used for cleaning each issue.
