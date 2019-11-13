## Medical Image Segmentation (Computer Vision)


### Introduction 

Many diagnostic applications critically depend on the successful localization of bone structure

In this project, we have trained a machine learning model (a convolutional neural network called U-Net) to perform bone segmentation on 3D knee magnetic resonance imaging (MRI). 

The goal is to develop a method that can automatically detect the bone area(Tibia bone) from a knee MRI image

### Method

The deep learning used in this project is U-net.

The U-Net is a convolutional neural network that was developed for biomedical image segmentation.

The network is based on the fully convolutional network [2] and its architecture was modified and extended to work with fewer training images and to yield more precise segmentations. 

Segmentation of a 512*512 image takes less than a second on a recent GPU.

![image](https://user-images.githubusercontent.com/43874699/68726609-01b09280-0590-11ea-9556-013d007acd4c.png)


For preparing training , Validation and testing data , dataset was divided into three different sets i.e 60% for Training , 20% for validation and 20 % for testing.

Finally we show graphs for training and validation data whereas for testing we showed calculated metrics i.e(loss, dice coef and similarity)

Our dataset contains 44 cases of 3D MRI knee.

Out of 44 cases we allotted 24 cases for training , 10 cases for validation and 10 cases for testing sets.

Each cases include 160 2D images  of Tibia bone. Each images contained segments which border tibia bone. 

In total we had 7040 DICOM images with 6000 mask generated from 44 cases 
     
Figure 3(a) provides an example of DICOM images . For each image we have labeled the tibia bone area as shown in Figure 3(b).Using Matlab code we have generated binary mask for each labeled image as shown in Figure 3(c).Figure 3(d) is U-net segmented image generated using U-net code.

### Results  

The models produces strong dice coefficients particular for 3D-DICOM images , for 29 epochs training set gives around 95 % , validation goes for around 90%.The model took around 2 hours to run all datasets.

Figure 2 plots the graph on training and validation datasets.

The performance of testing dataset in dice coef is 88%.The model prediction is accurate for most cases.

Figure 3(d) shows the example of predicted image after 29 epochs.

![image](https://user-images.githubusercontent.com/43874699/68726628-12610880-0590-11ea-8965-8ddc64a5abe1.png)

![raw](https://user-images.githubusercontent.com/43874699/68726698-53591d00-0590-11ea-855b-2a4aec47dcf1.png)
