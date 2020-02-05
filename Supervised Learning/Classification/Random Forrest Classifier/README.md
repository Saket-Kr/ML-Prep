**Entropy** is nothing but the measure of disorder. High entropy means a high level of disorder (meaning low level of purity).

*Summation for all classes, -(sum of (plogp))*, where *p* is the probability of that class in our data.

**Information Gain** Information Gain from X on Y is the entropy of just Y subtracted by  entropy of Y given X. Like this, we calculate the reduction of uncertainty about Y given an additional piece of information X about Y. This is called Information Gain. The greater the reduction in this uncertainty, the more information is gained about Y from X.

**IG(Y, X) = E(Y) - E(Y|X)**

We calculate the entropy for Liability for each value of Credit Score and add them using a weighted average of the proportion of observations that end up in each value. Why we use a weighted average will become clearer when we discuss this in the context of decision trees.
The information gain from feature, Balance is almost 3 times more than the information gain from Residence! If you go back and take a look at the graphs you can see that the child nodes from splitting on Balance do seem purer than those of Residence. However the left most node for residence is also very pure but this is where the weighted averages come in play. Even though that node is very pure, it has the least amount of the total observations and a result contributes a small portion of it’s purity when we calculate the total entropy from splitting on Residence. This is important because we’re looking for overall informative power of a feature and we don’t want our results to be skewed by a rare value in a feature.


<img src="https://render.githubusercontent.com/render/math?math=c2lnbWE=e^{i \pi} = -1">


