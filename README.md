# People Counter

This project is a people counter that utilizes video analysis and object detection to count the number of people in a given video. It can be used for various applications, such as monitoring crowd density, analyzing foot traffic, or estimating occupancy in public spaces.

## Features

- Real-time people counting using video analysis
- Object detection with YOLO (You Only Look Once) algorithm
- Object tracking with SORT (Simple Online and Realtime Tracking) algorithm
- Visualizations of counting lines and tracked objects
- Integration with Google Colab for easy setup and execution



## Prerequisites

- Python 3.x
- Google Colab
- Libraries: ultralytics, cvzone, opencv-python-headless, google-colab, filterpy, scikit-image, lap

## Usage

1. Clone the repository and navigate to the project directory.
```
git clone https://github.com/jakubpiwowarski/car_counter.git
cd car-counter
```
2. Download the necessary files, such as the YOLO model and the video file, and place them in the appropriate directories.
- YOLO model:
  - Store the YOLO model file at `/content/drive/MyDrive/101 - Object Detection /Pliki z kursu/yolov8n.pt`.
- Video file:
  - Store the video file at `/content/drive/MyDrive/101 - Object Detection /Pliki z kursu/Videos/people.mp4`.
3. Run the main script to start counting cars in the video.
```
python people_counter.py
```
4. The script will display the processed video with bounding boxes around people and person count information.

## Description

The main script, `people_counter.py`, performs the following steps:

1. Sets up the necessary dependencies and imports libraries.
2. Mounts Google Drive to access the required files.
3. Loads the YOLO model for object detection.
4. Defines the class names for detection.
5. Loads the mask image for the region of interest.
6. Initializes the object tracker.
7. Opens the video file for processing.
8. Processes each frame of the video:
- Applies the mask to the frame.
- Performs object detection using the YOLO model.
- Filters the detections to include only cars, trucks, buses, and motorbikes with confidence above a certain threshold.
- Updates the object tracker with the filtered detections.
- Draws bounding boxes around the tracked objects.
- Displays the processed frame with car count information.
9. Exits when the video processing is complete.

## Results

The script utilizes object detection and tracking techniques to count the number of person in a video. The processed video is displayed with bounding boxes around the people and the person count information. The script also draws a line indicating a specific region of interest.

## License

This project is licensed under the MIT License.

## Acknowledgments

This project is inspired by the "Project 2 - People Counter" from the "101 - Object Detection" course.

Please note that this README file assumes the repository structure and file locations based on the provided code. Adjustments may be needed if the structure or file locations differ.
