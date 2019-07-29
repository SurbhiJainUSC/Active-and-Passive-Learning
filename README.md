# Active-and-Passive-Learning
The task is classify authentication of banknotes using active learning and passive learning approaches.

## Dataset
The Banknote Authentication dataset contains data extracted from images that were taken for the evaluation of an 
authentication procedure for banknotes. It has 1372 instances and 5 real-valued attributes (variance of Wavelet Transformed 
image, skewness of Wavelet Transformed image, curtosis of Wavelet Transformed image, entropy of image and class). 

## Passive Learning
A Support Vector Machine (SVM) has been trained with a pool of 10 randomly selected data points from the training set using 
linear kernel and L1 penalty. The penalty parameter is selected using 10-fold cross-validation. This process is repeated by 
adding 10 other randomly selected data points to the pool, until all the 900 training points have been used. The test error 
for all 90 SVMs that were trained using 10, 20, 30, ... 900 data points are calculated. This process is repeated 50 times 
(monte-carlo simulation) and test errors are plotted for each simulation.

## Active Learning
A Support Vector Machine (SVM) has been trained with a pool of 10 randomly selected data points from the training set using 
linear kernel and L1 penalty. The penalty parameter is selected using 10-fold cross-validation. Then, 10 training data points 
closest to the hyperplane of the SVM are chosen and added to the pool. This process is repeated until all the 900 training 
data points have been used. The test error for all 90 SVMs that were trained using 10, 20, 30, ... 900 data points are 
calculated. This process is repeated 50 times (monte-carlo simulation) and test errors are plotted for each simulation.
