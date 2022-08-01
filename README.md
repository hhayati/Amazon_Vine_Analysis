# Amazon_Vine_Analysis
## Overview of the analysis

This challenge goal was set to analyze Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

For this challenge dataset No.1 was used.  This dataset contains reviews of a specific wine. To do the analysis,  PySpark was used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, Pandas was used to determine if there is any bias toward favorable reviews from Vine members in your dataset.




## Results
A screenshot of the downloded initial datafarme is presented below.

![image](https://user-images.githubusercontent.com/58461542/182086328-f7093da3-8c59-43a6-9fae-41abca6cdd2b.png)



![image](https://user-images.githubusercontent.com/58461542/182086649-deefaa20-fa0d-454c-ad5a-3c04f38c5598.png)


A statistical summary of vine data is presneted here:
![image](https://user-images.githubusercontent.com/58461542/182087222-d7f5990c-8d88-4c49-87ad-96fd6cf7b4bd.png)




* There are 613 Paid vine reviewers and 64,968 non-paid vine reviewers. 
* Of paid vine reviewers, 222 ratings were 5 star.
* Of non-paid vine reviewers, 30543 ratings were 5 star.
* The ratio of 5 star review for paid vine reviewers is 0.3621533442088091
* The ratio of 5 star review for unpaid vine reviewers  is 0.47012375323236055



## Summary
These results indicate that there might be some positivity bias for reviews in the Vine program. The ratio -5-star reviews for non-paid reviewers is clearly higher than paid reviewers. However, this bias should be examined more closely because the sample size for non-reviewers is significantly larger than the sample size for paid reviewers. 

To investigate this issue further, it is suggested to repeat this analysis for other products in vine program and see if the sample size has any effect on this bias.
