# Convolutional Neural Net

## Shakespeare LSTM

The Shakespeare LSTM can complete sentences which I use here to complete Shakespeare style 14 line sonnets. I am experimenting with this LSTM to analyze the correlation between accuracy and sequence length, batch size, and epochs. I have a collection of models trained under a different set of instructions. They exhibit interesting results.

To run the Shakespeare LSTM download the collection of Shakespeare text and the model. Run the code and change the name of file locations. 
You can experiment with different variations in text generation with trying different inputs in the generate text function. 

## MINST dataset

MINST is a dataset of handwritten numbers. I Trained a convolutional neural net on a MINST dataset for a 99% accuracy to detect handwritten digits and use a confusion matrix to visualize its performance. This can be used to scan handwritten numbers and translate it into digital format. 

## Dog Breed Detection

I try to determine a dog's breed from its photo by training a CNN using transfer learning technique. This convolutional net can differentiate between 133 different dog breeds with a roughly ~80% accuracy. I adopted two techniques to help the training process. First I use image augmentation to help increase the training size. Here I push the photo through random noise, exposure and flipping it vertically. This increased the data size by X4. 

The second challenge was that the image convolution was taking a long time. One epoch would take over 12 hours due to a large number of computation required by each pixel and the depth of the net. For this, I used transfer learning and the VGG19 model. I used the VGG19 model without the bottleneck to provide me with a bottleneck feature list which I then trained on a smaller net to classify the images.

## Will he default on his credit?

Using credit card default data, I trained a neural net to 80% accuracy to predict if a user would default on his credit card. 

## Quora Duplicate Question Net

This is from a famous competition from Quora who are trying to fix their duplicate question's problem. The dataset consists of 2 questions and the result in binary. The random probability if 50% for predicting duplicity and currently my LSTM can predict with ~70% probability.
