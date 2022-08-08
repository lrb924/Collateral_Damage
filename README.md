![War Image](Resources/War_Image.jpeg)
![Housing Prices](Resources/housing_prices.jpeg)
![Unemployment](Resources/unemployment.jpeg)

# Collateral Damage: The Effect of War on Stocks, Housing, and Unemployment

## **Project Overview**

  ### *Package Requirements and Versions*

`pip install x` ; where 'x' is the package listed below:
* `python == 3.7.13+` 
* `numpy == 1.21.5`
* `pandas == 1.3.5+`
* `hvplot == 0.7.3`
* `matplotlib == 3.5.1`
* `json == 2.0.9`
* `quandl == 3.7.0`
* `yfinance == 0.1.74`
* `plotly.express == 5.9.0`
  
###
  Our team decided to investigate the effect of an existing war and how that is reflected on stock prices for weapon manufacturers and stock prices for gas companies and how those can effect the cost of crude oil, housing prices and the unemployment rate. Our time references for wars are the Gulf War, the Iraq War, and the Ukrainian/Russian conflict.

The business question we hope to answer is *if we can predict an increase or decline in stock prices for weapon manufacturers and gas companies when there is an existing war. Additionally, we hope to be able to answer if we can predict a rise or decline in crude oil prices, housing prices, and the unemployment rate when there is an existing war.*

Our motivation for taking on this challenge is to find out if there is clear causation or merely a correlation between the effect of war on stock prices as well as crude oil prices, housing prices and unemployment rates.

We hope to find this data using stock data from Nasdaq and Alpaca, the cost of crude oil from eia.gov, the cost of housing prices from Data.gov, and the effect on unemployment rates from the US Department of Labor.

___

## Data pre-processing/gathering steps (cleaning and manipulation)
Our team has accessed stock data and crude oil prices from Nasdaq, Yahoo Finance and Alpaca.

To gather weapons manufacturer data, we used Yahoo Finance. We knew the tickers that we wanted, LMT, BA, RTX, NOC. Then we created a dataframe by narrowing the dates first for the Gulf War then for the Ukrainian War. We did the same for major oil company stocks, with their tickers being XOM, BP, COP and CVX. Then we did line plots for each.

To gather the unemployment data we used Nasdaq/Quandl. Data was converted to json with dates specified for both wars. We set the date as the index and plotted that.

Housing data was the most complex and needed the most manipulation because the data available from Zillow through Nasdaq was broken into regions. We had to identify which regions corresponded with which zip codes. Then we matched each zip code to a specific state. A random sample of 30 prices for each state was picked and then grouped together to find the national average also for date ranges pertaining to the wars in question. This was plotted as line graphs and bar graphs using hvplot.


## Visuals and explanations

![Gulf War Gas](Resources/gas_gulf.png)
Closing stock prices for gas companies before and during the Gulf War<br>
<br>

![Iraq War Gas](Resources/gas_iraq.png)
Closing Stock Prices for Gas Companies During the War in Iraq<br>
<br>

![Ukrainian War Gas](Resources/gas_rusua.png)
Closing Stock Prices of Gas Companies Before and During the Russian Invasion of Ukraine<br>
<br>

![Gulf War Housing](Resources/housing_gulf.png)
Quarterly Housing Prices Index Before and During the Gulf War<br>
<br>

![Iraq War Housing](Resources/housing_iraq.png)
Quarterly Housing Prices Index During the War in Iraq<br>
<br>

![Ukrainian War Housing](Resources/housing_rusua.png)
National Average and National Median of Housing Prices Before and During the Russian Invasion of Ukraine<br>
<br>

![Gulf War Interest Rates](Resources/interestrates_gulf.png)
Interes Rates Before and During the Gulf War<br>
<br>

![Iraq war Interest Rates](Resources/interestrates_iraq.png)
Interest Rates During the War in Iraq<br>
<br>

![Ukrainian War Interest Rates](Resources/interestrates_rusua.png)
Interest Rates Before and During the Russian Invasion of Ukraine<br>
<br>

![Gulf War Oil](Resources/oil_gulf.png)
US Oil Prices Before and During the Gulf War<br>
<br>

![Iraq War Oil](Resources/oil_iraq.png)
US Oil Prices During War in Iraq<br>
<br>

![Ukrainian War Oil](Resources/oil_rusua.png)
US Oil Prices Before and During the Russian Invasion of Ukraine<br>
<br>

![Unemployment during Gulf War](Resources/unemployment_gulf.png)
Unemployment Rate During the Gulf War<br>
<br>

![Unemployment during Iraq War](Resources/unemployment_iraq.png)
Unemployment Rate During the War in Iraq<br>
<br>

![Unemployment during Ukrainian War](Resources/unemployment_rusua.png)
Unemployment Rate During the Russian Invasion of Ukraine<br>
<br>

![Weapons Prices during Gulf War](Resources/weapons_gulf.png)
Closing Stock Prices for Weapons Manufacturers Before and During the Gulf War<br>
<br>

![Weapons Prices during Iraq War](Resources/weapons_iraq.png)
Closing Stock Prices for Weapons Manufacturers During the War in Iraq<br>
<br>

![Weapons Prices during Ukrainian War](Resources/weapons_rusua.png)
Closing Stock Prices for Weapons Manufacturers Before and During the Russian Invasion of Ukraine<br>
<br>

## Additional explanations
## Major findings
  Our primary finding is that war and gas prices may not correlate as simply as most Americans are lead to believe. Shortly after Russia invaded Ukraine in February of 2022, prices at the pump began a rise to all-time highs; soaring past $7 in some places and nearing $10 in others. Americans were told that these skyrockecting gas prices were due to the sanctions President Biden imposed on Russia, Europe's largest oil distributor, and that these sanctions were the direct result of Russia's actions in Ukraine. This narrative lead us to investigate the historical effect of war on gas prices, to see if the current bump in prices should be expected based on what has happpened in the past.

  To begin our investigation, we took a look at the stock prices for some major weapons & gas companies, and compared them to the price of oil during times of war. The weapons companies we gathered info for are Lockheed Martin Corp., Boeing, Raytheon, & Northrop Gruman. The gas companies are Exxon Mobil, BP, ConocoPhillips, & Chevron Corporation. The wars needed to be recent enough for us to find the relevant data, which led us to the Gulf War, and War in Iraq to compare alongside the War in Ukraine. Using this data our group hoped to find trends that suggest changes in the prices of these companies as a direct consequence of an existing war.

  Through this first part of our investigation, we found little data that clearly indicates the correlation between stock prices of our chosen companies, and ongoing war.  The first indication that war might affect a company's stock price is a sizable spike in Boeing's price near the start of the Gulf war. However, in taking a deeper look into the price hike, we found out that it was due to the excitement over Boeing's announcement of a new commercial aircraft, the 777. The next indication is the rise of weapons stocks during the beginning of the war in Iraq. These prices see a steady increase, right up until the 2008 recession, where they crash and fail to return to their pre-recession levels. The weapons prices during the the War in Ukraine show that two of our companies' prices are increasing while the other two decrease as the war progresses.
  
   Generally we can see that the stock prices move during times of war, but this doesn't make it clear that the prices moved because of the war. It's also worth noting that the companies we chose are regarded as the top 4 companies in their domains, and are the most likely to be affected by a change in their respective markets.

  Next, we took a look at the Dollar Per Barrel price of oil and how it changed during each war. Looking at this data, we can see clearly that oil prices generally tend to rise during times of war. For both the Gulf War and the War in Ukraine, we see noticible spikes in oil prices at the start of each conflict indicating that the news of war might directly impact oil prices in the short term. For the war in Iraq, we actually see a small dip in oil prices at the start, but we see the same trend of prices increasing accross the duration of the conflict. With this data, it's reasonable to assume that war does have an effect on oil prices, although it isn't clear how, or even how much it affects prices when compared to other variables.

  After analyzing our initial dataset, we discussed the other vairables that we should consider, and decided that inflation should be the key indicator that we analyze alongside what we've gathered. Our data shows spikes in inflation that occur at the same time as the spikes we see in gas prices during the Gulf War and War in Ukraine. For the Gulf war we get a graph very similar to the graph of oil prices during that time, suggesting that they are closely correlated. The same can be said for the graphs of inflation and oil prices during the War in Ukraine. Both show spikes near the beginning of the invasion and as inflation continues to rise, so does the cost of oil.

After analzing stock and oil prices, we decided to direct our attention towards the US housing and umeployment rates during our selected wars. Taking a look first at the War in Ukraine, we can see that housing prices have been on a steady incline since the beginning of the war. Given this we can expect the unmployment rate to be on a steady decline, which is exactly what we see when taking a look at the plot of the data. The same pattern plays out for the housing and unemployment data during the War in Iraq. The data suggest that the two markets directly correlate to one another and are inversely related. 

Our most interesting find comes when observing this same dataset for the Gulf War. According to our data, unemployment went up during this time, cand housing prices went down. While the markets did move properly according to their relationship, this data represents an anomaly because we would expect them to move in the opposite directions, as they did during the other wars that we investigated. 

We suspected the main culprit for our anomaly to be changing interest rates, so we took a look at them for each war. For both the War in Ukraine and the War in Iraq, we see interest rates spike during the early part of each timeline. They eventually dropped towards the end of the war in Iraq, so we might see something similar near the end of the War in Ukraine. For now we can see that interest rates continue to increase as that conflict ensues.

The interest rates during the Gulf War have a different trajectory. At the Start of the war, they were higher that they ever got during the War in Iraq, and higher than the rates that we currently see with War in Ukraine. This is likely due to the rates recovering from the all-time highs that occured during the early 1980s. Because the rates were already so high, we don't see the same spike that occurs during the other wars, and instead we see them stay relatively steady until they begin to fall as the war nears it's end. 
 


## Challenges, Limitations and future development

The initial challenge was pulling out housing data as the main sources that gather data are not very generous with it. Most of this data is pulled by the National Association of Realtors, which is the main custodian of the Multiple Listing Service. This data is then pulled by other real estate companies such as Zillow, Redfin or Realtor.com. But they also are not generous with their data either. Thankfully, Nasdaq gathers housing data through Zillow, and not just its stock price, and provides that gratuitously through their API. But because it is broken into small regions, it all needed to be cleaned and combined to provide the national average and median average.

After gathering and plotting all of the data, the limitations of this project are that there are multiple factors that could be influencing each other at various times. It is not always easy to isolate each factor and say for certain without a shadow of a doubt that one factor necessarily influenced another. For instance, we initially set out to explore how war may affect weapon manufacturers. Generally it would seem as though their stock prices went up before the war but then not much during war. Perhaps this is an instance of people "buying the rumor and selling the news." The only one that had sharp fluctuation was Boeing, which may have been due to the release of a new product that was not even closely related to the war. Point is, one would have to look at the news for each company every day for that period to see if there are other factors affecting their prices. The same could be said about housing data. It seems like there is more correlation with inflation than with war. More recently there was a pandemic that affected demand in houses due to people working from home and people having more money for a downpayment from stimulus checks. These were all factors not affected by conflict. With the time constraints for this project it would be hard to have a bird's eye view of all the factors affecting each other.

Limitations are clear pointers to future development. The relationship between all these factors is something that we could look at in the future. Now, if we are able to predict some of the future based on our current analysis, we could say that perhaps that some of the results from the Ukrainian War will not be so different from the results of the Gulf War. For instances, though oil prices increased at the beginning of each conflict, it is clear that in the Gulf War it eventually plateued and then it went down. There may be a repeat of that in the current conflict. This is because countries, organizations and people make adjustments to price fluctuations. For instance OPEC said they would increase oil production in response to the war. People are starting to buy more electric cars, etc. 




## Conclusion

## References

- Nasdaq/Quandl<br>
- Alpaca<br>
- Yahoo Finance<br>
- https://fred.stlouisfed.org/series/QUSR628BIS<br>
used for xls data that goes together with Nasdaq and Zillow housing data.<br>
- https://gist.github.com/dikaio/0ce2a7e9f7088918f8c6ff24436fd035<br>
used for gathering coordinates of 50 states.

## Team Members:

  - Darius Griffin (Project Manager)<br>
  - Bryan Follenweider<br>
  - Lara Barger<br>
  - Miguel Ramos<br>
  - Yohan Hwang
