# Face-recognition
FACE DETECTION USING HAAR CASCADE CLASSIFIERS AND LBPH


Haar features
OpenCV's algorithm is currently using the following Haar-like features which are the input to the basic classifiers:
Instead of applying all the 6000 features on a window, group the features into different stages of classifiers and apply one-by-one. (Normally first few stages will contain very less number of features). If a window fails the first stage, discard it. We don't consider remaining features on it. If it passes, apply the second stage of features and continue the process. The window which passes all stages is a face region.

haarcascade_frontalface_default.xml :
OpenCV already contains many pre-trained classifiers for frontal face etc. Those XML file are stored in haarcascade_frontalface_default.xml  


Libraries required: opencv(cv2), numpy, matplotlib
pip install --user opencv-python==4.3.0
pip install --user opencv-contrib-python==4.3.0.36

Histograms:
Trained model object stores histograms of the images in the facial database. It will compare the histogram of the target image with them later.

Face recognition:
We will feed a target image to LBPH model and it looks for it in the facial database. Predict function serves this duty. It returns both confidence score and index in the facial database of the found one.


