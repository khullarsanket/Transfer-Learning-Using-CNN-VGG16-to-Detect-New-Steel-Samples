# Transfer_Learning_using_VGG16_for_feature_generation_and_image_classification_using_SVM

# INTRODUCTION
This repository implements the concept of transfer learning from a pretrained VGG16. 

## Detailed Idea 
The concept of transfer learning is used. Pretrained wights of the filters in the Convolutinal Neural Network VGG16 are used to obtain feature vector of the input images. The weights for the dense layers are not incorporated.
Five different models are considered. Till each max pooled layer, different features can be extracted. For instance, till the first max pooled layer, the depth of the convolutional layer is 64 filters, thus the number of features that can be obtained from using the CNN (till this layer) from the input images will be 64. So these features can be transfered into an array of 64. If the layers till the second max pool layer is used, the depth of the covolutional layer is 128. Thus the number of features that can be obtained from using the CNN (till this layer) from the input images will be 128.  So these features can be transfered into an array of size 128, and so on. 

Further, these features vectors are used as input in the Support Vector Machine for binary classification of the micrgraph images. As there are 4 (out of all the categories) categories, one-vs-one approach is used to implement SVM. As the SVM is a binary classifer, 6 (4C2) classifiers are trained for each model. For each model the most frequent classifier can be assigned (multilabel classifier).

The one-vs-one and multilabel classifer are also compared using the cross validation error. 

![VGG16](https://user-images.githubusercontent.com/115849836/203476816-7582be1c-ba50-4848-b83a-03feab704648.png)
#### As there are five different max pool layers, there will be five models.


# Problem Statement 
![1](https://user-images.githubusercontent.com/115849836/203477653-487f01f7-0f4a-4681-9fe3-fe2bc9eac2f3.png)
![2](https://user-images.githubusercontent.com/115849836/203477655-d1c89cef-eb94-4eba-9ac2-4ae6b83df418.png)
![3](https://user-images.githubusercontent.com/115849836/203477650-3000bb9a-51de-42d5-933f-df274d4b9ec6.png)

# Resources
The problem statement is taken from the 6th chapter of the book Fundamentals of Pattern Recognition and Machine Learning (Ulisses Braga-Neto) - Question 6.12.
The data set is also available on the writers (Ulisses Braga-Neto) personal website. 

## The link to the data set used in this repository 
https://drive.google.com/file/d/1zmhN_dqoxhOMUPCW0IAWL_7jYU7y0snF/view

The data set is the folder nammed CMU-UHCS_Dataset
