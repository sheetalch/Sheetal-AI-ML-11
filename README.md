Step #1: Business Understanding
This research assignment uses a vehicle dataset and analyses the data using different model. I followed the CRISP-DM methodology for the data analysis. 

Step #2 - 3: Data Understanding and preparation 
I used the following steps to understand the vehicles dataset: 
1. Executed Dataframe.info() to get the list of columns, number of rows etc 
2. Removed null values from the dataframe. 
3. Used different barplots and countplots to review the data. 
4. The plot result showed that the data was not evenly distributed across 
   different values of the columns. So, I decided to filter the data for further analysis: 
   list_of_manufacturers = ["ford","chevrolet"]
   list_of_condition = ["excellent","good","like new"]
   list_of_fuel = ["gas"]
   list_of_title = ["clean"]
   list_of_type = ["SUV","sedan","truck"]
   list_of_size = ["full-size","mid-size","compact"]
   list_of_paint = ["red","blue","black","grey","silver","white"]
   list_of_cylinders = ["4 cylinders","6 cylinders","8 cylinders"]  
5. Removed price outliers using quantile method. 
6. Executed Dataframe.corr() to determine the correlation of price and various    
   attributes and found posivite and negative correlation of various attributes to price. 
7. Split the dataset into training and test datasets. 

Step #4: Modeling
In this step, I created several models using: 
1. Linear Regression 
2. Ridge Regression
3. Ridge Regression with optimal alpha (using GridSeachCV) 
4. Sequential Feature Selection
5. Lasso Regression 

Step #5: Evaluation 
Evaluated all the models using the mean squared error for training and test datasets. 
Best features found using Sequential Feature Selectors are - 
condition_excellent  
condition_like new  
drive_4wd  
size_compact
size_full-size  
type_SUV  
type_truck  
paint_color_red

The Lasso model was found to have the least training MSE. But the training MSE was higher. 

After evaluating the training and test MSEs of all the models, I concluded that the model generated using sequential feature selection is the best as the difference between the training and test MSEs is on the lower side compared to that of the other models. 

Step #5: 
Deploy the Readme and jupyter notebook to GIT Hub. 