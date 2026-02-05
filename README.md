# YOLOv8 Object Detection and Tracking

## Overview
This notebook implements real-time object detection and tracking on video using YOLOv8. It detects and tracks pedestrians, cars, motorcycles, buses, and trucks in driving scenarios.

## Features
- YOLOv8 nano model for object detection
- Two tracking algorithms:
  - **ByteTrack**: Fast and lightweight tracking
  - **BOT-SORT**: Optimized algorithm with re-identification
- Outputs video with bounding boxes and object IDs
- Generates CSV file with frame-by-frame tracking data

## Dependencies
- ultralytics
- opencv-python
- numpy

## Installation
```bash
pip install ultralytics opencv-python
```

## Configuration
Modify the following variables in the Config cell:
- `MODEL_NAME`: Path to the YOLO model (default: "yolov8n.pt")
- `VIDEO_PATH`: Path to input video file
- `OUTPUT_VIDEO`: Output video file name
- `OUTPUT_CSV`: Output CSV file name
- `ALLOWED_CLASSES`: Dictionary of object classes to detect

## Usage
1. Configure the video path and output settings in the Config cell
2. Run the desired tracking function:
   - `tracking_1()` for ByteTrack
   - `tracking_2()` for BOT-SORT
3. Press ESC key to stop video processing

## Outputs
- **Video**: Annotated video with bounding boxes and tracking IDs
- **CSV**: Tracking results with columns: frame_id, object_id, class, x1, y1, x2, y2

## Detected Classes
- Pedestrian (Cyan)
- Car (Green)
- Motorcycle (Magenta)
- Bus (Red)
- Truck (Orange)
