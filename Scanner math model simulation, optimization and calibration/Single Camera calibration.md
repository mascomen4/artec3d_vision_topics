To do camera calibration:
1. Be solid in derivation of camera projection matrix
2. Be solid in the derivation of optimization problem for fx,fy,cx,cy
	1. Degenerate configurations chapter 22
3. Be solid in the derivation of optimization problem for distortion parameters p.189

#### Recap
- For one camera we want to know the calibration parameters: fx, fy, cx, cy, distortion parameters
- [x] Derive the camera projection matrix. 
	- *There's still a lot to cover* starting from the page 156 **CCD cameras**
- To find fx,fy,cx,cy you solve the minimization problem Ap = u, where p is the camera projection matrix which is represented as a column.
	- First, go to the Homography computation, then come back here since the homography problem is closely related to finding camera params. 
	-  [x] Do the derivation by hand.  EDIT: Mostly it's just the generalization of Homogeneous case for 3D everything else if the same. Five and a half of points correspondence is needed. 
- To find the distortion parameters you take some number of shots of the static in 3D world object with a checkerboard pattern. 
	- [ ] What is the math behind? 