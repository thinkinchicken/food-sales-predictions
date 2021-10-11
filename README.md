# Food Sales Predictions
## Overview
Sales prediction for food items sold at various grocery and supermarket stores. 
In this workbook, we will be exploring the data from supermarket and grocery stores.
We first need to better understand the data and make sure that the data is clean and ready to be analyzed. Once that is done, we need to see if there are 
any strong relationships or correlations amongst the different attributes found within this dataset. 
Below is an example of the columns and the type of data we are looking at:
![image](https://user-images.githubusercontent.com/89652123/136720728-5fded79e-7588-417e-a575-f4228af265dc.png)
As mentioned above, there was a need to make sure that the data was clean and ready to work with. 
We ran a couple diagnostic code to make sure everything was ready to go. 
We then start plotting to get a better visual idea of the data. 
Figure 1: We start with Histograms to see if there is anything interesting in the frequency distribution of some of this data. 
Nothing too interesting from these histograms.

![image](https://user-images.githubusercontent.com/89652123/136720847-f9511553-c191-4468-a09d-b38215d931ca.png)

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



Let's start diving into machine learning and whether we can train the data to help us predict item sales. 
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


