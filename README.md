# Bitcoin Price and Public Sentiment

### Project Author
- Libin Huang | <u>[LinkedIn](https://www.linkedin.com/in/libinh/)</u>

---

### Table of contents
- <u>[Problem Statement](#Problem-Statement-and-Key-Objective)</u>
- <u>[Results](#Results)</u>
- <u>[Conclusion and Recommendations](#Conclusion_and_Recommendations)</u>
- <u>[Sources](#Sources)</u>

---

### Problem Statement and Key Objective

<b> Abstract </b>
- Cryptocurrency is one of the more speculative markets in today's time. With the rise of Bitcoin nearly reaching $20,000 in USD value in 2017 while still maintaining its intrinsic value in today's time, cryptocurrency is an commodity that can not be ignored. The motivation behind this project is to prove that human involvment plays a role in deciding Bitcoin's worth. 

<b> Problem Statement </b>
- To determine whether public emotion involvment and is a direct causation for the value of Bitcoin.

<b> Project Outline </b>
- Scraping online Reddit (r/bitcoin) data

Used PushShift API to scrape real time Reddit data for all of 2019, and into 2020.

- Data Wrangling

Removed duplicates, null values, spaces, and combining columns.

- Applying NLP Text normalization techniques

By normalizing text, which includes lower casing, removing stop words and unnessessary jargon, we are able to keep the lettings constant

- Sentiment scorer packages

By using NLTK Intensive Sentiment and TextBlob Analyzer, we're able to scale each post into a "sentiment" score.

- Neural Network Modeling


---

### Results
- The best model was the Summation Sentiment LSTM Neural Network Model with a MAPE score of 8.50, which was a 37.47% improvement from the Naive Baseline score (13.59). Augmenting sentiment scores along with Reddit frequency posts **does** have a correlation.
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



---

### Conclusion and Recommendations
- Reddit posts and overall cryptocurrency market value does have predicting value in forecast future bitcoin prices
- Developing a customized NLP text classifier charting text and price increase correlation
- Expand functionality and improve user-experience by building front-end with Flask or similar tool

---

### Sources
- https://medium.com/@datamonsters/text-preprocessing-in-python-steps-tools-and-examples-bf025f872908
- https://towardsdatascience.com/text-classification-with-state-of-the-art-nlp-library-flair-b541d7add21f
