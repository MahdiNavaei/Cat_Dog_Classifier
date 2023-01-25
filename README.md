# Cat_Dog_CNNmodel


In this notobook, I tried to classify Dog and Cat images

Approach
For defining an approach for this dataset, we need to keep few things in mind i.e The data set is small. It only have 697 images(this is total number of images i.e train + test), so it will be better to use transfer learning instead of training a model from scratch. Although, because this is a small data set, we will also have to work on regularizing the transfer learning model so it does not overfit the data.

Data Loading

Step 1 is to load the whole data. So that, this data can be used for data processing, data visualization and model training.
Data Processing

Step 2, Deep learning models cannot accept images with varying sizes. So we need to resize all the images into a fixed size. In this case, the fixed size is 256 by 256 pixels. The image pixels have a value range of 0 to 255. We will normalize the data and change the range to 0 to 1. Although this is a data preprocessing step, we can perform it at the time of loading the image.
Data Visualization

This is the 3rd step. As the name suggests, we plot each image, or we visualize each image from the data set to get a better understanding of the data set and to decide how the model should be builded. In many cases, this step is crucial for deciding the model architecture(A rough estimated of the model structure). This is step also help us to understand the data.
Model Building

Here we will build a simple model on top of multiple backbones, From here, based on the performance, we can decide which backbone is really helping for Cat vs Dog classification.
Model Hypertunning

Based on the results obtained from testing multiple backbones. We will choose the top three(or simply the best one) backbone(s) and perform hyperparameter search using Keras Tuner. This will allow us to get an even better model. Hyperparameters involves Learning Rate, Optimizers, Number of hidden layers, Number of hidden units, and Dropout Rate. These are the hyperparameters which we will tune in this case(your hyperparams may differ).
Model Evaluation

In this step, we will evaluate the models performance on the test data. This is important because we need to make sure that we do not tune the hyperparameters in such a manner that the model overfits the data instead of becoming robust.
Model's Predictions

Just like we did the data visualization, we will this time visualize the model's predictions and hoefully we will derive some conclusion about the model's understanding of the data.




# about dataset:

Over a 1000 images of cats and dogs scraped off of google images. The problem statement is to build a model that can classify between a cat and a dog in an image as accurately as possible.

Image sizes range from roughly 100x100 pixels to 2000x1000 pixels.

Image format is jpeg.




Image Data Link: 
https://drive.google.com/drive/folders/1Qc2zTpK5ZwUdlcipLaP0HNEOheAcBEEC?usp=share_link
