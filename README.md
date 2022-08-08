# EMG-Classification
 This is still a work in progress (although is quite advanced). 

 The porpouse is to use the public [EMG Data for gestures dataset](https://archive.ics.uci.edu/ml/datasets/EMG+data+for+gestures) to train a CNN for classification of gestures.
 The dataset contains myographic signals measured in the forearm of 36 different subjects while performing different static hand gestures (6 or 7). The instances are recorded every ms. Due to the fact that not every subject performed the 7-th gesture, only the first 6 are considered.

 The train-val-test data split is made by dividing the subjects instead of the instances, by doing so, we can evaluate the model by its capability of predicting the gesture of new different subjects (with respect to the used for training). This division is done randomly. For training are used 28 subjects, for validation 5 and for testing 3.

 So far we have established that we want to predict the hand gestures, but how exactly? more accurately: What are we predicting?

 As it has been said, every instance is a measure of EMG signals (8) every ms. What we are going to classify are windows of **N** consecutive instances (**N=800** is used) of 8 different signals corresponding to a specific gesture.

WARNING: This project is not finished. All contributions are welcome. 