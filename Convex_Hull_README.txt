The training data set consists of 920K examples. Each example has the 2D coordinates of a point set with n elements and the corresponding convex hull to this point set (20K examples for each n from 5 to 50).

The data has the following structure: 

- One example per line.
- First we have the 2D coordinates of the points, then the word "output" followed by the convex hull representation for these points.
- We represent the convex hull of a set {P1,...,Pn} by a sequence of natural numbers from 1 to n. This sequence represents the way we traverse the boundary of the convex hull for the set {P1,...,Pn}.  Each element of the sequence corresponds to the position in the input set.

For example, the line

x1 y1 x2 y2 x3 y3 x4 y4 x5 y5 output 1 4 3 1

says that the convex hull for the point set {P1,...,P5}, where Pi has coordinates (xi,yi) is the set enclosed by the polygon obtained by drawing the edges connecting P1 to P4, P4 to P3, and P3 to P1 (which closes the loop).

We follow two orders in our data: 

1) The first element of the sequence of integers representing the convex hull is always the smallest one in the sequence.
2) We traverse the boundary of the convex hull in the counter-clockwise orientation. 

The test set examples are for point sets with 10 elements. 