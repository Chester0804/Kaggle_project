
# Summary for Stage 1 Result


## For DJIA:

I backtested two strategies which are the cases short selling is not allowed and short selling is allowed. For each case, I selected five cases from the Kaggle solution which are:
* Baseline classifier: Naive Bayes classifier, no n-gram, no shift, combined all top news
* Bernoulli Naive Bayes classifier, n-grams, alpha=1, no shift, combined all top news
* Bernoulli Naive Bayes classifier, 1-2 n-grams, alpha=0.1, 1-day shift, combined all top news
* Bernoulli Naive Bayes classifier, 1-2 n-grams, alpha=0.5, 3-day shift, combined all top news
* Bernoulli Naive Bayes classifier, 1-2 n-grams, alpha=0.5, 2-day shift, combined top3,top12 and top25 news

Also, each method is backtested in the cases which the filling method is:
* fill at T+0 adjusted close price
* fill at T+1 open price

### Key result
The best Sharpe ratio obtained is 0.53 in the case that short selling is not allowed and 1.24 in the case that short selling is allowed. 
Using neural network classifier can obtain a slightly higher AUC (around 0.7), but the Sharpe ratio in the case that short selling is allowed can be improved to 1.56.

## For SP500:

### Key result
For SP500, I adapt the similar method and test cases but just assume that short selling is allowed. The AUC is quite bad in all the 5 cases, which is just around 0.52 (including neural network classifier). The highest Sharpe ratio is achieved by using neural network classifier with 0.72. 

## Further improvement

As stated in each notebook, I proposed three ways to improve the result
* Try different weights of top news
* Try other classification algorithms
* Use more advanced NLP methods

The first two are tested in all three notebooks. Neural network may improve the classification performance. I plan to try something NLP solution when dealing with neural sentiment classification. 
