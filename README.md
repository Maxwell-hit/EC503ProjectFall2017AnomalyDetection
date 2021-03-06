# EC503Project Fall2017 Anomaly Detection
Team members: Lingxiu Ge, Ayako Shimizu, Steven So
## Abstract
Anomaly detection is the process of analyzing a given data  set  and  determining  whether  or  not  an  anomaly -  a  deviation  from  the  standard - exists. These  deviations  determined  from  the  data  sets  are  classified as  outliers  or  anomalies  for  their  unexpected  behavior.   Algorithms  for  detecting  anomalies  have  various practical  applications,   such  as  fraud  detection,   network  intrusion  detection,  and  fraudulent  cellular  calldetection.  In  this  project  we  aim  to  explore  and  comparatively  evaluate  both  supervised  and  unsupervised anomaly detection algorithms.  In particular, we will focus on One-Class Support Vector Machines (OC-SVM) and k-nearest  neighbors  anomaly  detection  for  supervised learning algorithms, and global k-nearest  neighbors  anomaly  detection  for  unsupervised learning algorithms.

## Implementation
We used OCSVM, K-NN and Global K-NN on all five datasets.
- One-class SVM
  - Train with only normals
  - Test with different values of ‘nu’ to find the best ‘nu’
  - Kernel function default RBF
  - Computational time Complexity O(mn)
- K-NN
  - Separate data sets into training and testing datasets
  - Calculate distance between every testing point and every training points
  - Make prediction based on frequency of labels of k-nearest neighbors
  - Computational time Complexity O(n^2)
- Global K-NN
  - Calculate pairwise distance between all points in data set
  - For each point, calculate anomaly score (average distance) to k-nearest neighbors
  - Create threshold for anomaly score to separate data points into normals and anomalies
    - We tried mean+1*std and mean+2*std as thresholds
    - Assumed Normal Distribution
  - Computational time Complexity O(n^2)


## How to run our Project?
- You need MATLAB (Our project is built using MATLAB 2017b).
- Perprocessed datasets are located [here](https://github.com/Lilyxiuxiuxiu/EC503ProjectFall2017AnomalyDetection/tree/master/Datasets/Parsed%20Datasets).
- [K-NN](https://github.com/Lilyxiuxiuxiu/EC503ProjectFall2017AnomalyDetection/tree/master/K-NN) and [Global K-NN](https://github.com/Lilyxiuxiuxiu/EC503ProjectFall2017AnomalyDetection/tree/master/Global%20K-NN) can be run directly with the corresponding datasets.
- For [OCSVM](https://github.com/Lilyxiuxiuxiu/EC503ProjectFall2017AnomalyDetection/tree/master/OCSVM), you need to install [LIBSVM](https://www.csie.ntu.edu.tw/~cjlin/libsvm/) on MATLAB

## Results
<img align="center" src=results.png>



---
### Thanks!
### If you have any questions, feel free to email us at glxlily@bu.edu, shimizu@bu.edu or sbso@bu.edu
