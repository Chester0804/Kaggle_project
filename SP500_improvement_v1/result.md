# Result for the SP500 improvement
I tested three improvement method on SP500 using "Bernoulli Naive Bayes classifier, 1-2 n-grams, alpha=0.1, 1-day shift, combined all top news". It turns out that some proper risk management strategy can reduce drawdown. 

## Improvement Method
* Improvement 1: 
Adjust the threshold of predicting to be a up movement, i.e. normally, when the predicted up probaility is greater than 0.5, we will regard it as a up prediction, but now, we can increase this threshold to, say 0.7, meaning that we want more confidence on our prediction. The best Sharpe ratio is obtained when the threshold is set to be 0.99 whose Sharpe ratio is 1.822. 
* Improvement 2:
Add one more class. Suppose we are not so sure about our prediction, now we can choose to wait until we have enough confidence on our prediction. The new class is labeled as 0, up is labeled as 1, down is labeled as -1. The best Sharpe ratio in this case is 1.457.
* Improvement 3:
Set stop-loss. I consider to use the drawdown to stop loss. The drawdown will be calculated daily. If we have position and the signal is to hold that position, we need to check whether the drawdown in previous day has been over some pre-set value. If yes, then close the position to avoid further loss and if no, just hold that position. The best Sharpe ratio in this case is 1.023. 
