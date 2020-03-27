# Bitcoin Price Prediction

### Project Author
- Libin Huang | <u>[LinkedIn](https://www.linkedin.com/in/libinh/)</u>

---

### Table of contents
- <u>[Problem Statement](#Problem-Statement-and-Key-Objective)</u>
- <u>[Executive Summary](#Executive-Summary)</u>
- <u>[Findings](#Findings)</u>
- <u>[Conclusion and Recommendations](#Conclusion_and_Recommendations)</u>
- <u>[Sources](#Sources)</u>

---

### Problem Statement and Key Objective

<b> Abstract </b>
- Cryptocurrency is one of the more speculative markets in today's time. With the rise of Bitcoin nearly reaching $20,000 in USD value in 2017 while still maintaining its intrinsic value in today's time, cryptocurrency is an commodity that can not be ignored. 

<b> Problem Statement </b>
- The intention of this project is to see if there's a correlation between Bitcoin Prices and the general public sentiment for Bitcoin.

<b> Key Objective </b>
- Build a forecasting model that will take sentiment scores for Reddit posts and see if there's an underlying trend in human emotion and post activity.

---


### Executive Summary
- The best model was the LSTM Neural Network Model with a RMSE score of 738.58 which was a 13.36% improvement from the Naive Baseline score. Augmenting sentiment scores along with Reddit frequency posts **does** have a correlation.
- Sentiment Scores alone are not a good feature point in predicting Bitcoin Pricing
- Challenges observed: Sentiment scores require a lot of processing power. Further endeavors would be to access external reliable processing power to run the packages.  

---

### Data Dictionary
| Column | Description |
| --- | --- |
| **Date** | Date format (mm/dd/yyyy) |
| **created_utc** | Cumulative sum of epoch time. |
| **score** | Cumulative sum of upvote popularity score per date. |
| **vader_neu_score** | Average NLTK neutral score for all the posts per date. |
| **vader_neg_score** | Average NLTK negative score for all the posts per date. |
| **vader_pos_score** | Average NLTK positive score for all the posts per date. |
| **vader_compound** | Average NLTK compound score for all the posts per date. |
| **blob_polarity** | Average Textblob positive/negative score for all the posts per date. |
| **blob_subjectivity** | Average NLTK subjectivity score for all the posts per date. |
| **sum_posts_x** | Number of posts per day. |
| **sum_posts_y** | Number of posts per day version 2. |
| **b_cash_price** | Bitcoin Cash Closing Price per day. |
| **btc_price** | Bitcoin Closing Price per day. |
| **ltc_price** | Litecoin Closing Price per day. |
| **etc_price** | Ethereum Closing Price per day. |



---

### Conclusion and Recommendations
- Reddit posts and overall cryptocurrency market value does have predicting value in forecast future bitcoin prices
- Continue building robustness of model with ensemble LSTM methods to continue training model and improving accuracy
- Further development of more years worth of posts to see if the model is realistic
- Developing a customized NLP text classifier charting text and price increase correlation
- Expand functionality and improve user-experience by building front-end with Flask or similar tool

---

### Sources
- https://medium.com/@datamonsters/text-preprocessing-in-python-steps-tools-and-examples-bf025f872908
- https://towardsdatascience.com/text-classification-with-state-of-the-art-nlp-library-flair-b541d7add21f
