# GA-DSI-Project-5 Executive Summary
### Nate Bukowski and Colin Simon

# Contents:
- [Problem Statement](#Problem-Statement)
- [Data Summary](#Data-Summary)
- [Mapping](#Mapping)
- [Models and Techniques](#Models-and-Techniques)
- [Conclusions, Limitations and Recommendations](#Conclusions,-Limitations-and-Recommendations)

# Problem Statement
Using data science to identify commodity supply events using global news data.

# Data Summary
**Data Source:**
- The data for this project was pulled using Google Cloud Platform's BigQuery.
- GDELT

**Datasets Analyzed:**
- [master_clean.csv](./data/master_clean.csv)
  -  1,100 rows, 11 columns

# Mapping


# Models and Techniques
- The goal of our modeling was to use K-Means Clustering, PCA and CountVectorizer to  find a classification model that performed best when classifying the month of the year an article was written. A pipeline of various parameters was run through a GridSearch on the following models:
  - K-Nearest Neighbors
  - Random Forest
  - Logistic Regression
  - Support Vector Machine

  Below are the accuracy scores for the best performing models:
  - **K-Nearest Neighbors:**
    - Train accuracy: 58.9%
    - Test accuracy: 37.5%

  - **Random Forest:**
    - Train accuracy: 100%
    - Test accuracy: 44.6%

  - **Logistic Regression:**
    - Train accuracy: 69.6%
    - Test accuracy: 36.9%

  - **Support Vector Machine:**
    - Train accuracy: 99.3%
    - Test accuracy: 42.4%

# Conclusions, Limitations and Recommendations:

*Conclusions:*
  - This is a tremendously powerful dataset that updates many times a day.
  - Event hotspots can be located.
  - Date can be predicted from the location, tone and theme of an article.

*Limitations:*
  - We only used English Articles.
  - Our modeling dataset was small (1,100 data points).
  - Multiple Machine Learning levels used.
  - Cloud computing is expensive.
  - Dataset could not be used for time series modeling.

*Recomendations:*
 - Research Google, GDELT algorithms and NLP classifications .
 - Nonprofit or significant sponsorship angle needed.
 - Cleaning/engineering to allow for time-series modeling and improvement to clustering model.
