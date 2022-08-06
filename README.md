![War Image](Resources/War_Image.jpeg)
![Housing Prices](Resources/housing_prices.jpeg)
![Unemployment](Resources/unemployment.jpeg)

# Collateral Damage: The Effect of War on Stocks, Housing, and Unemployment

## **Project Overview**
  ### 
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
## Additional explanations
## Major findings
  
## Challenges, Limitations and future development

The initial challenge was pulling out housing data as the main sources that gather data are not very generous with it. Most of this data is pulled by the National Association of Realtors, which is the main custodian of the Multiple Listing Service. This data is then pulled by other real estate companies such as Zillow, Redfin or Realtor.com. But they also are not generous with their data either. Thankfully, Nasdaq gathers housing data through Zillow, and not just its stock price, and provides that gratuitously through their API. But because it is broken into small regions, it all needed to be cleaned and combined to provide the national average and median average.

After gathering and plotting all of the data, the limitations of this project are that there are multiple factors that could be influencing each other at various times. It is not always easy to isolate each factor and say for certain without a shadow of a doubt that one factor necessarily influenced another. For instance, we initially set out to explore how war may affect weapon manufacturers. Generally it would seem as though their stock prices went up before the war but then not much during war. Perhaps this is an instance of people "buying the rumor and selling the news." The only one that had sharp fluctuation was Boeing, which may have been due to the release of a new product that was not even closely related to the war. Point is, one would have to look at the news for each company every day for that period to see if there are other factors affecting their prices. The same could be said about housing data. It seems like there is more correlation with inflation than with war. More recently there was a pandemic that affected demand in houses due to people working from home and people having more money for a downpayment from stimulus checks. These were all factors not affected by conflict. With the time constraints for this project it would be hard to have a bird's eye view of all the factors affecting each other.

Limitations are clear pointers to future development. The relationship between all these factors is something that we could look at in the future. Now, if we are able to predict some of the future based on our current analysis, we could say that perhaps that some of the results from the Ukrainian War will not be so different from the results of the Gulf War. For instances, though oil prices increased at the beginning of each conflict, it is clear that in the Gulf War it eventually plateued and then it went down. There may be a repeat of that in the current conflict. This is because countries, organizations and people make adjustments to price fluctuations. For instance OPEC said they would increase oil production in response to the war. People are starting to buy more electric cars, etc. 




- Conclusion
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
