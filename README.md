# Pose-Detection
Human Pose detection
# README for Pose Detection Script

## Overview
This script, pose_detection.py, utilizes YOLOv8's pose estimation model to detect human poses in images. It specifically identifies and marks hand positions while also drawing connections between key body parts. The script generates annotated images, a hands-only visualization, and a JSON file containing detected hand coordinates.

## Features
- Uses YOLOv8 for pose detection.
- Identifies and marks key body points and connections.
- Detects and highlights hand positions (left and right wrists).
- Saves processed images with annotations and hands-only focus.
- Outputs JSON with hand coordinates.

## Requirements
- Python 3.x
- OpenCV (cv2)
- Ultralytics YOLO (ultralytics)
- JSON and OS (built-in Python libraries)

## Installation
1. Install dependencies:
   bash
   pip install opencv-python ultralytics numpy torch
   
2. Ensure that the YOLOv8 model (yolov8n-pose.pt) is present in the working directory.

## Usage
1. Place an image in the working directory.
2. Run the script:
   bash
   python pose_detection.py
   
3. The script will:
   - Detect and annotate keypoints in the image.
   - Create a hands-only version of the image.
   - Save a JSON file with hand coordinates.

## Output Files
- *Annotated Image:* output_<image_name>.jpg
- *Hands-Only Image:* hands_only_<image_name>.jpg
- *JSON File:* hands_coordinates.json (Contains detected hand coordinates)

## Example JSON Output
json
{
    "hands": [
        {
            "imagename": "test_image.jpg",
            "hand1": [150, 200],
            "hand2": [300, 250]
        }
    ]
}


## Notes
- Ensure input images are clear for accurate detection.
- Modify input_image in the script to change the image being processed.

## Author
This script is developed for pose detection and hand-tracking using YOLOv8.
