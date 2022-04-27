## Welcome

I am Andy Huynh. I am currently a Ph.D. student at Rutgers University interested in low dimensional topology. In my spare time, you might see me building Legos or tinkering or fixing some electronics. Here are some projects I worked on in the past.


## [Ubiquant Market Prediction](https://github.com/andyhuynh92/Ubiquant-Comp)

This is a project on Kaggle collaborating with [Professor Lei Yu](https://alcoholstudies.rutgers.edu/people/faculty/lei-yu/) and members of his laboratory. 

[Ubiquant](https://www.kaggle.com/competitions/ubiquant-market-prediction)

### Goal: 

The goal is to use the given data containing a `time_id`, `investment_id`, and 300 features to predict `target`. How they measure how submitted models perform is to find the mean of Pearson correlation between our predictions to the true values at each `time_id`. 

### Data Description: 

The data given is completely anonymized. That means
- All 300 features are anonymized. 
- Both time of the investment and the stock are anonymized. 
- The target is anonymized. 
In addition, I found out that the data has been additionally processed. In particular, fixing a value for a `time_id`, I found out that most of the time(but not all), the feature will have mean 0 and standard deviation 1.

From public forums, people were able to reverse engineer both `time_id` and `investment_id`, figuring out the real time correspondence for `time_id`, and the likely stock tickers corresponding to each `investment_id`. Using this data, I grabbed the stock data using the Yahoo! finance API and ran correlations between the stock price and the features. We discovered that the features and target are both detrended and normalized at each `time_id`, i.e., the features and target have mean 0 and standard deviation 1, making it difficult to reverse engineer the existing features and feature engineer new ones.

We submitted two models. The first model used LightGBM. The second model is an ensemble with LightGBM and a deep neural network.

## JPX Kaggle Competition(Currently ongoing)

Continuing from the Ubiquant Kaggle competition above, we followed up doing another [Kaggle competition hosted by JPX](https://www.kaggle.com/competitions/jpx-tokyo-stock-exchange-prediction), the parent company of the Tokyo stock exchange. The goal of this competition is to rank the stocks in the Tokyo stock market and get the highest competition metric, based on the [Sharpe ratio.](https://en.wikipedia.org/wiki/Sharpe_ratio)

The given data is directly from the Tokyo stock market. 


## [Root Insurance project](https://github.com/gedwards09/Root-it)

THis is a projet done with the Erdos Institute. 

Root Insurance – Bidding Strategy
Goal: Modelling bids for ad placement, a project with the Erdos Institute
Processed the data, featuring mostly categorical data using one-hot encoding
Modelled expected cost from given data, assuming certain probability distributions
Minimized the cost function constrained to 400 sales using gradient descent with a barrier function
Developed a strategy that saves up to 70% in costs depending on the desired number of expected sales
