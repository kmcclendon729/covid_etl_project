## Extract Source Data

We pulled csv our source data files freom Kaggle as follows:

* Hospital beds: https://www.kaggle.com/ikiulian/global-hospital-beds-capacity-for-covid19
* Covid 19 State and County files: https://www.kaggle.com/sudalairajkumar/covid19-in-usa

## Transform Data (Cleanup and Analysis)

We had to clean one of the csv data files in excel just a bit before loading it into the jupyter notebook as one file only had full state name and one had only the two digit postal code name for the state. 
We loaded the csv files into a jupyter notebook, creating a dataframe from each. We then began the cleanup as follows:

* Hospital beds df:
    * dropped unnecessary columns
    
* Covid States df:
    * dropped unnecessary columns
    * merged with Covid Counties df
    * renamed a few columns

## Load Data into Postres Database
* We created a database named covid_db with the following tables:
    * locations
    * avail_hospital_beds
    * cases

* Used SQLAlchemy to load our data into the our Postgres Database


## Notes/Issues Encountered
* The datasets pulled out of Kaggle weren't perfect. As mentioned above, we had to do a little cleanup before we could load them into our jupyter notebook
* The datasets themselves may also not have been complete datasets. For example, we noticed that in the hospital beds database, the numbers of available beds seemed off for some of the states. California had fewer beds than Alabama. Also, there were very few beds in the city of Sacramento. Far fewer than we know to exist. However, due to time constraints we had to work with the data we were able to gather.



