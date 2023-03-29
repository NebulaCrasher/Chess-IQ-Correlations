# Correlation-Between-IQ-And-Chess-Rating
Is there a relationship between Chess rating and IQ? To determine this, our group decided to pull data from 2 online resources and combined it with a third dataset containing well known abbreviations for country names in order to compare average IQ of countries to the amount of high quality Chess players those countries put out. 

### Step 1 Extracting data

HTML tables were extracted using pandas, reformatted and then exported as csv files once the data were relatively clean. More descriptive headers were added once the data was in csv form.


### Step 2 Transforming data

All data was merged into a singular Pandas DataFrame. This transformation served as a filtering function as it essentially allowed only countries that were referenced in both preliminary data sets. The following is an overview of the column header names and their meanings.

Country_name - full name of country
IQ Average   - the average iq of the country
Country      - the short code for each country
rank         - the fide rank of a chess player
name         - the full_name of a chess player
rating       - the fide rating of a chess player
birth year   - birth year of a chess player


### Step 3 Loading Data

There were duplicate rank columns that needed to be dropped as they were causing issues with the data reading. After dropping one of the rank columns, chess players were arranged by rating  by country. Sorting the data by those Chess rankings helped put into perspective the quality of players put out per country. 

### Step 3 Loading

By using the create_engine method from SQLalchemy we were able to open a connection using SQLite (a relational database) and from there import our dataframe which we could then iterate over and further filter down if interested.

### Findings

Despite being 10th in the world IQ chart Russia placed 25 players into the top 100 list while China despite being 3rd in IQ only placed 6 comparatively. This does not indicate a strong relationship between average IQ and amount of players in the Fide historical top 100 list. However, it is worth noting that all top 100 players were from countries that were ranked 25 or above in the IQ standings.

### Sources
https://www.kaggle.com/datasets/odartey/top-chess-players

https://brainstats.com/en/average-iq

https://laendercode.net/en/3-letter-list.html 
