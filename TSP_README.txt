The training data set consists of 1.6M examples. Each example has the 2D coordinates of the n cities and the corresponding Travelling Salesman Problem (TSP) minimum tour to this set of cities (100K examples for each n from 5 to 20).

The data has the following structure: 

- One example per line.
- First we have the 2D coordinates of the points (cities), then the word "output" followed by the TSP tour for these cities.
- We represent the TSP tour by a sequence of natural numbers from 1 to n. Each number of the sequence corresponds to the position in the input set.

For example, the line

x1 y1 x2 y2 x3 y3 x4 y4 x5 y5 output 1 3 4 2 5 1

says that the TSP tour for the five cities with coordinates Pi=(xi,yi) is to start at city 1, and then go to cities 3, 4, 2, 5, in this order, and finally go back to the first city 1.

We use the  following order in our data: 

1) The first element of the output sequence is always 1.

The test set examples are for point sets with 10 elements (cities). 