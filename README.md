# NBA-Draft
The NBA draft selection is a multi-million-dollar pivotal decision for every NBA team. 
They determine which player will bring the most success to their organization. 
This year’s draft included big names like Zion Williamson as the #1 draft favourite. 
But, where will the rest of the exceptional players rank? We predicted the top 50 prospects entering the 2019 draft. 
The focus was on player’s advanced stats in the most recent NCAA college basketball season.

Predictive Model Approach: I used Jupyter notebook and Python throughout the process. 

Step 1. Data Collection and Scraping:

I collected and scraped 10 years of NCAA players’ advanced stats historical data and draft results from  https://basketball.realgm.com. One condition I used when I scrapped the data was Qualified players only. Which means, ‘a player must be on pace to play 15 minutes per game’. This effected any injured players during the NCAA season like top prospects Bol Bol  and Darius Garland. 

Step 2. Preprocessing and Cleaning:

I used Python NumPy and Pandas packages to understand the data and build it into a consistent format.

Step 3. Supervised Learning Model Building:  

With 22 variables, including 18 advanced stats. I started my feature selection process by
first, checking the coefficient of variation of each numerical. Second, from sklearn.metrics I checked adjusted_mutual_info_score for each variable. And ended up with 9 main variables ( eFG%, ORB%, DRB%, FIC , PER, class, position, draft pick, and draft results) to start building the predictive model.

Building of the predictive model using Scikit learn:
-	Target: draft results (Drafted or Not Drafted)
-	Checked different classification models to predict the draft results with Logistic Regression giving the best results
-	Used the coefficients of the Logistic Regression model to assess the variables of the model:
o	The below 3 variables has the highest impact on player getting drafted
 FIC , PER , and player position
o	The below 3 variables shows a negative impact of the players selection process
college year, ORB% and DRB%

Step 4. Evaluating and scoring the predictive model:

-	Calculated the AUC curve score: 92.78%
-	Determined where the threshold yields at least 70% tpr
-	Used threshold to calculate probabilities of player’s getting drafted 
-	Calculated recall, and precision scores and confusion matrix

Step 5. Predicted 2019 Draft Picks

-	Displayed results of players getting drafted or not drafted 
-	Calculated the probability of each player getting drafted and determined the rank of each player

Results
-	82% accuracy on players draft prediction
-	58% accuracy on players’ rank prediction based on round 1 and round 2 selection
