The KNN algorithm assumes that similar things exist in close proximity(sometimes called distance, proximity, or closeness). Applicable in pattern recognition, data mining and intrusion detection. The separating boundary *becomes smoother with increasing value of K*. With K increasing to infinity it finally becomes all class A or all class B depending on the total majority. Error rate at K=1 is always zero for the training sample.

Two properties to define KNN:
*Lazy learning algorithm* − KNN is a lazy learning algorithm because it does not have a specialized training phase and uses all the data for training while classification.

*Non-parametric learning algorithm* − KNN is also a non-parametric learning algorithm because it doesn’t assume anything about the underlying data.

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
