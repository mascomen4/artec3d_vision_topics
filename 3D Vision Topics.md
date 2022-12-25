[[3D Scanner prototyping]]
[[Scanner math model simulation, optimization and calibration]]
[[3D surface reconstruction, registration (tracking), fusion, texturing, and post-processing]]
[[6DOF robot control automation. Path planning, collision avoidance, etc.]]
[[Automation of QA routines]]
[[Effective C++ essential ideas.]]

- What the kind of RANSAC Anton has been talking about during the interview? And what was its application to the Computer Vision?

## Statements
1. Understanding the computing of the fundamental matrix is one of the crucial basics for Scanner design
2. The understanding of an n-view geometry is also necessary to place a job at Artec3D
3. Numerical methods involved in the computing of characterisitics is a must-have basic. **Really important**
4. Understanding the C++ language as a tool and knowing how to use it efficiently. Writing consice programs in modern language, according to the industry golden standards. Being able to make robust, reliable, efficient and beatufil design choices. 
5. You also need to know the basics of Statistics and Probability
6. The understanding of robot control: path planning, collision avoidance, localization, robot moving (*continue the list here*)

## Questions
#### Having to build a good sensor software, what do you need to know? 
1. How to reconstruct the points from n-views? 
	1. How to filter the points
	2. How to localize a sensor?
2. How to reconstruct the surface from n-views? 
	1. First of all, how do you create a surface from a scan? 
	2. How to make surface-registration: merge surfaces you got from previous steps? 
	3. How to make surface texturing? (Ref.: Multiple-View Geometry)
3. How to perform a post-processing? (Ref.: Multiple-view geometry)
4. How to calibrate a sensor?
	1. How to do one-camera calibration
	2. How to do multiple-camera calibration
	3. How to do multiple-camera with IMU calibration
5. How to write the C++ code for everything you've mentioned <- *until here you can go sequentially* 
	1. How to perform the automation of QA routines
	2. How to optimize the software for each specific scanner? So it runs faster
6. How to make scanner math model simulation, optimization and calibration? 
	1. How to find things which can be optimized? 
	2. How to understand that the found calibration parameters are good? 
	4. How to create simulation of a scanner mathematical model? 
	5. How to create a scanner mathematical model itself? 
7. How to perfrom the scanner prototyping? 
8. How to perform robot control?
	1. Path planning
		1. A* algorithm
	2. Collision avoidance
	3. Localization
	4. Robot moving

## Learning plan
#### Important skills acquired by day-by-day learning
1. Linear Algebra
2. C++ 
3. Probability
#### Huge chunks of topics 
- Until *"5. How to write the C++ code"* you are free to go sequentially. 6 and 7 are high-level tasks need to be done after first 5, and 8 can be learnt freely.
- Still you'll have different topics: optimization methods, linear algebra, numerical methods, probability and ... so you just keep track of the progress in the notebooks. 