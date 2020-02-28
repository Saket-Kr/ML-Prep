K-Means is an unsupervised ML algorithm.
K-means generally uses on Euclidean Distance which computes the root of square difference between co-ordinates of pair of objects. We don’t use manhattan distance because it calculates distance horizontally or vertically only. It has dimension restrictions. On the other hand, euclidean metric can be used in any space to calculate distance. Since, the data points can be present in any dimension, euclidean distance is a more viable option.   
It is given by <img src="https://render.githubusercontent.com/render/math?math=\sqrt\sum_{k=1}^m%20(X_i_k%20-X_j_k)^2">.  
Other types of distance that can be used are:  
- Manhattan Distance - It computes the absolute differences between coordinates of pair of objects, given by
<img src="https://render.githubusercontent.com/render/math?math=Dist_{XY}=\sqrt{\sum_{k=1}^m%20(X_{ik}%20-X_{jk})^2}">
2.3 Chebychev Distance
Chebychev Distance is also known as maximum value
distance and is computed as the absolute magnitude of the
differences between coordinate of a pair of objects. 
International Journal of Computer Applications (0975 – 8887)
Volume 67– No.10, April 2013
14
2.4 Minkowski Distance
Minkowski Distance is the generalized metric distance.
Note that when p=2, the distance becomes the Euclidean
distance. When p=1 it becomes city block distance.
Chebyshev distance is a variant of Minkowski distance where
p=∞ (taking a limit). This distance ca
