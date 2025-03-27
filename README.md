# Face-Detection-Checkpoint-
A face detection checkpoint is a critical component in facial recognition systems. It involves the use of algorithms and models to detect and extract facial features from images or video frames1. The checkpoint ensures that the detected face meets certain criteria before proceeding to further stages, such as recognition or verification. This process helps in accurately identifying and verifying individuals by analyzing facial landmarks, expressions, and other biometric data.
# FACIAl RECOGNITION
# 1. Collect Training Data
This section captures face images from a live video feed for training purposes:

Face Detection: Uses OpenCV's Haar cascade classifier to detect faces in grayscale images.

Data Storage: Creates a dataset directory and saves 100 images per person in a subfolder named after their input name.

Image Processing: Crops and resizes detected faces to a fixed size (100x100 pixels) before saving them.

Visualization: Displays the video feed with a rectangle around detected faces for real-time feedback.

# 2. Train the KNN Model
This section processes the collected data and trains a K-Nearest Neighbors (KNN) classifier:

Dataset Preparation: Loads the stored face images, flattens them into 1D arrays, and associates each image with a label (numerical index representing the person's name).

Model Training: Fits the KNN model using the prepared face image data and corresponding labels.

Model Saving: Serializes (saves) the trained model and the name-label mappings into a .pkl file using Python's pickle module.

# 3. Real-Time Face Recognition
This section performs live face recognition and marks attendance:

Face Detection: Detects faces in a video feed in real time.

Model Prediction: Loads the trained model and predicts the label (and corresponding name) of each detected face.

#Attendance Marking:

Writes the detected person's name, along with the date and time, to an attendance.csv file.

Ensures no duplicate entries for the same person during a single session using a set of already marked names.

Live Display: Annotates the video feed with detected names and bounding boxes around faces.

# Key Features:
Face Data Collection: Efficiently collects and organizes training images.

KNN Classifier: Implements a simple yet effective algorithm for face recognition.

Attendance Tracking: Seamlessly integrates recognition with attendance logging.

Real-Time Processing: Handles real-time video streams and recognition dynamically.

This system provides a solid foundation for applications such as automated attendance systems and basic facial recognition solutions. 
