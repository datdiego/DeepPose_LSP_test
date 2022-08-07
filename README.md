# DeepPose_LSP_test
Testing Leeds Sports Pose Data set using DeepPose model.

## Study of Sport Pose Classification using Leeds Sports Dataset

<p>One of the main objectives of computer vision is to be able to analyze and interpret visual data correctly. Interpreting human poses in different scenarios has been one of the main challenges in computer vision. This is due to the different amount of joints and limbs that need to be identified in a two dimensional image.

As benchmark Leeds Sports Pose Dataset (LSP) [1] has been used to correctly classify the human body pose dependent of each of the sports represented in the Dataset.  OmniPose [2] (UniPose with WASPv2) and DeepPose [3] classification algorithms will be used to study the different approaches taken and how the technique has evolved in few years

### Abstract
#### The Leeds Sports Pose Dataset</h4>

This dataset contains 2000 pose images gathered from Flickr. The researchers, Johnson and Everingham [1], uploaded 1000 images for training and 1000 images for testing. Each image has an annotated has a corresponding matrix for each of the joints locations. The matrix was uploaded in a MATLAB data file with the dimensions 3x14x2000. The ordering of the joints were as follows:

1. Right ankle
2. Right knee
3. Right hip
4. Left hip
5. Left knee
6. Left ankle
7. Right wrist
8. Right elbow
9. Right shoulder
10. Left shoulder
11. Left elbow
12. Left wrist
13. Neck
14. Head top

The LSP Dataset was introduced in 2010 by Sam Johnson and Mark Everingham from University of Leeds, they also introduced the first method to determine the pose estimation using a pictorial structure model (PSM)[4]. This method was able to demonstrate an accuracy of 55.1% using a Cluster Nonlinear method. This method is a mixture of pose with non-linear classifiers for pose-specific part appearance.

### Deep Pose
Using Deep Neural Networks (DNNs) Google engineers Toshev and Szegedy were able to obtain a higher accuracy in 2014. They introduced a DNN based regression problem towards identifying body joints. They proposed a cascade of DNN-based pose predictors, which would allow the increased precision of the localization of joints. The used the location of each body joint using a 7-layered generic convolutional DNN, then each joint is regressed using the full image.

This method utilizes a 7-layered generic convolutional Deep Neural Network (DNN). The DNN is capable of capturing the full location of each joint, then the joint regressors uses the full image to create an augmented sub image. After each regression the DNN based regressors refines the prediction of the joint location by using the higher resolution sub-images. This model was tested using a single pass DNN. 

