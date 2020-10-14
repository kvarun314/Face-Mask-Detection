# Face-Mask-Detection

This is Face Mask Image Classifier which basically tells whether the image contains a person wearing a mask or not. Python and its various libraries were used to code. The project is mainly aimed at learning the workflow of Deep Learning Projects and basically to get the hands on experience. 

The dataset used here is from the user chandrikadeb7. 


## Libraries used

* Keras
* cv2
* matplotlib 
* os
* glob
* numpy 
* sklearn

IDE/Environment used: Google Colab

## My experience from this project.

* The flow of this project is basically using **cv2's** Haar Cascade Classfier, which is basically a Face Detector to find the coordinates of the face from the image.
* There are a couple of models available, like **'haarcascade.frontface_default'**,**'haarcasacade_frontface_alt'** and **'haarcascade_frontface_alt2'**. I tested these three classifiers and while testing images of myself, I found that the **'frontface_alt2'** worked best.
* Of course there are flaws. During testing with images from my phone camera, I noticed that the Face Detector detected random objects as a face. (My arm was detected once in a particular image). Maybe a custom face detector would yield more accurate results. Nonetheless, this one did a good job.
* This was created on Google Colab,where webcam can't be used through the **cv2.VideoCapture(0)** function.So without that processing video in real time was not possible.There is a workaround by writing the predictions onto a seperate video file. Which is not really in realtime.  
* Addtionally **cv.imread()** does not work on Google Colab. So I used the patched function which is from google colab itself. (from google.colab.patches import cv_imread)