---
name: IS445 Final Project Jekyll Webpage (Fall 2023)
tools: [Python, HTML, vega-lite]
image: assets/pngs/hw8.png
description: The purpose of this assignment is to create a 'Viz for the Public' with a 'data journalism' type article.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

Here is the url for the dataset that used in this HW#8:

* https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv


# Chart I:

**Plot 1. Histogram: Number of Buildings for Each Agency**

* The bar chart titled "Number of Buildings Acquired Each Agency" provides a visual representation of the number of buildings associated with different agencies. Each bar corresponds to a specific agency, with the agency's name labeled on the x-axis. The height of each bar indicates the number of buildings that the agency possesses, as detailed on the y-axis.

**Plot 2. LinePlot: Number of Buildings for Each Agency**

* The plot is named "Number of Buildings for Each Year". Using a line chart, the x-axis represents the years (termed "Year Constructed") in which buildings were constructed, and the y-axis quantifies the number of buildings constructed in each of those years. It represents the volume of buildings constructed for a given year.

**Selection Mechanism:**

* The plot uses an interactive brush selection named brush, which allows you to select a range of data in the plot by clicking and dragging across the plot area. This selection is defined to work across both the 'x' and 'y' encodings.

* The two charts are displayed side by side (indicated by the | operator in chart1 | chart2).
Interactivity is established between the two charts via the brush selection. When you select a range of agencies in chart1 (the bar chart), chart2 (the line chart) will update to show only the data for the selected agencies and their corresponding 'Year Constructed'.

* Overall, this interactive visualization allows you to filter the view of the data in one chart based on selections made in the other, providing a linked view that helps to explore and understand the relationships between the agency and the years the buildings were constructed.

<vegachart schema-url="{{ site.baseurl }}/assets/json/final1.json" style="width: 100%"></vegachart>

# Chart II:

**Chart 3: Bar Chart of Number of Buildings by Agency**

Visualization Description: 
* This bar chart visualizes the number of buildings associated with each agency. The agencies are listed on the x-axis, and the number of buildings is represented by the height of the bars on the y-axis. This gives a quick visual comparison of how many buildings are managed by each agency.

Encoding Types:
* The x-axis uses an ordinal encoding for 'Agency Name', arranging the agencies in a nominal fashion.
* The y-axis is quantitative, representing a count of buildings per agency.

Color Scheme:
* No specific color encoding 

Data Transformations:
* The data has been pre-filtered (building_filtered) to possibly exclude certain conditions or focus on specific agencies before being visualized.

Interactivity:
* Dropdown: Allows the viewer to filter the data displayed by selecting an agency from a dropdown list, focusing on data of interest without distractions from other agencies.
* Brush: Enables the user to select a range on the chart (although how this works on an ordinal x-axis might be limited).

**Chart 4: Line Chart of Buildings by Year Constructed**

Visualization Description: 
* This line chart provides a temporal view of the number of buildings constructed over the years. Each point on the x-axis represents a year, and the y-axis shows how many buildings were constructed in that year.

Encoding Types:
* The x-axis is temporal, showing 'Year Constructed', which allows for a chronological representation of data.
* The y-axis is quantitative, counting the number of buildings.

Color Scheme:
* Similar to Chart 3, no specific color encoding is mentioned. 

Data Transformations:
* Similar to Chart 3, any transformations would have occurred in the building_filtered data preparation.

Interactivity:
* Brush: When used in this chart, the brush selection allows for a more dynamic investigation of building construction over specific time periods.
* Dropdown: This interacts with the selection from Chart 3, allowing the user to see the temporal distribution of buildings for the selected agency.

**Combined Chart:**
Interactions in one chart will affect the other. Specifically:
* Selecting an agency from the dropdown will filter both charts to only show data for that agency.
* Using the brush tool in either chart will filter the other chart to show data for the selected range. However, since the brush is defined with both 'x' and 'y' encodings, its effect will depend on how it is used in the context of these particular charts.

<vegachart schema-url="{{ site.baseurl }}/assets/json/hw8_chart2.json" style="width: 100%"></vegachart>


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

