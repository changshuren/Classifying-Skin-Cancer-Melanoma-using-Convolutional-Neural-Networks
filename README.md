# Melanoma (skin cancer) Prediction using convolutional neural networks (CNN)

## Problem Statement
In this project, a multiclass classification model is used for a custom convolutional neural network using Tensorflow. 
 

#### Problem statement: To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution which can evaluate images and alert the dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:

1. Actinic keratosis
2. Basal cell carcinoma
3. Dermatofibroma
4. Melanoma
5. Nevus
6. Pigmented benign keratosis
7. Seborrheic keratosis
8. Squamous cell carcinoma
9. Vascular lesion
 

NOTE: No pre-trained model with transfer learning is used. All the model building process are based on a custom model.


#### Project Pipeline with detailed procedures: 
- Data Reading/Data Understanding → Defining the path for train and test images 
- Dataset Creation→ Create train & validation dataset from the train directory with a batch size of 32. Also, make sure you resize your images to 180*180.
- Dataset visualisation → Create a code to visualize one instance of all the nine classes present in the dataset 
- Model Building & training : 
    Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
- Choose an appropriate optimiser and loss function for model training
- Train the model for ~20 epochs
- Write your findings after the model fit, see if there is evidence of model overfit or underfit
- Choose an appropriate data augmentation strategy to resolve underfitting/overfitting 
**Model Building & training on the augmented data :**
  - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
  - Choose an appropriate optimiser and loss function for model training
  - Train the model for ~20 epochs
  - Write your findings after the model fit, see if the earlier issue is resolved or not?
**Class distribution: **
  - Examine the current class distribution in the training dataset 
  - Which class has the least number of samples?
  - Which classes dominate the data in terms of the proportionate number of samples?
**Handling class imbalances:** 
  - Rectify class imbalances present in the training dataset with Augmentor library.
**Model Building & training on the rectified class imbalance data:**
  - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
  - Choose an appropriate optimiser and loss function for model training
  - Train the model for ~30 epochs
  - Write your findings after the model fit, see if the issues are resolved or not?
 
## Findings

<div class="alert alert-block alert-danger">
    <span style='font-family:Helvetica'>
        <b>Findings after applying augmentation and dropout strategies and handling the class imbalance issues: </b>
        <ol>
            <li>The plots showed that the accuracy between the training  and validation sets are very close, and the model has  achieved around <b>86%</b> accuracy for the train set and <b>85%</b> accuracy for the validation set.</li>
            <li>As the accuracy of the training set increased dramatically over time, the one of the validation increases significantly up to 85%.</li>
            <li>Given that 30 epochs were processed slowly, as the loss values of training set decreases dramatically, the ones of validation set decreases largely.</li>
            <li>The differences on the values of accuracy are very small between the ones from training and validation indicated <b> there is no evidence of overfitting at all now</b> .</li>
        </ol>
    </span>    
</div>



## Technologies Used
- pandas - 1.3.4
- numpy - 1.20.3
- matplotlib - 3.4.3
- seaborn - 0.11.2
- plotly - 5.8.0
- sklearn - 1.1.2
- statsmodel - 0.13.2
- tensorflow - 2.11.0


<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- Many resrouces below are used during this fun project:
- https://www.geeksforgeeks.org/
- https://seaborn.pydata.org/
- https://plotly.com/
- https://pandas.pydata.org/
- https://learn.upgrad.com/
- https://www.tensorflow.org/

The model training  and applications were done using the Google colab.

## Contact
Created by [@changshuren] - feel free to contact me!

