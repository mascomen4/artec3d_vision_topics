- Computing eigenvalues from symmetrical matrix
- Make the Jacobi algorithm step by step by hand. 

### Statements
- Tridiagonal matrix is the matrix which has three diagonals: lower, main and the upper one.
- $Av=\lambda v$:  $v$ is right eigenvector, and $uA=ku$: $u$ is left eigenvector
- If you apply Gaussian elimination, you get 2 matrices, multiplication of which gives the original matrix.

### Questions
- [ ] What are "p" and "q" in $P_{pq}$ 
- [ ] What is orthogonal similiarity transformation?
	-  Well, it has a special property: it doesn't change the eigenvalues and is written in form $\Sigma = Z^{-1} A Z$. And the result is 
		- [x] Prove that: $det|Z^{-1}AZ-\lambda I| = det|Z^{-1}(A-\lambda I)Z|=det|Z|det|A-\lambda I| det|Z^{-1}|=det|A-\lambda I|$
		- [ ] If A is symmetric, the eigenvectors are real and orthonormal i. e. $A=A^T=Q \Lambda Q^{-1} = Q \Lambda Q^T$. 
- [x] Changing the diagonal values of a matrix, affects only the stretch of its $range<A>$ or the skew + rotation as well?
	- It's a **rotation**, skew doesn't make sense, since any vector collinear to vector from zero considered the same vector.
- [x] Why to find the eigenvectors, a matrix should be diagonal (not triangular)?
	- Remember the matrix diagonalization with eigenvectors $A=Q \Lambda Q^{-1}$ 
	- So it feels like it's the matter of the algorithm design (and number of steps) that after some number of steps you end up with the upper triangular matrix: $D=V^TAV$, $V$ is not a matrix of eigenvectors here, but still you can find the eigenvalues from $D$ and then find the eigenvectors (hmm.. although I'm sure it's much more efficient if you find this matrix right during the iterations, not solving a new SLE (system of linear equations) ) 
- [x] Ok how do you find the eigenvectors?
- [ ] How come the matrix which is stated in the book with els. $c,s,-s,c$ around center can eliminate 1 off-diagonal element? *Good question. experiment by hand*
- [x] If you are trying to eliminate off-diagonal elemetns, how come you end up with a diagonal matrix ?
	- [x] Can you get a diagonal matrix having zeros in the off-diagonal? ANSWER: No
	- [x] Write a code in C++ using Eigen and if it's going to be successful see how actually the matrix is changed with iterations. (I guess the off-diagonals will get closer to zero, and the diagonal will become a bit bigger, in the same time all of the other els should be approaching to zero)
	- So, it seems that the matrix P is designed in that matter, that by trying to eliminate the off-diagonal elements you're also eliminating the non-diagonal elements, so by the end you actually get a diagonal matrix.
	- [x] What are nondegenerate eigenvalues?
		- Не вырожденные собственные значения, по аналогии с не вырожденной (не сингулярной, у которой дет. != 0) матрицей, те значения, которым соотвествует один и только один собственный вектор. В противном случае, она считается вырожденной 
	- [x] What are sweeps during the Jacobi method?
		- It's a set of ~$n^2$ rotations. Basically one full cycle of rotatios from the first element to the last one.  
	- [x] What does that angles mean?
		- Actually the estimated param $\tau$ is used for rotations (See func. rot in the code, and eqs. 11.1.16, 11.1.17)
 