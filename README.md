# YOLOv7 Object Detection on COCO Dataset

This repository contains the implementation for training and evaluating the YOLOv7 (You Only Look Once version 7) model on the COCO (Common Objects in Context) dataset. YOLOv7 is a state-of-the-art real-time object detection model known for its high accuracy and speed.

## Features

- **Single-Stage Detection**: YOLOv7 processes images in a single pass, directly predicting bounding boxes and class probabilities.
- **High Performance**: Optimized architecture for superior speed and accuracy, suitable for real-time applications.
- **COCO Dataset**: Trained and evaluated on the COCO dataset, which includes 80 object categories with over 200,000 labeled images.

## Installation

1. **Clone the Repository**:

   ```sh
   git clone https://github.com/yourusername/yolov7-coco.git
   cd yolov7-coco

2. **Install Dependencies**:
   ```sh
   pip install -r requirements.txt

## Usage

3. **Training**
   ```sh
   python3 train.py --workers 2 --device 0 --batch-size 16 --data data/coco.yaml --img 512 512 --cfg cfg/training/yolov7.yaml --weights '' --name yolov7 --hyp data/hyp.scratch.p5.yaml --epochs 1

## Evaluation

4. **To evaluate the trained YOLOv7 model, run**:
   ```sh
   python3 test.py --data data/coco.yaml --img 512 --conf 0.001 --batch-size 16 --device 0 --weights runs/train/yolov7/weights/best.pt

## Detection

 5. **To Detect Yolov7 model**
    ```sh
    python3 detect.py --weights yolov7.pt --conf 0.25 --img-size 512 --source /content/work.jpeg


## Results
The model achieves high accuracy on the COCO dataset, making it ideal for applications in autonomous driving, surveillance, and more. Detailed results and model performance metrics can be found in the evaluation output.


## Acknowledgements
- YOLOv7: YOLOv7 GitHub Repository
- COCO Dataset: COCO Dataset Website




