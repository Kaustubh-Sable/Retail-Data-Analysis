For the purpose exploratory data analysis, we first cleaned the data and tried different visualizations with the same. We analysed the data for the corner cases and normalized it for other analysis tasks as well. Datetime related cleaning for the attribute "Transaction Time" was done as well.

Following observations were made whlie doing exploratory analysis:
* We have plot the distribution of sales transactions based
on hourly status:

![Hourly Shopping Analysis](https://github.com/Kaustubh-Sable/Retail-Data-Analysis/blob/master/EDA/Images/Hourly_Shopping.jpg)

From the plot, we can see that the people tend to buy more during the time span of 9 am to 5 pm . This type of data can also help in promotion of specific products based on the hourly trends of customers.

* Next, we plot the distribution of number of items purchased in a single basket. The frequency (i.e. the count) decreases as the number of items in a basket increase. Hence, we plot a separate graph for illustrating the higher number of purchased items in a basket. From the figure 2, we can deduce that customers tend to buy fewer items more often while rarely they purchase higher number of items (i.e. they probably stock the items).

![Hourly Shopping Analysis](https://github.com/Kaustubh-Sable/Retail-Data-Analysis/blob/master/EDA/Images/Items_Frequency.jpg)

Some other interesting facts we found about data:
* Costello’s Ace Hardware, even though being a hardware retail store, the store not only consists of the hardware items but also cookwares and food items like ’BIRD BLEND SUET’ and ’Diamond Naturals Lamb and Rice Dog Food’. The same was observed while browsing through the dataset.
* For the rows where Loyalty ID is not null, the Zip Code represents the area code of the customer who is making the purchase. While in case if Loyalty ID is null, Zip Code will represent the area code of the store.
* Store # and Store Name both uniquely represent the store. Similarly, Item Number and Item Description both uniquely define the items in the stores. Hence, for the computational purposes, we will stick to Store # and Item Number while for display purposes, we will use Store Name and Item Description wherever possible.
* An item may have different pricing across different stores. For some items across the stores, it may have different gross margin and different gross percentage. 
* $ Off-retail and (Actual - Retail) shows same results. We can say that they are redundant.
* Records for item CMN donations shows the amount donated by the customer. So, there is no retail price for such records. Every time according to column values it calculates all margin and margin %. Another thing to be noted, pricing source is always manual overridden for CMN donation records.
