
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