# FacialEmotionDetector
## Project Details:
1. To Implement a facial Emotion Detector using a Convolutional Neural Network(CNN).
2. To check whether our trained map performs the same or different than the edge detector filter.
## Data preprocessing:
1. While pre-processing I encountered an error while accessing the column names of the test. So I solved it by 
 displaying the column names(actually there is a space to begin the word) and changing it accordingly.
2. Now reshaping pixels into(48,48,1)asmentionedinthepaper.
3. Checking whether there are all categories in the training data.
4. Checkingwhethertheimagesarecorrectwithrespecttotheirlabels.
5. Now convert image labels into one hot encoded vector for further
processing.
6. Normalised the pixel values for better performance of the model.
##Previous and Current Setup:
1. We experimented with different neural network architectures, including a deep neural network (DNN) and Histogram Oriented Gradient features combined with Convolution layer features. Despite efforts to address overfitting using various regularization methods, the test accuracy remained at 50.8% for the DNN and 55.7% for other models due to the abundance of features.
2. In a subsequent approach, we combined a convolutional network with a simple autoencoder (shallow network), which yielded improved results. The autoencoder focused on learning essential feature representations, akin to capturing the top 512 eigenvalues (orthogonal basis), out of the total 4608 values, as indicated by the model summary. This contrasted with DNNs, which were found to learn redundant values beyond the necessary information.
##CNN Model:
a. 5 convolution layers to learn the features.
b. ReLU activation function chosen to overcome the saturation neuron effect.
c. BatchNormalization used to give learning rate more freedom
d. Dropoutisusedtounderminetheeffectofoverfitting.
e. Shallow neural network.
##Compilation:
1. Loss Function: Cross-Entropy Loss as it is a multi-class classification problem
2. Optimizer: We chose Adam as it is better than SGD here.
3. Metrics: We choose accuracy as it is one of the primary goals of this project.
## Reguralizaion Methods:
1. Early Stopping to ensure the difference between training and validation set
doesn’t move far away.
2. Decreasing learning rate when metrics stopped moving
3. Data Augmentation for better representation of the data.
4. Used Stratified sampling over random sampling as it ensures each group within the population receives the proper representation within the sample.





