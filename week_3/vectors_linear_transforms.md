### Machine Learning Motivation 


#### Vectors and Their Properties 
* Vector is an array of numbers with one column 
* Vectors can be seen an arrow in space
    * Important parts of vector:
    * Magnitude (size)
    * Direction

* Measure distance with Vector:
    * taxicab distance: follows streets/corners, always same distance between two points regardless of which streets/corners you take. 
    * Pythagorean Theorem SQRT(a^2 + b^2) = c 
    * Both give us distances for size of vectors 
        * L1-norm = |a| + |b| (taxicab distance)
        * L2-norm = SQRT(a^2 + b^2) (helicopter distance)

* Vector Notation 
    * Can be row or column vectors
    * Arrow above them or bold font can also represent vector. 
    * Square bracket for vector can mean part of a matrix. 

* Generalized L1/L2 norm
    * L1-norm
        * ||x||1 = |X1| + |X2| + ... + |Xn|
    * L2-norm
        * ||x|2 = SQRT(x1^2 + x2^2 + ... + xn^2)

#### Vector Operations
* Sum of Vectors
    * Add the coordinates together. v = (1,3) u = (4, 1), u + v = (4+1, 1+3) = (5,4)
* Difference of Vectors
    * Same as adding. v = (1,3) u = (4, 1), u - v = (4-1, 1-3) = (3,-2)

* General definitions
    * Sum: x + y = (x1 + y1 x2 + y2 ... xn + yn)
    * Difference: x - y =  (x1 - y1 x2 - y2 ... xn - yn)

* Distance
    * Distance between vectors? L1 or L2 norm == distance

* Multiply Vector by a Scalar 
    * u = (1, 2), lambda = 3, then lambda * u = (3, 6)
    * same for negative scalar

### The Dot Product
