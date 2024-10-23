# Object Detection with YOLOv3

This project implements real-time object detection using the YOLOv3 (You Only Look Once) model. YOLOv3 is a state-of-the-art, real-time object detection system that can identify multiple objects in an image with high accuracy. This notebook utilizes OpenCV and the YOLO framework to achieve effective object detection in real-time video streams.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Requirements](#requirements)

## Features

- Real-time object detection using webcam or video files.
- High accuracy in detecting objects from the COCO dataset.
- Easy-to-follow Jupyter Notebook structure.
- Visualizations of detected objects with confidence scores.
- Customizable confidence thresholds for detection.

## Installation

To run this project, you need to have the following installed on your system:

1. **Python 3.x**
2. **OpenCV**: Install OpenCV using pip:
   ```bash
   pip install opencv-python
   ```

3. **NumPy**: Install NumPy using pip:
   ```bash
   pip install numpy
   ```

4. **Jupyter Notebook**: Install Jupyter Notebook using pip:
   ```bash
   pip install jupyter
   ```

5. **Weights and Configuration Files**:
   - Download the YOLOv3 weights from [YOLO website](https://pjreddie.com/darknet/yolo/).
   - Download the YOLOv3 configuration file (`yolov3.cfg`) and COCO dataset names file (`coco.names`) from the YOLO repository.

Place these files in the same directory as your notebook.

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/ahmdmohamedd/Object-detection-YOLOv3.git
   cd Object-detection-YOLOv3
   ```

2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

3. Open the `yolo_object_detection.ipynb` notebook.

4. Run the cells sequentially to initialize the YOLO model and start detecting objects in real-time.

## How It Works

The YOLOv3 object detection model works by dividing the input image into a grid and predicting bounding boxes and class probabilities for each grid cell. The process includes:

- Loading the YOLO model and class labels.
- Setting up video capture from a webcam or video file.
- Processing each frame to detect objects, applying non-maximum suppression to filter out overlapping boxes.
- Drawing bounding boxes and labels on detected objects.

## Requirements

- Python 3.x
- OpenCV
- NumPy
- Jupyter Notebook
