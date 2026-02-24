# Dimensionality-Reduction
## Principal component analysis
It help reduce the number of features in datasets while keeping important ones

How it works:
1. Standardize Data
2. Calculate Coverance 
i,e consider the two features ; x1, x2
![alt text](image.png)

3. Find Principal Components
 > 1st Principal Component (PC1): The direction of maximum variance (most spread).
 > 2nd Principal Component (PC2): The next best direction, perpendicular to PC1 and so on.

# AX = LX
 When A acts on X it only stretches or shrinks X by the scalar L.
The direction of X remains unchanged hence eigenvectors define "stable directions" of A.

4. Pick The Top direction and Transform data
After calculating the eigenvalues and eigenvectors PCA ranks them by the amount of information they capture. We then:

Select the top k components that capture most of the variance like 95%.
Transform the original dataset by projecting it onto these top components.


Note in sklearn pca"
PCA simplifies the data, then Logistic Regression proves the simplified version still contains enough information to accurately classify wines. It's like showing you can identify countries by just 2 metrics (GDP & population) instead of needing 100 economic indicators!

## Linear Discriminant Analysis
1. Standardize the d - dimensional  dataset(d is the number of feaute)

2. For each class calculate d- dimesional mean vector

3. Construct the between class scatter, Sb and within class matrix Sw
4. compute the eigenvectors and corresponding eigen values of the matrix
5. sort the eigenvalues by decreasing order to rank corresponding eigenvectors
6. choose the k eigen vectors that corresponds to the k largest eigen values  to construct d*k  dimensional  transformation matrix, W; the eigenvectors are the columns of matrix
7. Project the examples of the examples onto the new feature subspace using the transformation  matrix, w

# Nonlinear  dimensionality reduction
The development and application of nonlinear dimensionality reduction techniques is also often referred to as manifold learning, where a manifold refers to a lower dimensional topological space embedded in a high-dimensional space. Algorithms for manifold learning have to capture the complicated structure of the data in order to project it onto a lower-dimensional space where the relationship between data points is preserved.

for more details: http://scikit-learn.org/stable/modules/manifold.html.


# Visualizing data via t-distributed stochastic neighbor embedding

Visualizing data using t-SNE by Maaten and Hinton, Journal of Machine Learning Research, 2018 (https://www.jmlr.org/papers/volume9/vandermaaten08a/vandermaaten08a.pdf)



