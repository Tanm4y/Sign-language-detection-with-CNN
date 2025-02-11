# Sign-language-detection-with-CNN

This repository features a Python-based application designed to recognize sign language gestures from a live webcam feed. The project leverages deep learning models, OpenCV for real-time video processing, and TensorFlow for classifying gestures. The primary aim is to detect hand gestures instantly and display the corresponding sign labels in real-time.

Features:
Real-Time Gesture Recognition: Detects hand gestures through a live webcam stream.
Deep Learning Integration: Uses a TensorFlow-based model for gesture classification.
Dynamic Hand Cropping: Automatically detects and isolates the hand region in the video feed.
Interactive Display: Presents the live webcam feed with real-time gesture labels overlaid on the screen.
Prerequisites:
Ensure the following dependencies are installed:

Python 3.7 or above
TensorFlow 2.x
OpenCV 4.x
NumPy
cvzone (for hand tracking)
How It Works:
Webcam Feed:
The application captures a live stream from the webcam and displays it on the screen.

Hand Detection:
OpenCV, along with the cvzone.HandTrackingModule, detects the hand within the frame. The bounding box around the hand is dynamically adjusted to focus solely on the hand region.

Gesture Classification:
The cropped hand region is preprocessed, resized, and passed to the TensorFlow model for gesture classification. The model then predicts the gesture and displays the relevant label on the screen.

Result Display:
The application overlays the predicted label and the bounding box on the webcam feed, providing real-time feedback. If no hand is detected, a message like "No Hands Detected" will be displayed.

Model Information:
Model Type: SavedModel format in TensorFlow  

Input Size: 300x300 pixels

Output: Predicted gesture label based on the input image

Limitations:
Best performance is achieved in well-lit environments.
The model may struggle with overlapping or multiple hands in the frame.
The accuracy is contingent on the quality of the training dataset.

Future Enhancements:
Extend support for more sign language gestures.
Improve classification accuracy with a larger and more diverse dataset.
Implement multi-hand detection and classification for more complex scenarios.
Develop a web-based interface for easier deployment and accessibility.
