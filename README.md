# Facial-Landmark-Detection

Facial Landmark Detection Documentation
This code utilizes the dlib library and OpenCV (cv2) to perform facial landmark detection on an input image. The facial landmark detection algorithm locates and marks specific points on detected faces, allowing for detailed analysis and manipulation of facial features.

Prerequisites
Python 3.x
dlib library
OpenCV (cv2) library
Ensure that the shape_predictor_68_face_landmarks.dat file, containing the pre-trained shape predictor model, is available in the same directory as the script.

Functionality
The code performs the following steps:

Import the necessary libraries: dlib for facial landmark detection and cv2 for image processing.

Load the shape predictor model using dlib.shape_predictor(). Provide the path to the shape_predictor_68_face_landmarks.dat file.

Load the input image using cv2.imread(). Ensure that the input_image.jpg file is in the same directory as the script.

Convert the image to grayscale using cv2.cvtColor().

Detect faces in the grayscale image using dlib.get_frontal_face_detector(). This function returns a list of rectangles, each representing a detected face.

Iterate over the detected faces using a for loop.

For each face, predict the facial landmarks using the shape predictor model and predictor(). Pass the grayscale image and the face rectangle as arguments.

Iterate over the 68 facial landmarks using a nested for loop.

Extract the x and y coordinates of each facial landmark using landmarks.part(n).x and landmarks.part(n).y.

Draw a circle around each facial landmark using cv2.circle(). Pass the image, the center coordinates (x, y), the radius (2), the color (green), and the thickness (-1 for a filled circle).

Display the output image with the drawn facial landmarks using cv2.imshow(). The window title is set to "Facial Landmark Detection".

Wait for a key press using cv2.waitKey(0) to keep the window open until a key is pressed.

Close all windows using cv2.destroyAllWindows().

Example Usage
To use the facial landmark detection code:

Make sure the required libraries are installed by running pip install dlib opencv-python.

Download the shape_predictor_68_face_landmarks.dat file from a reliable source or train your own model.

Place the shape_predictor_68_face_landmarks.dat file and the input image file (input_image.jpg) in the same directory as the script.

Run the code and observe the output window, which will display the input image with facial landmarks circled.

Limitations
The accuracy and reliability of facial landmark detection depend on the quality and clarity of the input image. Noisy or low-resolution images may yield less accurate results.
The code currently processes a single input image at a time. To perform facial landmark detection on multiple images or in real-time video streams, additional modifications are required.
Dependencies
dlib: Facial landmark detection library
OpenCV (cv2): Image processing library
Resources
dlib: http://dlib.net/
OpenCV: https://opencv.org/
Note: Ensure compliance with the licensing terms and conditions of the shape predictor model file (shape_predictor_68_face_landmarks.dat).
