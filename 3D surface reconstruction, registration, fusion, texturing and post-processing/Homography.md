When you're done with homography, go to Camera calibration. [[Single Camera calibration]]
### DLT algorithm
- We want to find the H such that $Hx_i=x'_i$. 
- So, let's take a convinient equation $x'_i \times Hx_i = 0$  
- Let's rewrite: $Hx_i = (h^{_1T}x_i, h^{_2T}x_i, h^{_3T}x_i)^T$, so $h^{_j}$ is simply the row which has column representation.
- And do $[x'_i]_{_\times} (h^{_1T}x_i, h^{_2T}x_i, h^{_3T}x_i)^T]=0$  
- Rewrite it in the matrix form where we put $x_i^T$ in the matrix, and we just leave $h^{_j}$ outside, because we use the fact that $h^{_jT}x_i = x_i^Th^{_j}$ 
- We eliminate the last row, since skew-symmetrc matrix has rank of 2, not 3
- So, we have a $2 \times 9$ matrix for 1 point correspondence, so we write for 4 of them, so we obtain a big matrix A of dims $8 \times 9$ multiplied by the $9 \times 1$ vector $(h^{_1}, h^{_2}, h^{_3})^T$ 
- We get the equation of the form $Ah = 0$, so the rank of the nullspace is 1 here. (If the system is not overdetermined the solution is easy, you can use either LU or QR decomposition and solve for $y$ and then for $x$)
- If the system is overdetermined, shortly the answer is the eigenvector which corresponds to the smallest eigenvalue of $A^TA$ 
- If to be more descriptive: you solve the minimization problem $min(||Ah||)$ with the constraint that $||h||=1$, 1 is arbitrary, you can pick anything, since anyway the $h$ is defined only up-to-scale.
- To find the minimum we find the SVD decomposition and eventually solve $min(||Dy||)$ where $y=V^Th$, taking into account that D is diagonal and has entries in the non-ascending order, the solution naturally comes: $y=(0,0,...,1)^T$ and so $h=Vy$  which is simply the last column of $V$
##### Degenerate configurations


- [ ] Remember to read about the example when the point is at infinity. How do you map then? 
- [ ] Why it would be a problem if you make $h_{33}=1$?