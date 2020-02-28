The KNN algorithm assumes that similar things exist in close proximity(sometimes called distance, proximity, or closeness). Applicable in pattern recognition, data mining and intrusion detection. The separating boundary *becomes smoother with increasing value of K*. With K increasing to infinity it finally becomes all class A or all class B depending on the total majority. Error rate at K=1 is always zero for the training sample. Research has also shown that a small amount of neighbors are most flexible fit which will have low bias but high variance and a large number of neighbors will have a smoother decision boundary which means lower variance but higher bias. Generally, for K odd number is chosen when the number of classes is even. It can be used with the regression problem. Output value for the object is computed by the average of k closest neighbors value. KNN is not suitable for the large dimensional data. We don’t use manhattan distance because it calculates distance horizontally or vertically only. It has dimension restrictions. On the other hand, euclidean metric can be used in any space to calculate distance. Since, the data points can be present in any dimension, euclidean distance is a more viable option. 

Two properties to define KNN:
*Lazy learning algorithm* − KNN is a lazy learning algorithm because it does not have a specialized training phase and uses all the data for training while classification. Lazy algorithm means it does not need any training data points for model generation. All training data used in the testing phase. This makes training faster and testing phase slower and costlier.

*Non-parametric learning algorithm* − KNN is also a non-parametric learning algorithm because it doesn’t assume anything about the underlying data.

In large dimension Euclidean distance is not useful anymore, hence cosine similarity can be used.

**Algorithm**
1. Load the data
2. Initialize K to your chosen number of neighbors
3. For each example in the data
3.1 Calculate the distance between the query example and the current example from the data.
3.2 Add the distance and the index of the example to an ordered collection
4. Sort the ordered collection of distances and indices from smallest to largest (in ascending order) by the distances
5. Pick the first K entries from the sorted collection
6. Get the labels of the selected K entries
7. If regression, return the mean of the K labels
8. If classification, return the mode of the K labels

**Advantages**
- The algorithm is simple and easy to implement.
- There’s no need to build a model, tune several parameters, or make additional assumptions.
- The algorithm is versatile. It can be used for classification, regression, and search (as we will see in the next section).

**Disadvantages**
- The algorithm gets significantly slower as the number of examples and/or predictors/independent variables increase.
