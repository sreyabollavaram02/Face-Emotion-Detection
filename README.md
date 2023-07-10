# Face-Emotion-Detection
Introduction
This project aims to classify the emotion on a person's face into one of seven categories, using deep convolutional neural networks. The model is trained on the FER-2013 dataset which was published on International Conference on Machine Learning (ICML). This dataset consists of 35887 grayscale, 48x48 sized face images with seven emotions - angry, disgusted, fearful, happy, neutral, sad and surprised.
##Basic Usage
First, clone the repository and enter the folder
Download the FER-2013 dataset inside the src folder.
If you want to train this model, use:

cd src
python emotions.py --mode train
#If you want to view the predictions without training again, you can download the pre-trained model from here and then run:
cd src
python emotions.py --mode display
The folder structure is of the form:
src:

data (folder)
emotions.py (file)
haarcascade_frontalface_default.xml (file)
model.h5 (file)
#
First, the haar cascade method is used to detect faces in each frame of the webcam feed.

The region of image containing the face is resized to 48x48 and is passed as input to the CNN.

The network outputs a list of softmax scores for the seven classes of emotions.

The emotion with maximum score is displayed on the screen.
