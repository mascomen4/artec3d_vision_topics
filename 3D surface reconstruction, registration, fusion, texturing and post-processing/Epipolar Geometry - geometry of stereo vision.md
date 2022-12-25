1. Why is epipolar geometry so good to use? 
2. How to find the distance from the Stereo-Camera to the point? Knowing 2 angles and 1 edge is enough to find the height jf the triangle
![Simple example of epipolar geometry](Epipolar_geometry.png)
1. So, this was a simplification of the things assuming that the centers of the cameras are behind the image planes. How does it look in the real case? Where are actually the $O_L$ and $O_R$ ? And how the things change in this case? 
2. Alright, and what about the case of multiple points? Multiple frames with multiple points?
3. How to find now the transformation from $O_L$ to $O_R$? Well, it's basically a fundamental matrix F

### Понятия:
- Эпиполь - точка пересечения базовой линии с плоскостью изображения 
- Базовая линия - линия соединяющая центры симметрии 
- Эпиполярная линия - линия пересечения эпиполярной плоскости с плоскостью изображения
- Эпиполярная плоскость - плоскость, образуемая базовой линией и точкой интереса Х

---
1. If A is real symmetric matrix, then it's SVD is EVD. prove it
2. If A is real skew-symmetrix matrix, then it's SVD is EVD of form $UBU^T$ where B is block-diagonal matrix (?), and the eigen vectors are purely imaginary. 
