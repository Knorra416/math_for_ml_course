### System of Equations Notes

#### Linear Algebra Applied 1 

* Linear regression
    * y = mx + b 
    * m is a weight
    * b is a bias term 
    * Within a training dataset, we know x and y and trying to find weights and bias which fit this data best. 

#### Linear Algebra Applied 2 

* Matrix notation can be used for our linear regression
    * W x Y + b = y-hat

* Plan for the week
    * Common vector and matrix operations 
    * Systems of Linear equations
    * Representing systems as vectors and matrices
    * Computing the determinant of matrices 

#### Check Your Knowledge 
1. Translate the following description into a system of linear equations.  

Bob has a mixture of apples and oranges of the same size, which he split into two bags. The first bag contains 4 apples and 3 oranges and weighs 700g. The second bag contains 2 apples and 6 oranges and weighs 1000g. 

4a + 3o = 700
2a + 6o = 1000

2. Translate the following system of linear equations into the matrix form:

5x+3y+5z=6
7x+2y+8z=17
4x+3z=8

[[5, 3, 5],
[7, 2, 8],
[4, 0, 3]]

[x, y, z]

[6, 17, 8]
​
3. Compute the determinant of the following matrix:

[1, 2, 1
0, 3, 5
4, 3, 8]

I don't remember this 

4. Does the matrix above have any linear dependent row?

I don't remember this 

5. Is the matrix singular or non singular?

I don't remember this 

#### Geometric Notion of Singularity 
* constants in the determinant don't matter when determining if equation is singular or non-singular 

#### Singular vs. Non-Singular Matrices
* Non-singular == unique solution
* matrix would be non-singular matrix 

* singular == no unique solution 
* matrix would be singular matrix 

* easy way to identify singular vs non-singular is to set constants to zeroes and evaluate from there. 

3x + y = 1100
x + 3y = 1050 


#### Linear Dependence and Independence 

* A system of equations is singular if the second equation carries the same information as the first one. 

* For matrix, the second row is a multiple of the first row (rows are linearly dependent on each other).

* For matrix, no row is a multiple of the other one (rows are linearly independent)

* Example
    * a = 1, b = 2, a + b = 3
    * rewritten as: a + 0b+ 0c = 1, 0a + b + 0c = 2, a + b + 0c = 3
    * rows are linearly dependent because from row 1 and row 2, can get row 3 

#### The Determinant

* The determinant is a quick formula to identify singluar/ non-singular matrix. 
* Given a matrix: 
    [a, b,
    d, c]
    ad - bc = 0 
    * if this value is zero then matrix is singular, nonzero otherwise. 

* Diagonals in a large matrix: 
* Given a 3x3 matrix: 
    [a, b, c
     d, e, f
     g, h, i]
    * (a * e * i) + (b * f * g) + (c * d * h) - 
      (c * e * g) + (a * f * h) + (b * d * i)

* Trianglular matrix: everything below the diagonal is zero
    * can still be singular 





