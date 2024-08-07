# Count-Parked-Cars
 This project uses YOLOv5 for real-time object detection to count the number of cars within a defined polygonal parking area in a video feed. The implementation includes a mouse callback function to dynamically display the coordinates of the mouse pointer on the video frame.
Parking Area Car Counter
This project uses the YOLOv5 object detection model to identify and count cars in a specified area within a video feed. The implementation includes a simple user interface for viewing the real-time count of cars and mouse pointer coordinates.

Overview
The script loads a pre-trained YOLOv5 model and applies it to a video file named parking.mp4. The model detects cars, and the program checks if the detected cars fall within a predefined polygonal area. If a detected car is within the area, it is highlighted, and the count is updated. The program also displays the current mouse coordinates on the frame, which helps in defining or adjusting the area of interest.

Code Breakdown
Model Loading: The YOLOv5 model is loaded using torch.hub.load from the Ultralytics YOLO repository.

Video Capture: The video is read frame-by-frame using OpenCV's cv2.VideoCapture.

Mouse Callback: A callback function POINTS is used to display the coordinates of the mouse pointer on the frame.

Detection and Counting:

For each frame, the YOLOv5 model identifies objects.
The script iterates through detected objects, checks if they are cars, and determines if their center is within the defined polygonal area.
If a car is inside the area, it is counted, and the bounding box is drawn around it.
Output: The resulting frame shows the detected cars, the count of cars within the area, and the mouse coordinates.

Usage
To run the script, simply execute it in a Python environment with the necessary dependencies installed. The video will play, showing real-time detection and counting.

Important Notes
Ensure the video file parking.mp4 is in the same directory as the script.
The predefined area is hardcoded in the script. Modify the area variable to change the detection zone.
