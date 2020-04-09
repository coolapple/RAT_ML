# Handwritten Digitals Classification for Math App



The objective of this handwritten digital classification project is to use single digital images and extract pixel values, to accurately identify 10 digitals for mathematical exercise and tests. We also provide an introduction to applying techniques that involve image-based features. We are going to apply different classification techniques to benchmark the relevance of classifiers in image classification problem. 

RoadMap of the Project:

1.	Data Cleaning and preparation step
   Using R language to import data from AWS MYSQL database. 
   This dataset contains one row for each of the 60000 training instances, and one column for each of the 784 pixels in a 28 x 28 image. Pixel values are between 0 to 255. 
   For each of the 10 digital images, there are roughly 10% of total records. This assures us that row data are evenly distributed among different digital images. 
   
2.	Feature Engineering

   By looking at histogram of pixel values, we found that most pixel values are either complete white (0) or complete dark (255) with little in between. It assures us the further feature engineering of the data without loss of much information. 
   For example: For some specific classification algorithm such as Bernoulli Classification, pixel values have been categorized as either 0 or 1 based on a cutoff pixel value such as 100/127.  

   For other classification algorithms, we take whatever is in the pixel columns. 

3.	Perform EDA on the given dataset and list our findings

   We are very interested in how the average images looks like and how each digitals’ variation from their average image respectively. 
 
   First, I find the mean pixel values for each digital and show their images. 
   Second, we look at the distribution of each digital to understand how each digital can be away from its centroid. We use Euclidian   distance to evaluate the difference. 

4.	Model Selection

   We look at three types of classification algorithms:
   Simple Gaussian classification without feature covariance
   Gaussian classification with feature covariance. 
   Bernoulli classification. 

   Gaussian classification gave us the highest accuracy about 95%. With Bernoulli classification gave us 85% with a little loss of information when doing feature engineering.  

5.	Train/Validation/Test

   we also looked at the impact of train set to evaluate training set size impact on the accuracy of a typical algorithm. With average    accuracy of 94.9% on test set with training set ranging from 10% to 90%. Training set size has immaterial impact on the accuracy of   Gaussian Naïve Bayes classification which confirms the multivariate Gaussian distribution of the pixel features. 

Conclusion:
We achieved average of 95% accuracy with Gaussian Naïve Classification to single digital images.  With 95% accuracy, we are comfortable with the algorithm. 
