# Immigration-Visualization
In the file `immigration_dashboard.pbix`, you can see an interactive dashboard visualizing Norwegian immigration data. If you only want to have a quick look, I have also exported the Power BI file as a PDF to provide a static screenshot of the dashboard. You can see this in `dashboard_screenshot.pdf`.

The data is dynamically retrieved directly from Statistics Norway's API. Because the original JSON format of the response contains a lot of unnecessary data and is inconveniently structured, several transformations are first performed to clean and prepare the data for visualizations.

## Contents of the Dashboard
The dashboard contains the following elements:
* A year filter, allowing you to select the year for which you want to see the immigration data.
* A bar chart of all countries sorted by the number of immigrants in Norway.
* A line chart of the number of the total number of immigrants from 1970 until the current year.
  * If you highlight specific countries, the line chart will be updated to consider only your selection.
* A text area that shows the year's biggest positive and negative changes in immigrants from the previous year.
  * Note that there are no valid values for this before 1987 because values 1971-1979 and 1981-1985 don't exist.
* A map chart with each country color-coded by number of immigrants.
  * Light blue --> Few immigrants.
  * Dark purple --> Many immigrants.
* Two bar charts showing five countries with a significant gender imbalance for each gender.


## Considerations
* I chose a dark turquoise color to represent men and an orange color to represent women. I did not want to choose colors that enforce gender stereotypes, such as blue and pink. I felt that the current colors do not enforce stereotypes, yet have adequate contrast, and my understanding is that it is accessible to people with color blindness.
* I chose the shades of light blue and purple for the map chart. Because immigration is a heavily debated topic, I did not want to pick colors such as red or green, which may suggest that a given amount of immigration is better or worse than another. I therefore chose light blue and purple. However, I admit that I don't know how good of a choice that is with regards to accessibility.
* Titles of charts are in English for the sake of inclusion, but the names of countries and genders are in Norwegian. This is because the data from Statistics Norway's API is in Norwegian. Perhaps it is possible to request English data, but I don't think it's a big problem as most country names are similar in English and Norwegian.
