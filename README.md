# group_6_project

## World Carbon Emissions Analysis

Carbon emissions refer to the release of carbon dioxide and other greenhouse gases into the atmosphere. These emissions are primarily caused by the burning of fossil fuels, such as coal, oil, and natural gas, in power plants, transportation, and industrial processes. Additionally, deforestation and other land-use changes can also contribute to carbon emissions.
One of the most significant effects is the contribution to climate change, which causes global temperatures to rise and leads to extreme weather events such as heat waves, droughts, floods and fires.

Carbon emissions also contribute to air pollution which can have serious impacts on human health, including respiratory issues and heart disease. Carbon emissions also cause acid rain, which can harm crops and wildlife. Finally, the ocean absorbs large amounts of carbon dioxide, which makes the water more acidic and harms marine life and coral formation. 

Overall, carbon emissions are having a major negative impact on the planet and all living things, and it is important to take action to reduce these emissions.

###  Project Description/Outline: 
Evaluate world carbon and energy consumption based on following:

### Questions to Answer:
* Country with Highest/Lowest Emissions
* Highest Energy Consumption and Production
* Which fuel type is being consumed by which country?
* Review correlation between Consumption of Energy vs. CO2 Emissions?
* GeoViews graph of Carbon Emissions and Energy Consumption
* How can we predict future optimal Carbon Emissions reduction by country?

### Datasets Used:

1. World CO2 Emissions: https://www.kaggle.com/datasets/thedevastator/global-fossil-co2-emissions-by-country-2002-2022
>* Source Reference: https://zenodo.org/record/7215364#.Y8mipOzMJro
2. World Fuel Production and Consumption: https://www.kaggle.com/datasets/shawkatsujon/worldwide-fuel-production-and-consumption
3. World Lat & Long Mapping: https://gist.github.com/tadast/8827699
4. Country to Continent Mapping: https://www.kaggle.com/datasets/andradaolteanu/country-mapping-iso-continent-region

### Libraries
* pandas
* numpy
* hvplot
* hv.extensions
* pathlib
* panel
* plotly
* holoviews
* bokeh
* warnings

## Carbon Emissions - Data Exploration

Based on the analyis there is data missing from the Carbon Emissions dataset. Columns 'Coal', 'Oil', 'Gas', 'Cement', 'Flaring' seems to have datapoints unavailable. The 'Other' column has over 61K unknown datapoints. 'Other' is defined as: Carbon Emissions from other forms of industrial processes. (Source: https://www.kaggle.com/datasets/thedevastator/global-fossil-co2-emissions-by-country-2002-2022).

### Global Emissions

![Global Carbon Emissions by Yr (2002-2022)](https://github.com/mananwala/group_6_project/blob/main/Images/Global%20Carbon%20Emissions%20by%20Yr%20(2002-2022).png)


#### Insight for Global Carbon Emissions

Looking at the Global Carbon Emissions data from the dataset including Coal, Oil, Gas, Cement, Flaring, Other Sources, the following insights are observed:
* Fuel source Coal has the highest Carbon Emissions globally. Oil and Gas also emit high levels of carbon while Cement, Flaring and Other make up the least source of Carbon Emissions
* Coal Emission ramped up significantly starting in 2009 while Oil increased slightly only
* All Coal, Oil, Gas Carbon Emissions dropped suddenly in 2020 due to the Pandemic

### Country Carbon Emissions

#### Global Carbon Emissions by Continent

![Global Carbon Emissions by Yr (2002-2022)](https://github.com/mananwala/group_6_project/blob/main/Images/Continent%20Carbon%20Emissions%20by%20Yr%20(2002-2022).png)

Based on above figure, 
* Coal is the main source of Carbon Emissions in Asia followed Oil, Cement and Gas.
* Americas alos have relatively large Carbon Emissions from Coal, Oil and Gas. 
* Eurpoe is using primarily Gas but small amounts of Oil and Coal.

#### Global Carbon Emissions by Continent by Country

![Africa Carbon Emissions by Yr by Country(2002-2022)](https://github.com/mananwala/group_6_project/blob/main/Images/1-Africa%20Carbon%20Emissions.png)

![Americas Carbon Emissions by Yr by Country(2002-2022)](https://github.com/mananwala/group_6_project/blob/main/Images/2-Americas%20Carbon%20Emissions.png)

![Asia Carbon Emissions by Yr by Country(2002-2022)](https://github.com/mananwala/group_6_project/blob/main/Images/3-Asia%20Carbon%20Emissions.png)

![Europe Carbon Emissions by Yr by Country(2002-2022)](https://github.com/mananwala/group_6_project/blob/main/Images/4-Europe%20Carbon%20Emissions.png)

![Oceania Carbon Emissions by Yr by Country(2002-2022)](https://github.com/mananwala/group_6_project/blob/main/Images/5-Oceania.png)

#### Insight

Countries emitting the highest Carbon Emissions by each Continent are:

* Africa: Algeria, Egypt, Nigeria, SOUTH AFRICA* 
* Americas: USA* 
* Asia: CHINA*, India, Japan, Iran, Indonesia, South Korea, Saudi Arabia
* Europe: Belgium, Czech, France, Germany, Italy, Netherlands, Poland, Romania, RUSSIA*, Spain, Ukraine, United Kingdom
* Oceania: AUSTRALIA*, New Zealand

Countries SOUTH AFRICA, USA, CHINA, RUSSIA, AUSTRALIA have the highest Carbon Emissions.

Countries with lowest Carbon Emissions by each Continent are:

* Africa: Angola, Libya, Morocco, Tunisia are emitting carbon but not as much as the high emitters.  Remainder of the countries in Africa are emitting marginal Carbon Emissions.
* Americas: Canada and Mexico are emitting carbon and remainder of the countries in Americas have low Carbon Emissions
* Asia: Most of the countries have small amounts of Carbon Emissions compared to the ones identified in high Emissions category.
* Europe: Majority of the countries in Europe have some degree of Carbon Emissions compared to other continents but the high polluters stand out.
* Oceania: Almost all the land masses have marginal Carbon Emissions except for the two countries with highest Carbon Emissions.

### GeoViews of Country Carbon Emissions

![Country Emissions from 2002-2022](https://github.com/mananwala/group_6_project/blob/main/Images/Country%20Emissions%20from%202002-2022.png)
#### Insight

USA and China stand out of the crowd with highest Carbon Emissions

## World Fuel Production

![Global Gas Production (m³) by Yr (1980-2019)](https://github.com/mananwala/group_6_project/blob/main/Images/Global%20Gas%20Production%20(m%C2%B3)%20by%20Yr%20(1980-2019).png)

![Global Coal Production (Ton) by Yr (1980-2019)](https://github.com/mananwala/group_6_project/blob/main/Images/Global%20Coal%20Production%20(Ton)%20by%20Yr%20(1980-2019).png)

![Global Oil Production (m³) by Yr (1980-2019)](https://github.com/mananwala/group_6_project/blob/main/Images/Global%20Oil%20Production%20(m%C2%B3)%20by%20Yr%20(1980-2019).png)

#### Insight

Global production of Coal, Oil and Gas have increased from 1980s to 2019.  There is a notable decrease in Coal Production in 2016 but it is hard to identify why this change occurred from these graphs. 

Also, reviewing the data for Fuel Production by Country, following countries have the highest Production by Fuel type:

* Gas:  Russia and USA
* Coal: China and USA
* Oil: USA, Russia, Saudi Arabia

Please see jupyter notebook for more details:

[Carbon_Emissions_DataExploration.ipynb](https://github.com/KSohi-max/Carbon_Emissions/blob/main/Carbon_Emissions_DataExploration.ipynb)

## World Fuel Consumption

![Coal Consumption (Ton) by Yr by Country (1980-2019)](https://github.com/KSohi-max/Carbon_Emissions/blob/main/Images/Coal%20Consumption%20(Ton)%20by%20Yr%20by%20Country%20(1980-2019).png)

![Gas Consumption (m³) by Yr by Country (1980-2019)](https://github.com/KSohi-max/Carbon_Emissions/blob/main/Images/Gas%20Consumption%20(m%C2%B3)%20by%20Yr%20by%20Country%20(1980-2019).png)

![Oil Consumption (m³) by Yr by Country (1980-2019)](https://github.com/KSohi-max/Carbon_Emissions/blob/main/Images/Oil%20Consumption%20(m%C2%B3)%20by%20Yr%20by%20Country%20(1980-2019).png)

### Insight

The following are insights from Consumption by Fuel Type:

* Gas Consumption:  USA and Russia have the highest Gas Consumption with China increasing consumption of Gas as of 2010
* Coal Consumption: China has the highest consumption of Coal fuel. India follows next on the list. USA has decreased the consumption of Coal as of 2008 as it has increase use of Gas significantly as of 2009
* Oil Consumption: USA and China have the highest Consumption. India is on the rise for Oil Consumption

### Correlation Heatmap (Emissions v. Production & Consumption)

![Correlation_Heatmap](https://github.com/KSohi-max/Carbon_Emissions/blob/main/Images/Correlation_Heatmap.png)

##### Correlation Insight

There are some strong correlations between Emissions and Energy Production+Consumption:

* Total Carbon Emissions Correlation:
>1. Coal, Oil and Cement contribute signifcantly to Total Carbon Emissions
>2. Both Coal and Oil Consumption is correlated highly with Total Carbon Emissions
>3. Coal Production is also correlated with Total Carbon Emissions

* Coal Carbon Emissions Correlation:
>1. Cement and Oil Carbon Emissions are correlated with Coal Carbon Emissions but this doesn't prove causation
>2. Coal Production and Consumption are directly correlated with Coal Carbon Emissions

* Oil Carbon Emissions Correlation:
>1. Oil Consumption is directly correlated with the Oil Carbon Emissions

* Gas Carbon Emissions Correlation:
>1. Gas production and consumption are directly correlated with Gas Carbon Emissions

* Cement Carbon Emissions Correlation:
>1. Coal production and consumption are highly correlated with Cement Carbon Emissions.  It will require more Cement related data to explore the reason for this correlation and causation remains unfounded.

* Carbon Emissions per Capita
>1. Gas and Oil production and consumption are relatively high in correlation to Carbon Emissions per Capital values.  This may indicate that majority of the population/countries on earth are consuming and hence producing Gas and Oil.

* Population 
>1. Coal, Oil, Cement Carbon Emissions are highly correlated with Population.  Larger populations of country may correspond to more buildings and roads (infrastructure).  Coal and Oil seem to be the Carbon polluters when it comes to Population.
>2. Coal production and consumption are highly correlated with Population.

*  Note that there are very few low correlations in the dataset as expected.

It is difficult to draw any conclusions based on these correlations except where there is a direct correlation indicated, i.e., correlations of 1 or close to 1.  There are no significant surprises except for Cement Carbon Emissions. More cement data is required to draw any conclusions.

## Prediction using Linear Regression

### Libraries

* sklearn

### Linear Regression Results

Coefficients: 
 [ 5.66718967e-09 -7.81410424e-09 -1.37673732e-06  1.08021003e-06
  1.02329647e-06  2.06133816e-06 -2.28143706e-02  4.74800346e-02
  4.80513041e-01  6.05989219e+01 -5.15740290e+00 -4.24446312e+00
  1.66590882e-06]

Intercept: 
 8.890725085823291

Mean Absolute Error : 134.20

Mean Squared Error: 328493.07

Coefficient of Determination: 0.22

### Insight

In using a simple linear regression to generate an equation that would define the relationship between Total Carbon Emissions and Fuel Production and Consumption, it is evident that the model created is not sufficient to define this relationship.

* The Coefficient of determination (R²) measures how well a statistical model predicts an outcome. The outcome is represented by the model's dependent variable. The lowest possible value of R² is 0 and the highest possible value is 1.  For this model, R² is 0.22. This indicates that a linear regression model does not fit the data well. 
* Clearly there are number of future analysis work to pursue:
> 1. Obtain more data rows than the 9,660 rows.  Also, explore other independent variables that may be far more relevant. More datapoints provide more training data to the model and can potentially increase the accuracy.
> 3. Try other models that might better fit the dataset
> 4. Review additional litreature to determine how to model this data better in the future.

If an equation or relationship between Total Carbon Emissions and the independent variables can be found, a minimization analysis can be carried out to determine which variables must be decreased to reduce the Total Carbon Emissions across different countries. It is important to note that this may be a complex model but also a complex political issue to resolve based on the current 'global policies' that seem to be based on "Bigger/Larger/Greater is Better" financial fundamentals.

## Conclusion

Based on above analysis it is clear that wealthy countries with high GDP and economic activities have the highest Carbon Emission, generally high Fuel Production and Consumption.  They may vary the type of fuel to work to reduce Carbon Emissions.  But the bigger question from financial point of view is:  Is it sustainable? 

### Sources for Python Code:

* Kaggle.com for Datasets
* Geek for Geeks: https://www.geeksforgeeks.org/multiple-linear-regression-with-scikit-learn/
* Stack Overflow:  Mapping dictionary to dataframe, removing rows from dataframe, etc.
* SNS Correlation Heatmap:  https://medium.com/@szabo.bibor/how-to-create-a-seaborn-correlation-heatmap-in-python-834c0686b88e
* Investopedia/Wikipedia:  https://en.wikipedia.org/wiki/Coefficient_of_determination
