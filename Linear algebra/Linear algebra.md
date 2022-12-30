
- [x] How do you compute matrix inverse? 
	- Gaussian elimination
	- Factorization methods
- [x] How do you find the solution of $A\rm{x}=0$?
	- Make the matrix upper-triangular and do the back-substitution
	- To make it upper-triangular you can use basically any factorization method
- [x] What is pivoting (Gaussian-Jordan elimination)
	- It's an interchange of the marix rows (columns)
		- [x] How do you automatrically select and interchange rows (cols)? 
			- **Partial pivoting** suggests that you find the biggest element in the row of the pivot you are currently considering, and interchange that row with the current row. 
- [x] How do you make the matrix squared? You just multiply it by itself ...

--- 
### LU Decomposition (Ref to Numerical Recipes)
Crout's algorithm is used (basically a special order of evaluation of the equations which desribe the multiplication. It goes from top to bottom iteratively from first column to the last one: first computings $b$ and then $a$, since $b$ are the upper triangular and $a$ are lower-triangular.
- Why do we choose $\alpha$ diagonals to be zero? 
- How is pivoting performed in LU decomposition
- What is better to rotate: rows or cols? 
- Can LU decomposition be applied to non-square matrices?
---
#### SVD Decomposition algorithms

##### Not stable algorithm:
- Remember that SVD is related to EVD in the form: $A^TA=V \Sigma^T \Sigma V^T$ so $V$ here are the eigenvectors of $A^TA$ related to the eigenvalues in $\Sigma^T \Sigma$
- We can compute the eigenvalue decomposition of $A^TA=V \Lambda V^T$, find 

##### Stable algorithm:
- TODO: your observations here

---
####  Eigenvalue decomposition algorithms
- *Algebraic multiplicity* - number multiplicity of an eigenvalue as a multiplicity of a root of characteristic polynomial
- *Geometric multiplicity* - the number of linear independent eigenvectors which correspond to an eigenvalue
- *Hessenberg matrix* - the matrix with zeros below it's first subdiagonal. 
- *Defective matrix* - is the matrix which doesn't have a complete basis of eigenvectors. If a matrix $A$ is of size $n \times n$, but the number of unique eigenvectors is less than $n$, the matrix $A$ is *defective*. 
	- In terms of multiplicity: if the *algebraic multiplicity* exceeds the number of *geometric multiplicity* for an eigenvalue $\lambda$ the matrix is *defective*


- Note: every matrix has at least one eigenvalue
- Two matrices are similiar if there's exist a similarity transformation between them: $B=X^{-1}AX$. Eigenvalues, geometric and algebraic multiplicities and characteristic polynomial are the same for the similar matrices
- Defective matrices are not diagonalizable i.e. they don't have the EVD.
- Determinant/trace of a matrix is simply the multiplication/summation of it's eigenvalues

##### Householder triangularization



##### Phase 1. Reduction to Hessenberg matrix

##### Phase 2. Power iteration, Inverse iteration

##### Other algorithms
- Jacobi algorithm [[Jacobi's method]]
- Bisection
- Divide-and-Conquer
