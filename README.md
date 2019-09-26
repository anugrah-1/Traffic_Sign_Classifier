# Traffic Sign Classifier
As traffic signs plays important role while driving, similarly we are going to train a model to do this task.

#Steps
* Load the dataset
* Summarize the dataset
* Design the model
* Train the model on the dataset
* Test the model against the test dataset

#Dataset Summary
* Number of training examples  = 34799
* Number of testing examples   = 12630
* Image data shape             = (32, 32, 3)
* Number of classes            = 43

#Model Architecture
I used LeNet architecture:
>Convolution 1: 32x32x1 -> 28x28x6 -> RELU -> 28x28x6
>Convolution 2: 28x28x6 -> 14x14x10 -> RELU -> 14x14x10
>Convolution 3: 14x14x10 -> 8x8x16 -> RELU -> 8x8x16
>Pooling      : 8x8x16 -> 4x4x16
>Flatten      : 4x4x16 -> 256
>Linear 1     : 256 -> 120 -> RELU -> Dropout -> 120
>linear 2     : 120 -> 100 -> RELU -> Dropout -> 100
>linear 3     : 100 -> 43 -> Output

#Parameters
I used the following parameters:
Epochs        : 100
Batch Size    : 2048
Learning rate : 0.0009

#Results
The model results are as follows:
Training set accuracy   : 0.96
Validation set accuracy : 0.94
Test set accuracy       : 0.93

#Conclusion
Successfully trained model to classify traffic signs from a given image.

Note:
You can train the model with different parameters and can get better or worst results compared to these results.
