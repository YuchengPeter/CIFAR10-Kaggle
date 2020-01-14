# CIFAR10-Kaggle
Code for Kaggle competition: CIFAR-10

Dataset has 10 classes. All images are 32x32. 

Preprocessing:
I extracted the RGB vector from each image and turned it into a 32x32x3 numpy array.
Then I linked each image's RGB numpy array with its label(which is stored in a csv file)

Defining model:
For this project, I am using tensorflow's conv2D model. Paddling is used to slow down dimensionality reduction as more layers are added. Maxpooling, batch normalization, and dropout layer are also implemented in the model. The model ends with two fully connected layers and one final layer with softmax activation function. 

Result:
The model has over 95% accuracy on training data without the dropout layer and around 91% accuracy with one dropout layer. However, the accuracy on testing data is super low: 74%. Is this overfitting or could this be caused by undesirable train/test split(training data contains insufficient number of samples on some classes which makes the model not fit to recognize those classes.) Next step is to find out the cause of this low accuracy. 
