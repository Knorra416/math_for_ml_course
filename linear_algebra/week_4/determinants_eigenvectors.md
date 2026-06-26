### Singularity and rank of all linear transformations 

* Non singular transformation
    - New basis covers the entire plane. 
    - If our transform is only one line segment, it can't cover the plane. 

* When a matrix is singluar, only covering portion of plane (line) in transform space

* Rank == dimensions of the image of the linear transformation 

### Determinant as an area 

* Determinant of the matrix is the area of the image matrix after transformation 
    * Singular matrix: Det = 0 and area = 0 

* Negative determinants
    - parallelogram can have a negative area 

### Determinant of a product 
* Determinant of product matricies 
    det(AB) = det(A) * det(B)

* Product with singular matrix means the product is singular too (since singular matrix has determinant zero)

### Determinants of inverses
* Determinant of an inverse is det^-1 (inverse determinant value)
    * det(A^-1) = 1/det(A)
* Singular matrix has no inverse 

### Bases in Linear Algebra 
* Two vectors coming from the origin are the basis
    - Two vectors which form a line are NOT a basis

### Span in Linear Algebra 
* Basis is a minimal spanning set
* Overlapping or vectors in the same line are not a basis

* Linear independent and dependent vectors
    - A vector can't be obtained through linear combination of the others then it is independent 
    - Dependent: can be obtained through linear combination with other vectors 
        * If two vectors span the plane, then any third vector added will always be dependent 
* Basis formal definition
    - A basis is a set of vectors that:
        * Spans a vector space 
        * Is linearly independent 

### Eigenbasis 
    - A special way of looking at a linear transfermation wrt a basis.
    - Moves the entire parallelogram by two stretches 

### Eigenvalues and Eigenvectors
- Formalized Eigenvalue definition
    - A * v1 = lambda1 * v1 
    - A * v2 = lambda2 * v2

    - Lambda1/2 are Matrix A's Eigenvalues
    - v1/v2 are Matrix A's Eigenvectors 

    - More efficient to use than Matrix multiplication 

    * Eigenvectors: the direction of stretch
    * Eigenvalues: how much it is stretched 
    * Eigenbasis: the set of matrix's eigenvectors, can be arraged as a matrix with one eigenvector in each column 


### Calculating Eigenvalues and Eigenvectors
* Finding Eigenvalues 
    - Find the place where characteristic polynomial is zero
    - For a 2x2 matrix [a, b       solve determinant = 0 of A - lambdaI so (a - lambda)x(d - lambda) - bxc =0
                        c, d]
    - For a 3x3 matrix, use rules to calc determinant and subtract lambda from diagonal. solve for lambda 
* Finding Eigenvectors
    - Use eigenvalues to solve system of linear equations with the associated matrix 

### On the Number of Eigevectors
* Can find distinct Eigenvectors even with repeated Eigenvalues 
* Summary
    - 2x2 
        - If EV1 != EV2, 2 Eigenvectors (2 directions)
        - If EV1 = EV2, 1 or 2 Eigenvectors
    - 3x3 
        - If EV1 != EV2 != EV3, 3 Eigenvectors (3 directions)
        - If EV1 = EV2 != EV3, 2 or 3 Eigenvectors
        - If EV1 = EV2 = EV3, 1 or 2 or 3 Eigenvectors
    
### Dimensionality Reduction and Projection 
* PCA
    - Goal: reduce dimensions (# columns) and preserve as much information as possible 
    - Projection: move datapoints into a space with smaller dimensions 
    * In general
        - To project Matrix A onto vector v
            - Ap = A * v/||v||2 
            - denom is norm of v

### Motivating PCA 
* Can project onto any line.
    - The more spread out the points are on the line, the more information is preserved. The goal is to find the project that maintains the maximum spread of the data 

    - Benefits of dimensionality reduction
        - Easier dataset to manage, PCA does this while minimizing information loss
        - Easier to visualize

### Variance and Covariance 
* Variance: The average squared distance from the mean 
* CoVariance: Measures how two features of dataset vary with respect to each other 
    - The direction of the relationship between two variables 

### Covariance Matrix 
* Compact way of storing all the relationships between variables in dataset
* Diagonal stores the variances of the pair of features, off-diagonal stores the corvariance 
* COV(x,x) == Var(x)

### PCA Overview 
* PCA combines projection, Eigenvectors/Eigenvalues, and Covariance matrix in clever ways to find the optimal number of components to reduce to. 
* The Eigenvector which gives the larger Eigenvalue will always have the most variance (and thus the better principal component)

### PCA - Mathematical Formula 
1. Create a matrix - n obs (rows) x y (columns)
2. Center the data - subtract column mean from each value 
3. Calculate Covariance matrix: 1/(n-1) x (X - u)T(X - u)
4. Calculate Eigenvalues and EigenVectors For the covariance matrix, sort by the EigenValues
5. Create Projection Matrix 
    - V = each column v1/||v1||2
6. Project Centered Data: Xpca = (X-u)*V

### Discrete Dynamical Systems 
* Markov Matrix - all values positive and add up to 1

 

    




