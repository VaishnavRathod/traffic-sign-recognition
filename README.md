# Traffic-Sign-Recognition
The give code is a run on Google Colab code for Traffic Sign Recognition using OpenCV, Tensorflow Keras, numpy, pandas, matplotlib librariers.
This code have clone the dataset from the following link https://bitbucket.org/jadslim/german-traffic-signs/src/master/
This code uses an CNN model for training and predicting the traffic signs.
It also contains graphs for comparing the train test validation after the training of the model.
At the end of the code you can save the model by the name "10_Epochs.h5" (You can change it if you want to.)
Image is taken from (https://www.google.com/url?sa=i&url=https%3A%2F%2Fpaperswithcode.com%2Ftask%2Ftraffic-sign-recognition%2Fcodeless%3Fpage%3D2&psig=AOvVaw1XuPfbVvR64cJMyNF29mlz&ust=1647531539807000&source=images&cd=vfe&ved=0CAsQjRxqFwoTCJDluu37yvYCFQAAAAAdAAAAABAK)


<img width="308" alt="Screenshot_2019-11-27_at_20 13 54_uFgzj57" src="https://user-images.githubusercontent.com/90707178/158629342-6548b7bc-2db9-4cb6-bbb8-9952fa0680dd.png">


# Code Explaination
The dataset is cloned from the given link using an API. It is Pickel format so we have imported pickel library for reading the dataset.
Then the dataset is split into train test & validation format considering 'X' as features and 'Y' as labels.
After that the data is preprocessed into the grayscale image and equilizehist is used for better extraction of the features from the images. The images are downsampled into 0 to 1 by dividing every pixel value by 255 float value. Then each array is reshaped.
in next step the images are augmented i.e some images are changed for more variety of images to train the model accurately.
The labels (stored in 'Y') are converted into hot encoded format i.e for each value it is convert into an array of 0's and 1's (eg: [0,0,0,0,........,0,0,0,1] for first label) 
Model is create having an architecture given in the code. (You can modify the architecture for checking for more accuracy).
