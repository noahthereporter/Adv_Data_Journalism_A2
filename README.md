# Adv_Data_Journalism_A2

# Analysis of New York City EV registrations vs. avaliable public chargers — 12/2024

This repository contains data, analytic code, and findings that support portions of the article, “[NYC EV charging installs can't keep up with adoption](https://wwe.link.com),” published 12/06/2024. Please read that article, which contains important context and details, before proceeding.

## Data

This analysis uses two CSV files.

The CSVs come from the following sources:

- Name of source: [New York State OpenData](https://data.ny.gov/Transportation/Vehicle-Snowmobile-and-Boat-Registrations/w4pv-hbkt/about_data)
  - `Vehicle__Snowmobile__and_Boat_Registrations_20241203.csv`: Raw data of vehicle registrations in the state.

- Name of source: [New York City OpenData](https://data.ny.gov/Energy-Environment/Electric-Vehicle-Charging-Stations-in-New-York/7rrd-248n/data)
  - `Electric_Vehicle_Charging_Stations_in_New_York.csv`: Raw data of EV chargers in New York state.

## Methodology

The notebook [`NYC_EVs_vs_Infrastructure.ipynb.ipynb`](notebooks/NYC_EVs_vs_Infrastructure.ipynb.ipynb) performs the following analyses:

##### Part 1: Filtering

- After compiling the notebook and importing the data, I needed to filter each dataset down to the geographical and EV focused needs of the project.
  -New York State Registration Data: This was filtered by Record Type to specify it was an automobile, Registration Class to narrow it down to passenger vehicles, County to narrow it down to specifically vehicles used in New York City and Fuel Type to narrow down to electric vehicles.
  -New York State Charger Data: This was filtered by ZIP code to narrow the chargers to those just within New York City. I created five lists within the code with Zip Codes provided by [Zip-Codes](https://www.zip-codes.com/) and cleaned them in a [Google Sheet](https://docs.google.com/spreadsheets/d/1T9KsswpceAEB8igOB3k95JAsupEvjUtfvYjHGQ9XF8M/edit?usp=sharing).


##### Part 2: Comparing

-I then did a simple compairson by summing the number of plugs for each type of charger per county via a pivot table and ran a count pivot table for the number of reported EVs for the city per county as of December 2nd.
-I then merged them on the county and created input data for plotting.
-I then plotted them on a horizontal bar graph to show the EVs vs. the infrastructure.


## Outputs

-The notebooks output this CSV, which contains the final pivot table: NYC EV Life.csv.
-The notebook out this jpg, which is the final pivot table in graph form: EV Chargers vs Vehicles Graph.jpg

## Running the analysis yourself

You can run the analysis yourself. To do so, you'll need the following installed on your computer:

- Python 3

Python Libraries
- Pandas
- MatPlotLib

## Licensing

All code in this repository is available under the [MIT License](https://opensource.org/licenses/MIT). The data file in the output/ directory is available under the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0) license. All files in the data/ directory are released into the public domain.

## Feedback / Questions?

Contact Noah at noahthereporter@gmail.com
