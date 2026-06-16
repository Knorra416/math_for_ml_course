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

* Eigenbasis 
    - 