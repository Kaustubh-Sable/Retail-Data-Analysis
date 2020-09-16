**Loss leader** is a product offered at cheaper price in expectation of selling other products having higher margin and in turn increase customer base in future. For an instance, giving offers and discounts on some product which is related to other product such that purchasing both products at a time will increase overall profit.

#### Data Preprocessing:
We encountered certain irregularities in the dataset and
resolved them as below:
* Header rows and Date feature were treated the same way as done for MBA.
* Converted ’Gross Margin’ feature to numeric value. 
* Removed the records belonging to items containing Item Description such as ’Coupons’, ’Rewards’, ’INST SAVINGS’, etc.. This is done because these promotional items are not actual items and hence cannot be considered for this analysis.

#### Analysis:
Features used: ’Store Name’, ’Item Description’, ’Gross Margin’. 

##### Description:
For this analysis, we calculated ’Gross Margin’ per store by grouping dataset per store and summing over the margin for each store. Following figure shows the aggregate gross margin of each store:
![Aggregate Gross Margin](https://github.com/Kaustubh-Sable/Retail-Data-Analysis/blob/master/Loss_Leader_Analysis/Images/Aggr_Gross_Margin.png)

From the figure, we can observe that Island Park store has the maximum gross margin among other stores. We also created a plot for only negative gross margin that each store has incurred. This is done by grouping store items of each store that have negative gross margin. From this plot, we observed that Island Park store has second highest negative loss margin among all the stores. Following figure shows the negative loss margin:

![Aggregated Negative Gross Margin](https://github.com/Kaustubh-Sable/Retail-Data-Analysis/blob/master/Loss_Leader_Analysis/Images/Aggr_Neg_Gross_Margin.png)

Hence, it could be noted from above two figures that even after bearing a major negative gross margin, the Island Park store achieves the maximum total gross margin. Thus, from this, it could be deduced that some loss leader pricing has been done by Island Park store. To further analyze, we curated the list of items for Island Park store which have negative gross margin. We selected top 15 products having highest negative loss margin. Next figure shows that there are some items like Fasteners, Lawn Food, LED Feit and Top Soil etc. are offered at lower prices (with negative gross margin) to the customers in expectation of purchasing other products which are relatively expensive. Thus we can say that, the items like Fasteners, Lawn Food, LED Feit and Top Soil etc. are used as Loss Leader products which gives us an indication that giving away these products at a loss, will lead to customers having to buy other products, in order to make use of them.

![Negative Gross Margin per Item (Island Park store)](https://github.com/Kaustubh-Sable/Retail-Data-Analysis/blob/master/Loss_Leader_Analysis/Images/Neg_Gross_Margin_Per_Store_IP.png)

Furthermore, we did similar Loss Leader analysis for PASADENA store having store number 16661. We grouped each item in PASADENA store having negative gross margin and selected top 15 items having most negative gross margin. Next figure shows that NUT AND BERRY BUDDIES has a huge negative gross margin, most among all items in PASADENA store. However, upon further analysis, it was found out that the positive margin for NUT AND BERRY BUDDIES is 1139074:12 while the negative margin is 1125783:58. The resultant difference between Positive and Negative margin is very low i.e. 13290.54. This large negative gross margin shows that either the Leader Loss analysis is not done properly for item NUT AND BERRY BUDDIES or that the item itself is not profitable for the PASADENA store. Next figure shows negative gross margin of NUT AND BERRY BUDDIES is significantly large than other items. Hence, PASADENA store should revisit its negative margin items and increase margin on NUT AND BERRY BUDDIES in order to increase profits. Also, interesting insights could be taken from Island Park store which has implemented the Loss Leader strategy successfully.

![Negative Gross Margin per Item (Pasadena store)](https://github.com/Kaustubh-Sable/Retail-Data-Analysis/blob/master/Loss_Leader_Analysis/Images/Neg_Gross_Margin_Per_Store_PD.png)


#### References
* https://www.shopify.com/encyclopedia/loss-leader-pricing#:~:text=Loss%20leader%20pricing%20is%20a,step%20foot%20in%20the%20store.
* https://www.dotactiv.com/blog/loss-leader
