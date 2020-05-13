README for Project 5 (group project)



# Notes about datasets
- Official column headers are here:
https://www.gdeltproject.org/data/lookups/CSV.header.dailyupdates.txt
- These are good for April 2013 - present so should be good for us
- Column headers in .xlsx format:
https://www.gdeltproject.org/data/lookups/CSV.header.fieldids.xlsx

#### The "tone" column is super interesting:
    "AvgTone. (numeric) This is the average “tone” of all documents containing one or more mentions of this event. The score ranges from -100 (extremely negative) to +100 (extremely positive). Common values range between -10 and +10, with 0 indicating neutral. This can be used as a method of filtering the “context” of events as a subtle measure of the importance of an event and as a proxy for the “impact” of that event. For example, a riot event with a slightly negative average tone is likely to have been a minor occurrence, whereas if it had an extremely negative average tone, it suggests a far more serious occurrence. A riot with a positive score likely suggests a very minor occurrence described in the context of a more positive narrative (such as a report of an attack occurring in a discussion of improving conditions on the ground in a country and how the number of attacks per day has been greatly reduced)."





# DOWNLOADS:
- MAY 5 raw CSV file here:
https://drive.google.com/open?id=1kP5tttaB41Qh1kZKLvkhL4TECdh9Alsl

- GDELT has about ten datasets. The one we looked at earlier today(Friday May 8) is the "GDELT 2.0 Event Database":
http://data.gdeltproject.org/events/index.html

- Overview of our dataset here
https://blog.gdeltproject.org/gdelt-2-0-our-global-world-in-realtime/

- Here's the full list of other datasets we could use:
https://blog.gdeltproject.org/the-datasets-of-gdelt-as-of-february-2016/

- We don't have to use AWS, they have other tools: https://www.gdeltproject.org/#downloading


# TO-DO list
- Finish gathering and concatenating data
- Conduct any remaining cleaning
- Get mapping program to work
- Fit mapping to GKG instead of Events dataset
- Find high-resolution world map shapefile
- Modeling:
    - Time series modeling?
    - Unsupervised methods??
- Evaluate??
    - Pick specific world news items and see if the map shows it?
- Conclusions/Recommendations
    - How good is the GDELT GKG data set for illuminating commodity shortages/gluts during disasters?
    - Would other GKG data sets be worthwhile?
    - Further steps?
    


# Traditional DS WORKFLOW
- Problem Statement
- Gather Data
- Explore Data
- Clean
- Feature Engineering
- Models:
    - Data Analysis:
        - quantity of shortage themes over time
    - Time-series:
        - difference data
        - forecast data
    - Unsupervised:
        - Cluster by time
        - Cluster by location
        - Cluster by tone severity
        - Cluster by multiple
- Evaluate
    - 
- Conclusions & Recommendations







