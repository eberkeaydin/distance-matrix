# distance-matrix
Creating distance matrix with random coordinats by C# language.

1) CREATING A DISTANCE MATRIX FROM POINTS IN A 2D PLANE
In this part of the project, we need to generate points and points in 2 dimensional (2D) Euclidean space.
I am asked to perform some calculations on it.
The distance between any two points in 2D Euclidean space is given by the formula
is calculated:

𝑑 = √ (𝑥2 - 𝑥1)^2 + (𝑦2 - 𝑦1)^2

For example, for two point coordinates P1 (1 = 10.5, 𝑦1 = 20.7) and P2 (𝑥2 = 3.1, 𝑦2 = 19.9)
the distance between them will be found as follows:
𝑑 = √ (3.1 - 10.5)^2 + (19.9 - 20.7)^2 ≅ 7.44

a) Random Point Generation: 2-dimensional space given its width (width) and sufficient (height)
I writed n random dots point and return method inside. Points produced nx2
matrix '; its a row a point and its a column is also the primary x and y coordinate
corresponding to their values ​​will be stored and returned. Coordinates to be generated
should be of double type.

Test this method separately with the parameter: Test result returned
Provide the information of the matrix (its x and coordinate information for a point) to the console.
1.n = 10, width = 100, height = 100
2.n = 100, width = 100, height = 100

b) Distance Matrix (DM) Generation: The nx2 points given to it
distance of nxn matrix (Post method jacket in the previous item)
I writed the method that converts and returns the matrix. Distance matrix (DM) for each pair of points
It contains the distance information between. For example, DM [i, j] at points i and j
will give the distance. The distances are symmetrical, dm [i, j] = DM [j, i] equality will be provided.
(The distance from i to j and the distance from j are the same).
Test this method with n = 10, width = 100, height = 100 samples. DM produced
Give it to the console.
