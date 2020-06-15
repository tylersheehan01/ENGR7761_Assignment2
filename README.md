# ENGR7761_Assignment2 - BOVW using SIFT descriptors to train a SVM for detecting cars in a carpark 
The algorithm is developed in python. The following process using the previously described components are implemented in the python programming environment and utilised in the following manner. 

1.	Gather a set of training images:
a.	positive images (cars) 
b.	negative images (not cars)

2.	Extract SIFT keypoints and compute the descriptors, for all the training images.

3.	Cluster all the descriptors to create a codebook or dictionary of visual words

4.	With respect to each individual image in each class, create a histogram of features with respect to the codebook generated in step 3).

5.	The histograms of the positive and negative samples are labelled 1 for positive and -1 for negative.

6.	A sliding window is applied to the test image, at each window SVM is used to predict the class of the subsection of image. A bounding box is draw if a positive sample is found.

7.	Non-maximum suppression is used to reduce the number of instances of boxes drawn. And count the number of cars



* Requires OpenCV contribution version (OpenCV on Wheels)
    * New versions of OpenCV contrib do not have SIFT
    * The following commands are required 
      * pip install opencv-python==3.4.2.16
      * pip install opencv-contrib-python==3.4.2.16
      * may need to use this instead
      * pip install opencv-contrib-python==3.4.2.16 --user
