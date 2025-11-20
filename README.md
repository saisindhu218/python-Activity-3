
# Density-Aware K-Means Clustering  
### A Modified and Improved Version of the Standard K-Means Algorithm

## Overview
This project introduces **Density-Aware K-Means**, a custom enhancement to the traditional K-Means clustering algorithm.  
The goal is to address a major limitation of standard K-Means:  
its **sensitivity to cluster density and imbalance**.

Density-Aware K-Means improves clustering accuracy by adjusting centroid updates using **inverse-density weights**, enabling the algorithm to treat small and sparse clusters fairly.



## Why Standard K-Means Fails
K-Means assumes:
- Clusters have similar density  
- Clusters have similar size  
- Points contribute equally to centroid updates  

Because of this, standard K-Means:
- Pulls centroids toward large dense clusters  
- Fails to detect small sparse groups  
- Produces biased cluster boundaries  

These limitations reduce its performance on real-world datasets.



## Proposed Solution: Density-Aware K-Means
To overcome these issues, this project modifies the centroid update rule.

### Key Idea
After each iteration:
1. Compute **mean intra-cluster distance** (cluster density)  
2. Assign **inverse-density weights**  
3. Update centroids using weighted averages  

This ensures:
- Sparse clusters have more influence  
- Dense clusters do not dominate  
- Centroids settle at more meaningful positions  



## Algorithm Workflow
1. Initialize centroids randomly  
2. Assign each point to closest centroid  
3. Calculate cluster density  
4. Compute inverse-density weights  
5. Update centroids using weighted averages  
6. Repeat until convergence  

This maintains the simplicity of K-Means while solving its weaknesses.



## Features Included in This Implementation
- Full implementation of Density-Aware K-Means class  
- Standard K-Means baseline for comparison  
- Scatter plot visualizations  
- Cluster centroid tables  
- Elbow curve for Density-Aware K-Means  
- Side-by-side comparison with standard K-Means  



## File Structure
```

├── density_aware_kmeans.ipynb     # Main implementation notebook
├── README.md                      # Project documentation
└── data/ (optional)               # Any dataset used for testing

```


## Requirements
Install required dependencies:

```

pip install numpy pandas matplotlib scikit-learn

```



## How to Run
1. Open the Jupyter Notebook:
```

jupyter notebook density_aware_kmeans.ipynb

```

2. Run cells in order to execute:
   - Data loading  
   - Standard K-Means  
   - Density-Aware K-Means  
   - Visual comparison  

3. Use your own dataset or any public dataset (e.g., Mall Customers).


## Results Summary
- Standard K-Means shows centroid bias toward dense clusters  
- Density-Aware K-Means produces more balanced and accurate clusters  
- Cluster boundaries become clearer  
- Small but meaningful groups are preserved  

The performance improvement is especially noticeable on datasets with uneven density.


## Conclusion
Density-Aware K-Means is a simple yet impactful modification to traditional K-Means.  
By incorporating density-based weighting, the algorithm becomes significantly more robust and reliable for real-world clustering tasks.

This project demonstrates that even small enhancements to classical ML models can produce meaningful improvements.


## Author
Rachabattuni Sai Sindhu, Reddy Akkamma Chandana, Sinchana H M 
Master of Computer Applications  
Density-Aware K-Means Mini Project
