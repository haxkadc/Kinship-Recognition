# Kinship-Recognition
University Project: Kinship recognition between two images depicting human faces and Kinship type recognition between the same two images.

##
## Description

- Recognition of belonging to the parental class of two individuals through images depicting their faces.
- Recognition of the type of kinship of two individuals through images depicting their faces.
- The combination of the two problems listed above.

##
## Datasets

For the recognition of the existence of kinship, the "RECOGNIZING FACES IN THE WILD" dataset of the Kaggle competition was used (https://www.kaggle.com/competitions/recognizing-faces-in-the-wild/data)

For the training of the recognition of the type of kinship it was chosen to use the KinfaceW dataset (https://www.kinfacew.com/download.html)
The KinFaceW-I and KinFaceW-II databases contain 64x64 pixel images of people in an uncontrolled environment, with no restrictions on pose, lighting, background, and expressions.
As in most previous databases, four types of kinship are considered: father-son (F-S), father-daughter (F-D), mother-son (M-S), and mother-daughter (M-D). 

KinFaceW-II contains 250 pairs for each type of relationship, while KinFaceW-I contains 156, 134, 116, and 127, respectively. 

The main difference between the two datasets lies in the fact that the images of family members in the first come from different photographs, while in the second, in most cases, from the same photograph.

For the Test of trained networks were used the datasets mentioned above and some created ad-hoc for these problems (Dataset Actor and "Dataset Ignoti")

##
## Built with

<img src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue" /> 
<img src="https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252" /> 
<img src="https://img.shields.io/badge/OpenCV-27338e?style=for-the-badge&logo=OpenCV&logoColor=white" /> 
<img src="https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white" /> 
<img src="https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white" /> 
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" /> 
<img src="https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black" />

##
## Architecture

The type of Neural Network used are the Siamese.

Siamese neural networks are models that learn to recognize what makes two inputs similar to each other, as opposed to classification networks, which learn to recognize the characteristics that allow you to associate an input to a given class.


<img width="500" src="https://github.com/haxkadc/Kinship-Recognition/assets/134702013/8d2813be-fb6f-4276-93c9-14e734c532d0"/>

For these reasons it was necessary to use the Siamese Networks in order to calculate the same weights on two different inputs and obtain a prediction as output.

##
## Transfer Learning

Transfer Learning allows you to reuse most of the parameters (weights) of a neural network already trained previously on a problem similar to the one we have to solve, focusing only on the training of the last layers that are usually those dedicated to the classification and / or regression of the features obtained with the previous layers.

In our case, since it is a kinship verification problem, concerning facial analysis, it was decided to use a pre-trained network on a face recognition database as a base-network. In particular, we decided to test the performance on the architecture of the VGG-Face network (VGG-16), pre-trained on the homonymous dataset.

<img width="500" alt="image" src="https://github.com/haxkadc/Kinship-Recognition/assets/134702013/147922f3-e9e2-40b5-9d40-9022ae491723">



##
## Results


|    PUNTATA    |   RISULTATO   |          
| ------------- |:-------------:| 
|     09-03     |     **FD**      
|     10-03     |    MD-MS      |       
|     11-03     |      **MS**       |   
|     16-04     |      **FD**       |    
|     18-04     |      **MD**       | 
|     19-04     |    MD-MS     | 
|     20-04     |      **FS**       | 
|     28-04     |      **FD**       | 
|     01-05     |      **FS**       | 
|     05-05     |      **FS**       | 







