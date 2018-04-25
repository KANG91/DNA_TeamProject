# Santander Product Recommendation

### Synopsis
There are 13,647,309 bank records from Jan, 01, 15 to May, 30, 16 that occured in Santander bank in Spain. Independent variables are all kinds of customer's personal information like sex, age, seniority and so on.  What we had to do was that recommend the fittest product to customers based on past visit information. 

### Evaluation method
$$ MAP@7\quad =\quad \frac { 1 }{ \left| U \right|  }\sum _{ u=1 }^{ \left| U \right|  }{ \frac { 1 }{ min(m,7) } }\sum_ { k=1 }^{ min(n,7) }{ P(k) }  $$
where |U| is the number of rows (users in two time points), P(k) is the precision at cutoff k, n is the number of predicted products, and m is the number of added products for the given user at that time point. If m = 0, the precision is defined to be 0.

### Things that we consiered
- How to deal with NULL values
> Some variables are asymmetric like they have only one or two classes.
>  After some kind of test, we conclude that too less class values can't influence with results.
- What kind of algorithm we use?
> We tried some basic classification algorithm at first like Logistic, LDA, QDA, But, result was not that good
> We assume that complicated algorithm can control complicated rules in data.
> After some kind of test, we think that 'XGboost' is the fittest for our model
- over 13 million data!
> it was the hardest part of this project.
> For me, I used google colab.

### Final result

Best score : 0.0298268 - 255th/1787(14%)
> feature selection : sex, age, seniority, active or not, type of customers, house income, province code  and so on 

### Conclusion
1. What we learned from project...
- We did not repeat same mistake as we did at first project.(I would like to compliment to myself:))
- Data scientist always can struggle with BIG data problem. I should learn how to deal with it.

2. Now, We can do....
> - We can now classify multi-class data by using logistic, randomforest, xgboost and check performance.
