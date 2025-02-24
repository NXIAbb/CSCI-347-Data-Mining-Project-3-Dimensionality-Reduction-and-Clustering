Download Link :https://programming.engineering/product/csci-347-data-mining-project-3-dimensionality-reduction-and-clustering/


# CSCI-347-Data-Mining-Project-3-Dimensionality-Reduction-and-Clustering
CSCI 347: Data Mining Project 3: Dimensionality Reduction and Clustering
Turn in the CODE in D2L and PDF report in Gradescope.

Your code, especially Part 2, will be tested. Make sure it follows the template posted on d2l (assignment section) for naming your functions and parameters each function takes. If your code is missing, has errors, or doesn’t follow the template, it will be marked as “failed to be tested” and points will be deducted without the opportunity for reconsideration.

Ensure that your code is well-commented to facilitate understanding of the methods used to generate your results.

The full names of all members should be included in the first page of the report as well as name of the file (it can include only last names).

The team size must be between 2-4 members.

Each team is required to submit their report and code only once per team, and the same team member should submit on both D2L and GradeScope platforms. Multiple submission by same person is allowed.

The submission on GradeScope will be the primary document for grading purposes.

To clarify individual contributions, please prefix your initials before each question (or part) to indicate who worked on each problem.

Please be aware of the following points, as failure to comply will result in a deduction of points:

teams with fewer than 2 or more than 4 members.

Missing partners name on either the report or file name

Multiple submissions by the same team, even if identical.

Different versions of the report submitted by various team members

If your report does not include the necessary code

If your code fails the testing (refer to b)

Reports that are disorganized, unreadable, or contain excessive unrelated code

Missing initials for each question.

Choose a data set that you are interested in from the UCI Machine Learning Repository that has at least 5 numerical attributes, and that you believe may contain clusters. Only use the numerical attributes for this project. Note: if you are planning to complete the extra credit portion of this project, you will need to use a data set that has class labels (ground truth cluster labels), i.e., a classification data set, in order to compute the accuracy of the clustering. If you would like to use a data set from a diﬀerent source, please discuss this with me.

Part 1: Think about the data Answer

the following questions:

[1 point] Why are you interested in this data set?

[1 point] How many numerical attributes and categorical attributes are there in the data set?

[1 point] Are there any missing values? If there are missing values, how are you planning to handle these (will all data instances with missing values be removed? Will all attributes with missing values be removed? Will missing values be imputed? If so, how?)

Before doing any analysis, answer the following questions:

[1 point] Why do you expect clusters to be present in the data?

[1 point] Why might finding clusters in this data set be helpful (how might this help us understand or analyze the data)?

[1 point] How many clusters do you expect to see in the data? Provide a range of values to answer this question. For example, 2 to 4. Why do you expect a number of clusters in this range?

[1 point] Do you expect that the clusters will be of similar size (i.e., cluster 1 is about the same size as cluster 2, is about the same size as cluster 3, etc..)? Why or why not?

Part 2: Write functions for graph analysis in Python

Write the following functions in Python. You may use scikit- learn or other packages to check the correctness of your implementation, but you may not use any existing clustering algorithm implementation in your code. Also test cases provided to test your functions.

[10 points] A function that implements the k-means clustering algorithm. The function should take a data matrix, a number of clusters k, and a convergence parameter epsilon, as input, and return the representatives (means) as well as the clusters found using k- means. If the distance is the same between a point and more than one representative (mean), then assign the point to the mean corresponding to the cluster with the lowest index.

[10 points] A function that implements the DBSCAN clustering algorithm. The function should take a data matrix and the parameters minpts and epsilon as input, and return the clusters found using DBSCAN, where each data point is labeled as either a noise point, a border point, or a core point.


Extra credit (5 points): A function that computes the precision of a clustering. The function should take a list of true cluster labels and a list of the cluster labels returned by some clustering algorithm, and return the precision of the clustering.

Part 3: Analyze your data

Report the following, using tables or figures as appropriate. You may use scikit-learn’s implementation of k-means and DBSCAN, but you are encouraged to first try using your own implementations on real-world data.

[4 points] Use sklearn’s PCA implementation to linearly transform the data to two dimensions.

Create a scatter plot of the data, with the x-axis corresponding to coordinates of the data along the first principal component, and the y-axis corresponding to coordinates of the data along the second principal component. Does it look like there are clusters in these two dimensions? If so, how many would you say there are?

[3 points] Use sklearn’s PCA implementation to linearly transform the data, without specifying the number of components to use. Create a plot with r, the number of components (i.e., dimensionality), on the x-axis, and f(r), the fraction of total variance captured in the first r principal components, on the y-axis. Based on this plot, choose a number of principal components to reduce the dimensionality of the data. Report how many principal components will be used as well as the faction of total variance captured using this many components.

[5 points] For both the original and the reduced-dimensionality data obtained using PCA in question 9, do the following: Experiment with a range of values for the number of clusters, k, that you pass as input to the k-means function, to find clusters in the chosen data set. Use at least 5 diﬀerent values of k. For each value of k, report the value of the objective function for that choice of k.

[5 points] For both the original and the reduced-dimensionality data obtained using PCA in question 9, do the following: Experiment with a range of values for the mints and epsilon input parameters to the DBSCAN function to find clusters in the chosen data set. First keep epsilon fixed and try out a range of diﬀerent values for minpts. Then keep minpts fixed, and try a range of values for epsilon. Use at least 5 values of epsilon and at least 5 values of minpts. Report the number of clusters found for each (minpts, epsilon) pair tested.

Extra credit (3 points): Create a plot of clustering precision for each value of k used in question 10, each value of epsilon used in question 11, and each value of mints used in question 11, for both the original and reduced-dimensionality data.
