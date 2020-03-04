The perceptron is a simple algorithm which, given an input vector x of m values (x1, x2, ..., xn) often called input features or simply features, outputs either 1 (yes) or 0 (no). Mathematically, we define a
function: 

Here, w is a vector of weights, wx is the dot product , and b is a bias. If you remember elementary geometry, wx + b defines a boundary hyperplane that changes position according to the values assigned to w and b. If x lies above the straight line, then the answer is positive, otherwise it is negative. Very simple algorithm! The perception cannot express a maybe answer. It can answer yes (1) or no (0) if we understand how to define w and b, that is the training process that will be discussed in the following paragraphs. 
