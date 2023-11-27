---
name: IS445 Final Project Jekyll Webpage (Fall 2023)
tools: [Python, HTML, vega-lite]
image: assets/pngs/uiuc_ischool.png
description: The purpose of this assignment is to create a 'Viz for the Public' with a 'data journalism' type article.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# IS 445 Final Project (Fall 2023)
Group 5: Xinzhe Miao (xinzhem2), Wenjin Duan (wenjind2), Yuxi Tian (yuxit2)
<br>

### Dataset Information: 
* Dataset Name: **Electric Vehicle Population Data**
* Data Provided by: Washington State Department of Licensing
* Dataset Description: This dataset shows the Battery Electric Vehicles (BEVs) and Plug-in Hybrid Electric Vehicles (PHEVs) that are currently registered through Washington State Department of Licensing (DOL).
* Dataset Official Website: https://data.wa.gov/Transportation/Electric-Vehicle-Population-Data/f6w7-q2d2
* license: https://opendatacommons.org/licenses/odbl/1-0/

The Open Database License (ODbL) is a legal tool that governs the use, sharing, and modification of a database, covering copyright and database rights while excluding rights to individual contents, computer programs, patents, and trademarks. It functions as both a license and a contractual agreement between the licensor and the user.

Within this license, it includes several right and restriction that the users should obeied or has. The Open Database License (ODbL) grants users the right to use, modify, and share a licensed database freely, including for commercial purposes, with conditions such as maintaining copyright and database right notices, and sharing derivatives under the same or a compatible license (Share Alike). The license permits voluntary, waivable, and non-waivable compulsory license schemes differently and reserves the licensor's right to potentially release the database under different terms or stop distribution.

* Dataset Size: 154K Rows with 20 Columns.
* File Size: 38.7MB (Accepted by GitHub Limit)


| Column Name                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Type       |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| VIN (1-10)                                  | The 1st 10 characters of each vehicle's Vehicle Identification Number (VIN).                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Plain Text |
| County                                      | This is the geographic region of a state that a vehicle's owner is listed to reside within. Vehicles registered in Washington state may be located in other states.                                                                                                                                                                                                                                                                                                                                                                                 | Plain Text |
| City                                        | The city in which the registered owner resides.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Plain Text |
| State                                       | This is the geographic region of the country associated with the record. These addresses may be located in other states.                                                                                                                                                                                                                                                                                                                                                                                                                            | Plain Text |
| Postal Code                                 | The 5 digit zip code in which the registered owner resides.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Plain Text |
| Model Year                                  | The model year of the vehicle, determined by decoding the Vehicle Identification Number (VIN).                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Plain Text |
| Make                                        | The manufacturer of the vehicle, determined by decoding the Vehicle Identification Number (VIN).                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Plain Text |
| Model                                       | The model of the vehicle, determined by decoding the Vehicle Identification Number (VIN).                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Plain Text |
| Electric Vehicle Type                       | This distinguishes the vehicle as all electric or a plug-in hybrid.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Plain Text |
| Clean Alternative Fuel Vehicle (CAFV) Eligibility | This categorizes vehicle as Clean Alternative Fuel Vehicles (CAFVs) based on the fuel requirement and electric-only range requirement in House Bill 2042 as passed in the 2019 legislative session.                                                                                                                                                                                                                                                                                                                                              | Plain Text |
| Electric Range                              | Describes how far a vehicle can travel purely on its electric charge.                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Number     |
| Base MSRP                                   | This is the lowest Manufacturer's Suggested Retail Price (MSRP) for any trim level of the model in question.                                                                                                                                                                                                                                                                                                                                                                                                                                       | Number     |
| Legislative District                        | The specific section of Washington State that the vehicle's owner resides in, as represented in the state legislature.                                                                                                                                                                                                                                                                                                                                                                                                                             | Plain Text |
| DOL Vehicle ID                              | Unique number assigned to each vehicle by Department of Licensing for identification purposes.                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Plain Text |
| Vehicle Location                            | The center of the ZIP Code for the registered vehicle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Point      |
| Electric Utility                            | This is the electric power retail service territories serving the address of the registered vehicle. All ownership types for areas in Washington are included: federal, investor owned, municipal, political subdivision, and cooperative. If the address for the registered vehicle falls into an area with overlapping electric power retail service territories then a single pipe \| delimits utilities of same TYPE and a double pipe \|\| delimits utilities of different types. Blanks occur for vehicles with addresses outside of Washington or for addresses falling into areas in Washington not containing a mapped electric power retail service territory in the source data. | Plain Text |
| 2020 Census Tract                           | The census tract identifier is a combination of the state, county, and census tract codes as assigned by the United States Census Bureau in the 2020 census, also known as Geographic Identifier (GEOID). More information can be found here: [Census Glossary](https://www.census.gov/programs-surveys/geography/about/glossary.html#par_textimage_13) and [Geographic Identifiers](https://www.census.gov/programs-surveys/geography/guidance/geo-identifiers.html)                                                                                                                                   | Plain Text |
| Counties                            | No Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Plain Text      |
| Congressional Districts                            | No Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Plain Text      |
| WAOFM - GIS - Legislative District Boundary                          | No Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |Plain Text     |

<br>
<br>



### Description Plot

**Plot 1: Total Electric Vehicle Sales by Model Year**
<img src="{{site.baseurl }}/assets/pngs/plot1.png" alt="Total Electric Vehicle Sales by Model Year" style="width: 100%">

* The bar plot illustrates the total electric vehicle sales by model year. It shows a clear trend of increasing sales over the years, with particular spikes in certain years, which likely correspond to the introduction of popular models or increased adoption due to other factors like improvements in infrastructure, technology, or government incentives.

<br>

**Plot 2: Top Electric Vehicle Models by Year**
<img src="{{ site.baseurl }}/assets/pngs/plot2.png" alt="Total Electric Vehicle Sales by Model Year" style="width: 100%">

* Here is the line plot showing the count of the top electric vehicle models by model year. Each line represents one of the top models, and the trend in their counts over the years is visible. You can see how some models have gained popularity over time, especially recent models like the Tesla Model 3 and Model Y.

<br>

**Plot 3: Average Electric Range for different car 'Make' with corresponding 'Models'**
<img src="{{ site.baseurl }}/assets/pngs/plot3.png" alt="Total Electric Vehicle Sales by Model Year" style="width: 100%">

* The horizontal bar plots display the average electric range for each model within the top makes. Each subplot corresponds to one of the top makes, and the models are sorted by their average electric range. This visualization helps in comparing the electric range within the lineup of each make.

<br>

**Plot 4: Number of Models for each 'Make'**
<img src="{{ site.baseurl }}/assets/pngs/plot4.png" alt="Total Electric Vehicle Sales by Model Year" style="width: 100%">

* The bar plot shows the number of models available for each make. Makes with a wider range of models are on the left, indicating a larger portfolio of electric vehicles, while those with fewer models are on the right. This visualization provides an insight into the diversity of electric vehicles offered by different manufacturers.​

<br>

**Plot 5: Top Model Location in 2023 and later**
<img src="{{ site.baseurl }}/assets/pngs/plot5.png" alt="Total Electric Vehicle Sales by Model Year" style="width: 100%">

* Data Filtering: The dataset is filtered to include only records where the 'State' is 'WA' (Washington) and the 'Model Year' is 2023 or later. This step ensures that the analysis focuses on recent EV registrations in Washington.
* Identifying the Top Model: Among these filtered records, the code identifies the most popular EV model based on the number of registrations. The value_counts() method is used to count occurrences of each model, and the top one is selected.
* The resulting map should show the locations of the top EV model in Washington state as of 2023, overlaid on a basemap for better geographic context. This analysis is useful for understanding the popularity and distribution of this EV model in Washington.

<br>
<br>
<br>

### Interactive Plot:

<vegachart schema-url="{{ site.baseurl }}/assets/json/final1.json" style="width: 100%"></vegachart>

This interactive plot helps users explore and compare the popularity of different car makes over time and provides insight into the diversity of models available for each make. It's a valuable tool for anyone interested in understanding trends and variations in car sales data from 2010 onwards for the top 10 car manufacturers in this dataset.

* **Line Plot:** The main plot on the left-hand side of the dashboard is a line plot titled "Number of Vehicles by Top 10 Makes and Model Year." It shows the trend in the number of vehicles for the selected car make over the years from 2010 onwards. Each line represents a different car make, and the color of the line corresponds to the selected make.

* **Bar Plot:** The right-hand side of the dashboard displays a bar plot titled "Number of Model(s) for [Selected Make]." It shows the number of models available for the selected car make, providing a more detailed view of the variety within that make.

* **Dynamic Bar Chart Update:** Upon selecting a range of years in the line plot, the bar chart on the right automatically updates to show data relevant to that selection. It displays the number of different models for the selected car make within the chosen year range.

<br>
<br>

### Contextual Datasets

The **"Electric_Vehicle_Title_and_Registration_Activity.csv"** dataset shows records of title activity (transactions recording changes of ownership), and registration activity (transactions authorizing vehicles to be used on Washington public roads). Here is the official link: https://data.wa.gov/Transportation/Electric-Vehicle-Title-and-Registration-Activity/rpr4-cgyd

It provides detailed information about title and registration activities for electric vehicles, including:

* **Clean Alternative Fuel Vehicle Type:** Type of electric vehicle (e.g., Battery Electric Vehicle (BEV)).
* **VIN (Vehicle Identification Number):** Partial VIN numbers for individual vehicles.
* **DOL Vehicle ID, Model Year, Make, Model:** Identifying and descriptive details of the vehicle.
* **Vehicle Primary Use:** The primary use of the vehicle (e.g., Passenger).
* **Specifications:** Electric Range, Odometer Reading.
* **Odometer Code:** Type of odometer reading (e.g., Actual Mileage).
* **Registration and Title Details:** Including transaction type, transaction date, and transaction price.
* **Legislative and Utility Information:** Legislative District, Electric Utility.


This dataset **"Electric_Vehicle_Title_and_Registration_Activity.csv"**, as one contexual dataset, complements the "Electric_Vehicle_Population_Data.csv" by providing more dynamic information such as odometer readings, transaction types, and dates, which reflect the usage and transaction history of electric vehicles. Given the content of both datasets, here are some ways the second dataset (Electric Vehicle Title and Registration Activity) can support the first one (Electric Vehicle Population Data):

* **Vehicle Usage Insights:** Odometer readings from the title and registration dataset can give insights into how much electric vehicles are being used, which can be correlated with the population data to analyze usage patterns.

* **Transaction Trends:** Understanding the transaction types and dates can help in analyzing the market dynamics, like how often electric vehicles are bought and sold, and how this trend correlates with the overall population of electric vehicles.

* **Geographic Analysis:** Both datasets include geographic information which can be used to analyze regional differences in electric vehicle adoption and usage.

* **Model and Make Analysis:** By comparing the models and makes in both datasets, one can analyze the popularity and longevity of different electric vehicle models.

* **Policy Impact Analysis:** By correlating legislative district and utility information with vehicle types and usage, one can assess the impact of local policies on electric vehicle adoption.

* **Environmental Impact Assessment:** The usage data (like odometer readings) combined with population data can help in estimating the environmental impact and benefits of electric vehicles in different regions.




<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

