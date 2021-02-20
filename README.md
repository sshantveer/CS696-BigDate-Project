### Big Data Class Project 
### Analyze the effect of Elon Musk's tweets on Tesla stock price.
    - Using data set available from kaggle
        - Elon Musk tweets from 2012 to 2017 https://www.kaggle.com/kulgen/elon-musks-tweets
            - This contains all tweets made by @elonmusk, his official Twitter handle, between 11/16/2012 and 09/29/2017.
        - Tesla stock price data https://www.kaggle.com/rpaguirre/tesla-stock-price
            - 06/29/2010 to 03/17/2017.

    - Special Library Used : TextBlob
        - pip install -U textblob
        - https://textblob.readthedocs.io/en/dev/install.html
#### Approach taken to correlate the two data sets.
    - Tweet
        - Clean tweet data and stock data.
        - Make sure both the data belong to a given date range. (May be not required)
        - Remove unwanted columns from the column.
            - Tweet -> remove 'user', 'row ID' -> not required.
        - Analyze tweets using TextBlob library.
        - Based on this analyses, categorize tweet as 'positive', 'negative' or neutral
        - Since there are multiple tweets in a day, get the maximum sentiment of the day and assign this to the day.

    - Stock data
        - Calculate the day's percent change. [(close_price-open_price)/(close_price)]*100
        - Merge Tweet and Stock data on 'Time' field.
            - Use inner merge, i.e consider only matching dates.

### Analysis:
    - Run machine learning on the merged/prepaired and calculate correlation between tweet sentiment and stock price change sentiment.
    - Used linear regression and random forest to develop the model.

### Conclusion:
    - As per the data, the model was not able to predict any correlation between Elon Musk's tweets and Tesla stock price changes.# CS696-BigDate-Project
 
