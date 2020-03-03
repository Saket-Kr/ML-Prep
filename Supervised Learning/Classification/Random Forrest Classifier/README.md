**Entropy** is nothing but the measure of disorder. High entropy means a high level of disorder (meaning low level of purity). Entropy shows the level of disorganization in your data and reduces with increasing proximity to the leaf node.  

**Entropy is given by the formula, <img src="https://render.githubusercontent.com/render/math?math=E(S)%20=%20\sum_{i=1}^c%20%20-%20p_i*%20log_2%20p_i">, where *p* is the probability of that class in our data.**

**Information Gain** Information Gain from X on Y is the entropy of just Y subtracted by  entropy of Y given X. Like this, we calculate the reduction of uncertainty about Y given an additional piece of information X about Y. This is called Information Gain. The greater the reduction in this uncertainty, the more information is gained about Y from X.  Information gain depends on a reduction in entropy following the spilling of a dataset on an attribute. Information gain increases with proximity to the leaf node.  

**Information gain is given by the formula, *IG(Y, X) = E(Y) - E(Y|X)***



Read the decision tree example from [How Decision Trees Make Decisions : towards DataScience](https://towardsdatascience.com/entropy-how-decision-trees-make-decisions-2946b9c18c8) to get the clear picture with very nice explanantion. 



