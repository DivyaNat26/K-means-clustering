# Clustering Handwritten Digits into the different classes-K means

Write java code to perform k-means clustering using MapReduce. The program must take 4 inputs in this order: k, n, full path to input directory, full path to output directory. k is the number of clusters and n is the dimensionality of the data points.
When your program is run it should process all of the data files in the input directory which will contain one line per input point with each value delimited by a single space and terminated by a newline. There will be no blank lines in the input files. For example, if the input points are 4-dimensional, a file may look like this:
0.1 12.2 3.4 1.1
0.78 -14.2 800.9 12.0
An excellent test file is the MNIST data (without class labels) that you used for the previous homework. In fact, that will be one of our test cases.
The initial centroids should be
 <i, ..., i> 
for values of i from 1 to k. For example, if the data points are 4-dimensional and k = 3, the initial centroids would be:
<1, 1, 1, 1>
<2, 2, 2, 2>
<3, 3, 3, 3>
This ensures that everyone (assuming a correct implemetation) will get the same output for the same input.
The output of the reducers should be the cluster centroids.
It is perfectly OK for the mappers and reduces to open and read from files to load side information.
Note that you'll implement one round of k-means in MapReduce and will thus need to wrap it in a little logic that iterates until cluster centroids don't change on two successive iterations.

Data Set http://yann.lecun.com/exdb/mnist/

