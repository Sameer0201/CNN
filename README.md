# Convolutional Neural Net

## Shakespeare LSTM

The Shakespeare LSTM can complete sentences which I use here to complete Shakespeare style 14 line sonnets. I am experimenting with this LSTM to analyze the correlation between accuracy and sequence length, batch size, and epochs. I have a collection of models trained under a different set of instructions. They exhibit interesting results.

To run the Shakespeare LSTM download the collection of Shakespeare text and the model. Run the code and change the name of file locations. 
You can experiment with different variations in text generation with trying different inputs in the generate text function. 

Below is a sample sonnet generated by my latest trained model. I started off providing it with the first 3 lines from Shakespear's collection and it autocompleted it to to whole verses. It's intersting to see that it keeps to the structure of a sonnet, i.e. the number of words across and below remains constant. It has learned rhyming, tale - pale - twain. If you read through the poems you will find no difference between the orginal and the machine generated. The only error I can find is that it generates 15 lines instead of 14 lines which is standard for sonnets. 

from off a hill whose concave womb reworded
a plaintful story from a sistering vale,
my spirits to attend this double voice accorded,
and down i laid to list the sad-tuned tale;
ere long espied a fickle maid full pale,
tearing of papers, breaking rings a-twain,
and by their pride and there were shows
the season of the shame that she the sane.
and as the pldasant for his soft past prime,
and swear that pay the world with her disgrace:
in me each pece and thou shalt find thy might?
so of thy beauty thou art bound in shem,
and time to see one white all men a part.
the that my case that sings in thee remain
when they have most whth thine in shaml remain.

'i will not praise that i do can not feel
which thou art blamed in one, one leag put thee,
  and thou shalt find thy might to show her still,
that they whose whoteht is then my love,
you might be buried with a boar display,
and beauty sleep themselves be stain both good,
some in their pride and there where thou art bright,
which in thy stranger eyes from his lips to give,
the scars of painter with a bastard shame:
for since each hand his cheeks and hard no father,
that they where thou wilt should i sostow thee:
then my deeacss of this shalt have thy state'
nor thou of mane, that they had not seen to thee:
  thine be any say that you may be so blld
that thou shalt kete in this alone and thee:

## MINST dataset

MINST is a dataset of handwritten numbers. I Trained a convolutional neural net on a MINST dataset for a 99% accuracy to detect handwritten digits and use a confusion matrix to visualize its performance. This can be used to scan handwritten numbers and translate it into digital format. 

## Dog Breed Detection

I try to determine a dog's breed from its photo by training a CNN using transfer learning technique. This convolutional net can differentiate between 133 different dog breeds with a roughly ~80% accuracy. I adopted two techniques to help the training process. First I use image augmentation to help increase the training size. Here I push the photo through random noise, exposure and flipping it vertically. This increased the data size by X4. 

The second challenge was that the image convolution was taking a long time. One epoch would take over 12 hours due to a large number of computation required by each pixel and the depth of the net. For this, I used transfer learning and the VGG19 model. I used the VGG19 model without the bottleneck to provide me with a bottleneck feature list which I then trained on a smaller net to classify the images.

## Will he default on his credit?

Using credit card default data, I trained a neural net to 80% accuracy to predict if a user would default on his credit card. 

## Quora Duplicate Question Net

This is from a famous competition from Quora who are trying to fix their duplicate question's problem. The dataset consists of 2 questions and the result in binary. The random probability if 50% for predicting duplicity and currently my LSTM can predict with ~70% probability.
