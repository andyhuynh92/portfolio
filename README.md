## Welcome

This is my website


### Ubiquant 

This is a project on Kaggle collaborating with [Professor Lei Yu](https://alcoholstudies.rutgers.edu/people/faculty/lei-yu/) and members of his laboratory. 

[Ubiquant](https://www.kaggle.com/competitions/ubiquant-market-prediction)

The goal is to use the given data to predict the target. How they measure how submitted models perform is to find the mean of Pearson correlation between our predictions to the true values at each `time_id`. 

The data given is completely anonymized. All 300 features are anonymized. Both time of the investment and the stock are anonymized. The target is anonymized. 

From public forums, people have reverse engineered both `time_id` and `investment_id`. Using this data, I then grabbed the stock data using the Yahoo! finance API and ran correlations between the stock price and the features. We discovered that the features and target are both detrended and normalized heavily at each `time_id`, making it difficult to reverse engineer the existing features and feature engineer new ones.

We submitted two models. The first model used LightGBM. The second model is an ensemble with LightGBM and a deep neural network.

### JPX Kaggle Competition(Currently ongoing)

Continuing from the Ubiquant Kaggle competition(below), we followed up doing another [Kaggle competition hosted by JPX](https://www.kaggle.com/competitions/jpx-tokyo-stock-exchange-prediction). The goal of this competition is to rank the stocks in the Tokyo stock market and get the highest competition metric, based on the [Sharpe ratio.](https://en.wikipedia.org/wiki/Sharpe_ratio)

The given data is directly from the Tokyo stock market. 


### Root Insurnace project

Root Insurance – Bidding Strategy
Goal: Modelling bids for ad placement, a project with the Erdos Institute
Processed the data, featuring mostly categorical data using one-hot encoding
Modelled expected cost from given data, assuming certain probability distributions
Minimized the cost function constrained to 400 sales using gradient descent with a barrier function
Developed a strategy that saves up to 70% in costs depending on the desired number of expected sales
