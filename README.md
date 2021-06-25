# Campaign Finance Inferential Model 

## Goal
To infer which factors were most influential in determining the outcomes of the 2015-16 American House and Senate races.


##Steps

Source

Data pulled from Finance info is from the Federal Election Committee (FEC). We used the 'Campaign Finance versus Election Results' dataset from [Kaggle](https://www.kaggle.com/danerbland/electionfinance). The dataset contained information on state, district, party, contributions, expenditures, etc. The information contained in the dataset is from the Federal Election Committee (FEC) and the results from CNN's election page. 


##Cleaning

The data presented itself with ample opportunity for cleaning. There were large numbers of columns dealing with detailed accounting figures. Furthermore, the data in these columns were the wrong datatype and required processing. Additionally, we ended up dropping numerous columns and rows that dealt with the presidency. We also dropped columns concerning states as they interfered with our investigation into how campaign finance influenced the election. 


##EDA
Our EDA overturned some of our prior assumptions. We learned that individual contributions played an insignificant role in the outcome of House and Senate races. Additionally, candidate contributions to their own campaigns played the most significant role in our best model. On the other hand, contributions that stemmed from political parties played a significant role in the outcome of elections. Moreover, as expected those running for Senate tended to receive more money than those who ran for Congress. 


![EDA](https://raw.githubusercontent.com/ntsegaw/campaign_predictions/main/images/Net_Cont.png)


##Baseline Model

For our baseline model, we ran a dummy classifier which returned a score of 0.72. 


##Preprocessing 

We created a matrix of features, a target variable, and a list of features to be used in the model. We then defined our categorical and numerical columns and after that created pipelines for each. After that, we fitted and transformed our training data in the numerical columns. We created a pipeline for our features and ran onehotencoder to create dummy columns for our categorical features. 




##Models (Logistic Regression, Random Forest, XGBoost)

For our first model, we chose to use a pipeline and grid-search to run logistic regression. Our best parameters returned an F1 score of 0.9 and our AUC was equal to 0.98. For our next model, we used random forest. Again, we used a pipeline with grid-search and our best parameters returned an F1 score of 0.93. Lastly, we ran XGBoost with a pipeline and grid-search which returned the same F1 score as random forest. The AUC was 0.99 for both of them. 

![AUC IMAGE](https://github.com/ntsegaw/campaign_predictions/blob/main/images/RF.png)

## Author
[Adam Cumurcu](https://github.com/AdamCumurcu)

[Natnael Tsegaw](https://github.com/ntsegaw)