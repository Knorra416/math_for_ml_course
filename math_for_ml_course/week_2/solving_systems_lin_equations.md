### Solving Systems of Linear Equations

#### Matrix Row Reduction 

* Also called gaussian elimination 
    - Convert matrix to a simplified form

* Row echelon form - 1s on diagonal and 0s underneath diagonal 

#### Row Operations that preserve singularity 
* Can switch the position of two rows 
    - Maintains non-singularity 
    - negative of the original determinant 
* Multiplying a row by a (non-zero) scalar 
    - Determinant is scaled by the scalar
* Add a row to another row 

#### The Rank of a Matrix
* Use of matrix rank: Compressing images - reducing rank

#### The Rank of the a Matrix in general 
* 3 x 3 are evaluated similarly to 2x2 for rank by looking at the new information provided by corresponding equations. 
* Row echelon form is an easier way to identify the rank of a matrix. 

#### Row Echelon Form 
* Steps for Row Echelon Form (2x2):  
    1. Divide each row by left-most coef
    2. Subract the first frow from the second row 
    3. Divide the second row by the leftmost non-zero coef 

* Row Echelon for Singular Matricies 
    * Can't divide by zero after step 2, so that becomes the row echelon form

* All zeroes matrix 
    * Can't do anything, so thats it

* The connection, rank of a matrix is the number of 1s in the diagonal in the row echelon form 

#### Row Echelon Form in General
* Pivots, left most value is non-zero. 
* Some text books will divide by this value so all are 1s, but isn't necessary. 

#### Reduced Row Echelon Form 
* General Method
    - Turn anything above a pivot value into a zero 
    - 

#### The Gaussian Elimination Algorithm 
* Augmented Matrix - adds constants as column to matrix 
* Can use augmented matrix to solve system of equations 
* Whatever row operations performend to get row echelon form, apply to augmented matrix to solve 

* Gaussian elimination works for singular matrix. If you find row of zeroes, that means singular. 
* If row is zeroes and the constant is also zero, then the system has infinitely many solutions. 
* If row is zeroes and the constant is non-zero, then the system has no zolutions
* Gaussian Elimination - Summary
    * Create the augmented matrix 
    * Get the matrix into reduced row echelon form
    * complete back substitution
    * Stop if you encounter a row of zeroes 





