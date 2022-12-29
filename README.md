# Wine-Quality-Assessment
Scenario: You are working for a large beverage distributor that among other products specializes on selling wine. Every year a new batch of different wines is delivered from all over the world for further distribution. To assess the quality of wine (and price it appropriately) the distributor hires a sommelier – a trained and knowledgeable wine professional who can determine the quality of the product. Given the variety and quantity of products, the company must hire at least 3 of such professionals. While the hired sommeliers are doing a great job in determining the wine quality, their services are expensive and time consuming. 

As an alternative solution to this problem, the company decided to use big data analytics approach. They took about 5,000 different wines for which the sommeliers have already determined the quality (on a 1 to 10 scale) and sent them to a laboratory for chemical analysis. Based on the analysis, they were able to identify 11 of the most important characteristics that determine the quality of the wine: fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, ph-level, sulphates, and alcohol. 

The distributor now plans to train a machine learning based algorithm that would allow quality assessment of any of its new wines using the 11 characteristics determined by chemical analysis. By doing so, the distributor anticipates reducing its costs and time required for wine quality assessment.

You are tasked to train an algorithm for assessment of the wines using the dataset available in Canvas/Files/HW3 You are advised to follow the following procedures:

1.	Prepare data for analysis: import dataset, handle missing values if there are any, ensure all variables are numerical, run basic commands to describe your data including distribution of the outcome variable. 
2.	Train a baseline model using Linear Regression:
2.1	Specify the input (X) variables and target (y) variable. Use all available features for training. 
2.2	Split the data into training (70%) and validation (30%) sets (use random_state = 0)
2.3	Instantiate the regressor, train it, and make predictions on the validation set.
2.4	Evaluate prediction performance using root mean squared error (RMSE). Provide a brief written statement with your overall conclusions associated with your baseline model’s accuracy.
Note: The baseline accuracy that you should be able to achieve is RMSE = 0.779
3.	The baseline RMSE of 0.71 that you should have achieved is not a bad start for any machine learning project. Now, your task is to improve your prediction accuracy. To do so, you should try:
3.1	Standardize your predictors, re-run your model, and provide a brief statement if your RMSE improved considerably. Continue using standardized predictors for the rest of the analysis. 
3.2	Check the variables for signs of multicollinearity. Re-run your model with two variables that are mostly collinear removed from analysis. Provide a brief statement if removing those two variables improves your prediction accuracy.
3.3	Three features – residual sugar, free sulfur dioxide, and density – have noticeable outliers. Use scatter plots to identify those and exclude them from the dataset (by creating a new data frame without outliers). Re-run your model using a newly created data frame that contains no outliers. Provide a written statement if you observe considerable improvement in your prediction accuracy. Decide if you want to continue with original data frame or one with removed outliers. 
3.4	Run a KNN model with number of neighbors equal to 5. Provide a brief statement if using KNN model improves your prediction accuracy.
3.5	Run appropriate code to determine the optimal value for k using a range from 2 to 22. 
3.6	Re-run your KNN model with the “optimal” number of neighbors value. Provide a brief statement if you were able to improve your prediction accuracy.
3.7	Now, import the library to run a Support Vector Regressor (SVR) model, https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVR.html 
3.8	Using example in the self-study notebook, run a Grid Search for SVR model trying the following values for the corresponding parameters:
(i)	C (regularization parameter) values from 1 to 3,
(ii)	kernel: rbf and poly,
(iii)	gamma: scale and auto
3.9	Now, using the “best” parameters suggested by GridSearchCV, re-run your SVR model. Provide a brief statement if using SVR with parameterization suggested by GridSearchCV improves your prediction accuracy.
3.10	 Finally, using 5-fold cross validation, run your “best” performing model using appropriate scoring and make a conclusion if your model trains equally well on different randomly drawn datasets or there is variance bias present. 
