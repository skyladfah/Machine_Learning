<h1> Machine Learning Assignment 3 </h1> 

<h2><a href="https://github.com/visualizedata/ml/tree/master/final_assignment_3/option_3">Option 3</a></h2>
<p>Work with data on food contamination to cluster incident descriptions into broader categories.<p>
  
<h2>The specific differences in my modified code</h2>
I added two parameters to the CountVectorizer object:
<ul>
  <li>stop_words='english': To exclude common English stop words, such as "a", "an", "the", "in", "on", "at", etc, as these stop words are not informative and can be safely ignored without affecting the result.</li>
  <li>max_df=0.9: to filter out words that are too common and not informative. I set max_df to 0.9 so that if particular words appear in <b>more than 90%</b> of the documents, they will be excluded from the vocabulary list, since they are likely to be too common and uninformative. In fact, words that appear in <b>fewer than 90%</b> of the documents will be retained in the vocabulary list, as they are more likely to be informative and distinctive.</li>
</ul>
<p>For KMeans, I used clusterVal values of 15, 25, 35, 45, and 55 to evaluate the clustering performance for 5 different numbers of clusters.</p>

<p>I changed the value of <b>n_clusters</b> to i because I am using a loop that iterates over a range of cluster numbers, from 1 up to clusterVal - 1. In each iteration of the loop, a new KMeans object is created with n_clusters set to the current cluster number and that is represented by the loop variable i. By setting n_clusters to i, I can evaluate the clustering performance for multiple numbers of clusters, without having to manually change the value of n_clusters each time.</p>

<p> I also added the <b>distortions</b> to track how the distortion changes as the number of clusters increases. By examining the plot of the number of clusters vs the distortion, I can identify the elbow point and select the optimal number of clusters for your dataset.
    
  
<h2> Plots </h2> 

<h4>Cluster 15</h4>

![image](https://github.com/skyladfah/Machine_Learning/blob/main/final_assignment_3/cluster%2015.png)

<h4>Cluster 25</h4>

![image](https://github.com/skyladfah/Machine_Learning/blob/main/final_assignment_3/cluster%2025.png)

<h4>Cluster 35</h4>

![image](https://github.com/skyladfah/Machine_Learning/blob/main/final_assignment_3/cluster%2035.png)

<h4>Cluster 45</h4>

![image](https://github.com/skyladfah/Machine_Learning/blob/main/final_assignment_3/cluster%2045.png)

<h4>Cluster 55</h4>

![image](https://github.com/skyladfah/Machine_Learning/blob/main/final_assignment_3/cluster%2055.png)

<h2>Conclusion</h2>
    <p> </p>    
