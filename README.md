# Correlation-Between-IQ-And-Chess-Rating
Is there a relationship between Chess rating and IQ? To determine this, our group decided to pull data from 2 online resources and combined it with a third dataset containing well known abbreviations for country names in order to compare average IQ of countries to the amount of high quality Chess players those countries put out. 

### Step 1 Extracting data

This step was made possible by your friendly neighborhood teaching faculty. Shoutout to them for teaching us some hieroglyphs that made reading the HTML tables easy.
The HTML tables were read using pandas and then exported as csv files once they were relatively clean and then further had their headers changed once in csv form.


### Step 2 Transforming data

We merged all data to one Pandas DataFrame with columns starting with IQ by Country and Country Abbreviations and then finally merging on the Country abbreviations in the FIDE historical dataset. This transformation served as a filtering function as it essentially allowed us to only look at the countries that existed both in the Chess
players' list and the IQ by country list. 

Country_name - full name of country
IQ Average   - the average iq of the country
Country      - the short code for each country
rank         - the fide rank of a chess player
name         - the full_name of a chess player
rating       - the fide rating of a chess player
birth year   - birth year of a chess player


### Step 3 Loading Data

We had to drop the duplicate rank columns since that interfered with the next step. We opted to keep the Chess players position in the list of the historical Chess ratings. After that, sorting the data by those Chess rankings helped put into perspective the quality of players put out per country. 

### Step 3 Loading

By using the create_engine method from SQLalchemy we were able to open a connection using SQLite and from there added in our dataframe which we could then iterate over and further filter down if interested.

