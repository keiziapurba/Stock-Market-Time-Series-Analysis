# Stock Market Time Series Analysis
#### Analyze big tech company's stock market and their correlation whether are affecting their price and daily returns or not (using data from 2013/4 to 2018).
---

## Table of Content
  * [Analyzing Closing Price of Stocks & Volume Trading](#Analyzing-Closing-Price-of-Stocks-&-Volume-Trading)
  * [Analyzing Daily Returns](#Analyzing-Daily-Returns)
  * [Multivariate Analysis](#Multivariate-Analysis)
  * [Value at Risk Analysis](#Value-at-Risk-Analysis)

---

## **Analyzing Closing Price of Stocks & Volume Trading**

Visualization of big techs companies stock market time to time from 2013/2014 to 2018:

<img width="1012" alt="Screen Shot 2022-03-15 at 13 10 44" src="https://user-images.githubusercontent.com/91368463/158317896-1efd7d31-0adc-4750-8eeb-c7aea767e2eb.png">

Overall, distribution of highest peak stock in each company:
- Apple in 24 January 2014 with total volume: 266.8M
- Google in 17 July 2015 with total volume: 11.2M
- Microsoft in 19 July 2013 with total volume: 248.3M, followed by 23 August 2013 with total volume: 225.4M
- Amazon in 30 January 2015 with total volume: 23.8 M

<img width="605" alt="Screen Shot 2022-03-15 at 20 28 23" src="https://user-images.githubusercontent.com/91368463/158388566-434572e2-4d61-465d-b9ad-a9aa6f54e5fb.png">

In 2017 we can take some points:
- Apple have peak in 1 febuary with total volume: 112M and rest of the time Apple stock average at below 50M.
- Google have peak in 27 october with total volume: 5.2M, followed by 24 July with total volume: 4.7M and the rest is performing average
- In 27 October, Microsoft have a little peak with total volume: 71.1M, but overall the stock is performing average
-  For Amazon, the peak is in 27 October with total volume: 16.6M, in this year, Amazon have some peaks in February, June, July and November aswell


## **Analyzing Daily Returns**
- In this step, I analyze Amazon daily return percentage in 2015.

<img width="1241" alt="Screen Shot 2022-03-15 at 19 17 27" src="https://user-images.githubusercontent.com/91368463/158389356-3bb43742-e1db-4759-8900-ddf7fa04c2ff.png">

- Based on the graph, we can see that Amazon have its peak and crash in August, 2015. Amazon stock at its highest peak in August, 24, 2015 with 8% daily return and crash happened the day after the peak, August 25, 2015 with -7% daily return.
- There might some factors that affecting this, for example because of the government policies or maybe Apple launch new product.

<img width="386" alt="Screen Shot 2022-03-15 at 19 26 29" src="https://user-images.githubusercontent.com/91368463/158389777-82d54e84-620c-490e-9b91-aba2f5197ac8.png">

- We can see that Amazon have downward trends to its monthly mean of close feature, but after 2016 the main price starts increasing rapidly.



## **Multivariate Analysis**
- Amazon and Microsoft plot is very close to linear, which means if the Amazon price is increases or the closing price of Amazon and stocks increases, Microsoft stock closing price will be increases aswell.
- Apple and Google plot dont have good correlation, because it's far from linear. It means that we can't find a very good relationship between closing price od apple and between closing price of google

<img width="709" alt="Screen Shot 2022-03-15 at 19 47 33" src="https://user-images.githubusercontent.com/91368463/158390841-75fef392-687e-4708-a649-9ff797b3c574.png">

Tech companies that have high correlation to each other are:
- Amazon and Microsoft: 96% 
- Google and Microsoft: 91%
- Apple and Microsoft: 90%
- Amazon and Google: 89%
- Amazon and Apple: 82%

Overall, the correlation between each tech companies are high, except correlation between Google and Apple: 64%, it's not necessarily bad but they have low correlation (>0.7: high correlation)

<img width="353" alt="Screen Shot 2022-03-15 at 19 47 55" src="https://user-images.githubusercontent.com/91368463/158391054-59e02350-7bdd-4a84-b431-e61f53cfe51d.png">


## **Value at Risk Analysis**
- In this step, we make new feature called change which is closing price minus opening price then divide it with closing price and convert it to percentage by times it with 100. Change feature is a change in each and every stock every year from 2014 to 2018 (in %).

<img width="634" alt="Screen Shot 2022-03-15 at 20 53 18" src="https://user-images.githubusercontent.com/91368463/158393304-f23f34a2-c4de-46d2-b22a-a4fc6cea960e.png">

Overall the change correlation between each companies are low, but Amazon and Microsoft have the highest correlation: 42%. It means if Amazon have high daily return, there is 42% probability that daily retuen in Microsoft is also high.

<img width="411" alt="Screen Shot 2022-03-15 at 20 57 06" src="https://user-images.githubusercontent.com/91368463/158393813-a9265837-83c3-4b0c-860e-3b21079dfb1e.png">

Then we check one of company distribution. Here I used apple change distribution and it shows that it have normal distribution:

<img width="398" alt="Screen Shot 2022-03-15 at 20 59 02" src="https://user-images.githubusercontent.com/91368463/158394207-44aaf495-392c-46fe-a048-f237eb40a222.png">

- We can check the standarization using std()*3 to check 99.7% entire data, because the distribution is normal. After checking using std()*3 it shows that 99.7% chance that Apple daily return will lay in range between -3.5 and 3.5.
- We can also check using quantile. I used quantile(0.1), which means 90%. The data shows that 90% of the time Apple worst daily lost will not exceed -1.4
- Here are percentage daily return of each company after doing value risk analysis (value in %):

<img width="704" alt="Screen Shot 2022-03-15 at 20 08 34" src="https://user-images.githubusercontent.com/91368463/158395427-985a4fa5-b860-4f5f-aeb4-81183e03ca2d.png">





