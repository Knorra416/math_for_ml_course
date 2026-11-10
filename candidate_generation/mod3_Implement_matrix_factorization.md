### Scaling Collaborative Filtering
* Matrix factorization
    - User/Item interaction matrix 
        * users along one axis, items along another in a matrix. 
        * cells are the interaction values for those two. 
        * Not every user interacts with every item (sparse matrix)

* SVD is an elegant mathematical solution to this sparse matrix problem
    - Decomposes sparse matrix into lower-dimensional vectors
    - Captures latent user preferences and item traits 
    - Predicts missing interactions without complete historical data 

* Limits of SVD
    - ALS is designed to be parrallizable version of SVD bottlenecks 
    - Alternating steps solving user/ item factors 
    - Can parallize this 

### Objective Functions and Regularization 
* Eigendecomposition
    - A square matrix can be broken down into its Eigenvectors and Eigenvalues 
    - This maps the primary variance of data in the matrix 

* Real world problem:
    - Works for square, but user x item data is not square or dense

* This lead to Single Value Decomposition (SVD)
    - Factorizes any matrix with the following formula:
        - $M$ = $U$ x $\sum$ x $V^T$
        - Where:  $U$ holds user factors, $\sum$ holds singluar value diagonal matrix with weights of each dimension, and $V^T$ holds item factors. 
        - SVD fails for sparsity, cannot impute 

* ALS is the solution to issues with SVD 
    - Core formula: $R$ $\approx$ $U$ * $V^T$
    - Where $R$ is the original matrix (Users x Items), $U$ is the user matrix (Users x k), and $V^T$ (k x Items)
    - k is the rank (latent factor dimensionality)
    - Number of hidden dimensions used to describe users and items 
        * Model discovers this many categories on its own. 
    
    - CORE CONCEPT: the dot product of user and item factor matricies should approximate the original preferences. And gives a prediction for unseen pairs. 

* Explicit Feedback ALS (star ratings or numerical scores)
    - ALS minimises SSE between observed ratings and predicted ratings. 
    - iteratively adjust the user/item latent factors to narrow the gap between observed ratings and predicted ratings. 
    - Key constraint: only evaluates over observed pairs, so sparse matrix aren't a problem like before. 

* Implicit Feedback ALS (user visits/ viewed products)
    - Model higher confidence with more interactions on a given item for a user. 

* L2 Regularization
    - Penalizes large values in the user/item latent factors
        * Adds the squared magnitutde of every vector to the cost in the loss function
        * Model must balance: fitting observed data, keeping latent vectors from growing too large 
    - Why does this matter on sprase data? 
        - Without regularization, sparse matrix data will overfit to few data and memorizes user/item pairs instead of generalizable patterns. 
        - Lambda (regularization term) hyperparameter: higher, simpler patterns but less fit. Lower, more complex patterns, but risk overfitting 
