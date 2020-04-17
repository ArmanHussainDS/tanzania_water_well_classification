 Hello everyone and welcome to our project Pump it Up: Data Mining the Water Table!

 Here I will outline our journey diving into Tanzanian water pumps from start to finish, referecing our competiton notebook where you can find all of our code. 

-----------------------

 What are we doing?
 
 - We are working on behalf of Tanzania's Ministry of Water to help predict which water pumps across the country are functional, completely broken or in need of some sort of maintenance. 
 
 - We are also collaborating with Taarifa, an open-source web API that offers a lot of data on this particular problem. 
 
 - Our goal is to best predict issues with water pumps to promote greater access to clean water across Tanzania, an issue plaguing much of the country. 
 
 - Our idea of success would be to achieve a classification accuracy of greater than 75% and to be able to give the Tanzanian Ministry of Water some key insights into which factors put a strain on pumps and how to best avoid them breaking down. We will also identify regions where a large majority of the pumps are non-functional which the Ministry can then target as a problematic area as a whole. 
 
 -----------------------
 
 Please find our Competition notebook in the folder!
 
 1. Data Understanding - Section 1.1

 We started by importing and understanding the data that we were given. The data can be found in the Raw_data folder. We did some merging and dropping of repeated rows, the ID's for example. We followed on by beginning to select data that we thought would be relevant in making predictions on the functionality. There was a lot of overlapping features, for example 5 separate geographical features therefore we began to cut these down and select only the most feasible to use (some had thousands of unique values). 

 Once we had selected the relevand data we made several visualisations to assist in understanding in simple terms how the features affected the target variable and any other early trends. This can be found in section 1.1.3. We also created a map of the distribution of pumps by their functionality across Tanzania which is useful for targeting improvement efforts geographically. 

 2. Data Preparation - Section 1.2

 Onto the preparation part! We began here by cleaning some of our features, preparing them for our modelling stage. There were several features that we assumed would be good predictors however had a vast majority of values at zero. We cleaned such features by creating a zero categorical feature for these values and kept the rest as continuous. We also feature engineered a new variable called duty_cycle which using two other features, estimated the operational life cycle of the pumps as a continuous variable. We proceeded to then dummy all of our categorical variables and drop the original ones and also drop all the features we thought to be irrelevant in the previous section.
 
 3. Modelling - Section 1.3
 
 We created an initial baseline model using a logistic regression without any tuning. The score on our validation set was 0.689, this was our score to beat for every future model! Next we added some regularisation to our logistic regression model in the form of L1 and L2 penalties. The L1 regularisation worked best and gave a score of 0.74! A big improvment already and without hardly any overfitting (training score a 0.06 higher). 
 
 Next we looked to a decision tree to try and obtain a higher accuracy score. These models are known to be good predictors but overfit too therefore it was no surprise that our model scored 0.752 on our validation set and 0.942 on our training. It was time to tune some hyperparameters. We decided to tune our decision tree's max depth and minimum leaf samples parameters and apply a 5-fold cross validation. We also tried tuning the max_features parameter however this caused our model to run for hours without converging so we decided to leave it out. Accuracy on our validation set went up to 0.76 and our training set obtained a score of 0.83 - overfitting had been reduced. We sought to tune  further by narrowing the range of parameters to use around the best_params we found here and our validation score went up slightly to 0.765.
 
 We looked now to a random forest classifier to further improve our performance. Our baseline model performed with a new best accuracy score on our validation set - 0.787 but again was considerably overfit with a training performance of 0.941. Our inital tuning of the random forest baseline did not yield any validation performance improvements however brought overfitting down. Similarly our second tuning iteration did not change our best performance score but we kept it as our new best model given the further reduction in overfitting. 
 
 Finally we used AdaBoost classifier to try and improve our model however no improvement to our accuracy was obtained.
 
 Now we wanted to see if we could play around with some feature engineering to try and come up with better scores. We first manipulated our independent variables adding in polynomial features. This significantly weaked our model. We also tried scaling the data which had no effect on our best performance. 
 
 There we had it, our final model was to be the second iteration tuned random forest classifier!
 
 4. Evaluation - Section 1.4

 We began by applying our model on our test set that we withheld from the beginning of the experiment. Our model returned a score of 0.789!! We had achieved a great degree of generalisation and a high score, exceeding our target of 0.75! We then made a visualisation of the top-10 feature importances and they denoted the features that are most important in explaining the target variable. 
 
 5. Notes - Section 1.5
 
 In the notes we include some work we did trying to use the OneVsRest Classifier on top of our final model in an attempt to get ROC curves and then select thresholds for our classification errors however it did not seem very intuitive. Also we played around with adding error bars to our feature importances however we could not come up with an error that made sense. 
 
 In conclusion, we found that Tanzanian water pump functionality is not easy to predict each region has its own issues that effect the functionality. We managed to however correctly predict functionality almost 80% of the time and came up with 10 features that our stakeholders should look at as being integral in deploying pumps across the country. 
 
 
 
 
 