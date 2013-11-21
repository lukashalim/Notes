### More clustering
Often useful to run factor analysis prior to the cluster analysis - see code example

If there are eliptical clusters, CCC will first increase rapidly, then the increase will slow

Irrelevant variables introduce noise into cluster solution

Always mention the size of the segments

If the data you are scoring has a smaller number of variables than the data used to create the clusters, then you should try to use the to-be-scored data to predict the clusters.  Need at least 70% accuracy.

#### SHORT FORM
- subset of the data which you can use to score new data
- should predict original clusters with at least 70% accuracy
- data for variables should be easy to predict
- can be created using discriminant analysis, multinomial logit model, decision trees
