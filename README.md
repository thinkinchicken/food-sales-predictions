# Food Sales Predictions
## Overview
Sales prediction for food items sold at various grocery and supermarket stores. 
In this workbook, we will be exploring the data from supermarket and grocery stores and seeing if we can train models to predict sales off of this current data set using several different methods. There are steps to clean the data and also prepare it for machine learning. We will also evaluate which model is best at predicting said sales off of the given features. We will also need to evaluate which features are the most important in these models. 

## Exploring the data
We first need to better understand the data and make sure that the data is clean and ready to be analyzed. Once that is done, we need to see if there are 
any strong relationships or correlations amongst the different attributes found within this dataset. 
Below is an example of the columns and the type of data we are looking at:
![image](https://user-images.githubusercontent.com/89652123/136720728-5fded79e-7588-417e-a575-f4228af265dc.png)
As mentioned above, there was a need to make sure that the data was clean and ready to work with. 
We ran a couple diagnostic codes to make sure everything was ready to go and there weren't any duplicates and that each of the columns were the correct data type
according to the data dictionary. 
We then start plotting to get a better visual idea of the data.

Figure 1 - A),B),C): We start with Histograms to see if there is anything interesting in the frequency distribution of some of this data. 
Nothing too interesting from these histograms

![image](https://user-images.githubusercontent.com/89652123/136722025-617a0870-2995-4831-82e1-eb79c56b192e.png)

![image](https://user-images.githubusercontent.com/89652123/136722064-7ba705ed-1572-4ef9-b14d-e0e56cf595ff.png)

![image](https://user-images.githubusercontent.com/89652123/136722087-ffca4a85-2ca0-4b32-b90e-46cc16ad4bbe.png)

So we move onto some boxplots to see if there may be some outliers in some of these quantitative data.

Figure 2: We take a look at the distribution of Item sales of Items based off of their fat content. From this we want to see if 
low fat or regular fat products may have higher sales. From the figure, we see that they are pretty equal with outliers in both. 

![image](https://user-images.githubusercontent.com/89652123/136721006-3582bdba-c195-458c-9118-44d704bdc787.png)

Figure 3: We take a look at another boxplot of item outlet sales by item type to see if any specific item sticks out as a higher sales item. 
![image](https://user-images.githubusercontent.com/89652123/136721068-abd10c2d-8a4f-4fd7-88bd-b265aec4d10b.png)


Figure 4: We take a look at the quantitative values in our data and see if there is any correlation amongst them. 
This heatmap gives us the information that Item MRP and Item Outlet Sales have a pretty decent correlation. Not super strong but 
there is something there worth looking into. 

![image](https://user-images.githubusercontent.com/89652123/136721167-8e1ea61f-7eb7-4abc-85f9-66b79d8f9cf4.png)

We also look into some horizontal bar charts of each super market type. We find that there are top item types that are consistently seen
across each super market type: Fruits and Veggies, Household Items, Frozen Foods, Snack Foods, and Dairy. 

See below Figure 5: for the example for Supermarket Type 3

![image](https://user-images.githubusercontent.com/89652123/136721315-64e6338a-f12a-4d6a-8b29-8c57966997e3.png)


## Machine Learning and Predictions
Let's start diving into machine learning and whether we can train the data to help us predict item sales. 
We end up prepping the data by one hot encoding all the categorical features that are within the data set. 
We will go through 4 different machine learning models of predicting Item Sales based off of selected features. 
The four models are: 
1) Linear Regression
2) Regression Tree
3) Bagged Trees
4) Random Forests

We will train and test each data set using machine learning and evaluate how each performs on both the training and testing data. 
Using an R2 value as the main gauge for how well of a fit the model is to predicting the data. 
We will also take a look at the RMSE(root mean square error) of the predictions of each model in order to evaluate how much 
error is to be expected from each of these models.  

## Results 

A couple of hyperparameters needed to be altered for the Random Forest model/Decision Tree model in order for it to have the highest R2 value. 
We ran a function in order to see the max depth of the tree that would optimize our R2 value and we found it to be max_depth = 5. 

Figure 6: Max Depth optimization for Random Forest/Decision Tree Model 

![image](https://user-images.githubusercontent.com/89652123/136722850-51052382-c9e4-4872-828d-10008a611b77.png)

Lastly, just out of curiosity, I look into the top features based off of importance in the Random Forests model. 
We see that the values are pretty darn similar to the correlations we looked at before where Item_MRP is clearly the strongest
in predicting Item Sales. I decide not to get rid of any of the features because I am unsure of what the threshold should be in removing them. 

Figure 7: Top 10 Feature Importance for the Random Forest Model

![image](https://user-images.githubusercontent.com/89652123/136722967-275032f4-70e4-4482-bebb-8eb9eca51c69.png)


## Conclusion

Once we have run through all 4 models, we find that although not perfect in it's predictions and not optimal, the Random Forests model is the best 
fit for predicting sales in comparison to the other 3 models. Both the Decision Tree and Random Forest model show promise in the R2 values, but the Random Forest is 
ever so slightly better. Although they aren't perfect, the training and test scores for these models are relatively close, which suggests that predicting on the
test set is pretty on par with the training set. These two models(Regression decision tree & Random forests) also do much better than the simple linear regression model, 
where the R2 value for the test set proved it was unsuccessful at predictions. We can say that from the random forests model, that 60% of the variation within
the prediction in the item_outlet_sales can be accounted for by the features we selected for this model. 
In addition, we can say that the variation in error on any predictions made off of this model, given by the RMSE is about plus or minus $667 in item sales. 



