The training data set consists of 1.8M examples. Each example has the 2D coordinates of a point set with n elements and the corresponding Delaunay triangulation to this point set (400K examples for each n from 5 to 50).

The data has the following structure: 

- One example per line.
- First we have the 2D coordinates of the points, then the word "output" followed by the Delaunay triangulation representation for these points.
- We represent the Delaunay triangulation by sequentially outputting all its triangles. We represent a triangle by a triplet of integers which 
refers to its vertex positions with respect to the input points.
- We have a special token "<ENDT>" between triangles which represents end of a triangle. 

For example, the line

x1 y1 x2 y2 x3 y3 x4 y4 x5 y5 output 3 4 5 <ENDT> 1 3 5 <ENDT> 1 2 3

says that the Delaunay triangulation for the point set {P1,...,P5}, where Pi has coordinates (xi,yi) consists of three triangles which vertices are {P3,P4,P5} , {P1,P3,P5}, and {P1,P2,P3}.

We follow two orders in our data: 

1) The sequence of integers representing a triangle is always increasing.
2) We order the triangles in the Delaunay triangulation by lexicographic order on the 2D incenter coordinates of each triangle. 

The test set examples are for point sets with 10 elements. 