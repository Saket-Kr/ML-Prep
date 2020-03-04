The perceptron is a simple algorithm which, given an input vector x of m values (x1, x2, ..., xn) often called input features or simply features, outputs either 1 (yes) or 0 (no). Mathematically, we define a
function: 

        f(X) = 1 if wx + b > 0 or 0 otherwise

Here, w is a vector of weights, wx is the dot product , and b is a bias. If you remember elementary geometry, wx + b defines a boundary hyperplane that changes position according to the values assigned to w and b. If x lies above the straight line, then the answer is positive, otherwise it is negative. Very simple algorithm! The perception cannot express a maybe answer. It can answer yes (1) or no (0) if we understand how to define w and b, that is the training process that will be discussed in the following paragraphs. 


Historically, perceptron was the name given to a model having one single linear layer, and as a consequence, if it has multiple layers, you would call it multilayer perceptron (MLP). 

Cons:
A perceptron is either 0 or 1 and that is a big jump and it will not help it to learn.
