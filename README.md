

In this repo, I am trying to learn & implement GAIN AND LIFT CHARTS.

Gain and Lift charts are used to evaluate performance of classification model. They measure how much better one can expect to do with the predictive model comparing without a model. It's a very popular metrics in marketing analytics. It's not just restricted to marketing analysis. It can be used in other domains as well such as risk modeling, supply chain analytics etc. It also helps to find the best predictive model among multiple challenger models. In this tutorial, we will see how gain and lift metrics are calculated along with their interpretation.
# Gain / Lift Analysis
- Randomly split data into two samples: 70% = training sample, 30% = validation sample. 
- Score (predicted probability) the validation sample using the response model under consideration. 
- Rank the scored file, in descending order by estimated probability 
- Split the ranked file into 10 sections (deciles) 
- Number of observations in each decile 
- Number of actual events in each decile 
- Number of cumulative actual events in each decile 
- Percentage of cumulative actual events in each decile. It is called Gain Score. 
- Divide the gain score by % of data used in each portion of 10 bins. For example, in second decile, divide gain score by 20.

** Gain

Gain at a given decile level is the ratio of cumulative number of targets (events) up to that decile to the total number of targets (events) in the entire data set

** Lift

It measures how much better one can expect to do with the predictive model comparing without a model. It is the ratio of gain % to the random expectation % at a given decile level. The random expectation at the xth decile is x%.
