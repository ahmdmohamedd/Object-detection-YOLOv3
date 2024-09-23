YOLOv3 Object Detection

This repository demonstrates object detection using the YOLOv3 (You Only Look Once) model with COCO dataset labels. YOLOv3 is a fast and accurate object detection algorithm that can identify multiple objects in an image or video in real-time.

## Features

- Uses **YOLOv3** for object detection.
- Detects objects from the **COCO dataset** which includes 80 classes like person, car, dog, etc.
- Supports image and video inputs for detection.
- Outputs annotated images or videos with detected objects and confidence scores.

## Technologies Used

- Python 3.x
- OpenCV
- YOLOv3 (Darknet framework)
- COCO dataset

## How It Works

YOLOv3 breaks an input image into grids and predicts bounding boxes, class probabilities, and confidence scores for each grid. It detects multiple objects of different classes in an image using a single forward pass through the network, making it very efficient.

1. **Pre-trained Model**: We use a pre-trained YOLOv3 model trained on the COCO dataset, which can detect 80 different objects.
2. **Input Data**: The system accepts both images and videos as input and runs object detection on each frame in the case of videos.
3. **Output**: The detected objects are highlighted with bounding boxes, and the class name along with the confidence score is displayed for each detected object.

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/yolov3-object-detection.git
    cd yolov3-object-detection
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Download the pre-trained YOLOv3 weights:

    ```bash
    wget https://pjreddie.com/media/files/yolov3.weights
    ```

4. Ensure the following files are in your project directory:

    - `yolov3.cfg`: YOLOv3 model configuration file.
    - `yolov3.weights`: Pre-trained weights for YOLOv3.
    - `coco.names`: List of 80 COCO dataset object class names.

## Usage

1. **Object Detection on Images**:

    Run the object detection on a single image.

    ```bash
    python detect.py --image images/sample.jpg
    ```

2. **Object Detection on Videos**:

    Run the object detection on a video file.

    ```bash
    python detect.py --video videos/sample.mp4
    ```

3. **Live Object Detection Using Webcam**:

    Perform real-time object detection using your webcam.

    ```bash
    python detect.py --webcam
    ```

### Example Output

- The output will display bounding boxes around detected objects in the image or video with labels such as:
  - "person: 98%" 
  - "car: 89%"

## File Structure

```bash
yolov3-object-detection/
│
├── detect.py            # Main detection script
├── yolov3.cfg           # YOLOv3 configuration file
├── yolov3.weights       # Pre-trained YOLOv3 weights
├── coco.names           # COCO dataset labels (80 object classes)
├── images/              # Directory to store sample images
├── videos/              # Directory to store sample videos
├── output/              # Directory to save output images/videos with detections
├── requirements.txt     # List of dependencies
└── README.md            # Project documentation
```

## Arguments

- `--image`: Path to the input image.
- `--video`: Path to the input video.
- `--webcam`: Use webcam for live detection.

## How to Run

1. For an image:

    ```bash
    python detect.py --image path_to_image
    ```

2. For a video:

    ```bash
    python detect.py --video path_to_video
    ```

3. For real-time detection with a webcam:

    ```bash
    python detect.py --webcam
    ```

## Results

- **Annotated Images**: The output images will be saved in the `output/` folder with bounding boxes around detected objects.
- **Annotated Videos**: The output video will have bounding boxes and be saved in the `output/` folder.

## COCO Dataset Classes

This project uses the COCO dataset, which includes 80 classes like:

- person
- car
- dog
- bicycle
- chair
- etc.

For the full list, check the `coco.names` file in the repository.

## How to Contribute

Contributions are welcome! If you'd like to improve this project:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit the changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a Pull Request.
