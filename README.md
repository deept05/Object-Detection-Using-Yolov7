# YOLOv7 Object Detection on Custom Dataset

This repository contains the implementation for training and evaluating the YOLOv7 (You Only Look Once version 7) model on the COCO (Common Objects in Context) dataset. YOLOv7 is a state-of-the-art real-time object detection model known for its high accuracy and speed.

## Features

- **Single-Stage Detection**: YOLOv7 processes images in a single pass, directly predicting bounding boxes and class probabilities.
- **High Performance**: Optimized architecture for superior speed and accuracy, suitable for real-time applications.
-**Custom Dataset**: Trained and evaluated on a custom dataset including four categories: cat, dog and rabbit.
  
## Installation

1. **Clone the Repository**:

   ```sh
   git clone https://github.com/WongKinYiu/yolov7.git
   wget https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7.pt
   cd /content/yolov7

2. **Install Dependencies**:
   ```sh
   pip install -r requirements.txt

## Usage

3. **Training**
   ```sh
   python3 train.py --workers 2 --device 0 --batch-size 16 --data data/custom.yaml --img 512 512 --cfg cfg/training/yolov7.yaml --weights '' --name yolov7 --hyp data/hyp.scratch.p5.yaml --epochs 50


## Evaluation

4. **To evaluate the trained YOLOv7 model, run**:
   ```sh
    python3 test.py --data data/custom_data.yaml --img 512 --batch 16 --conf 0.001 --iou 0.65 --device 0 --weights yolov7.pt --name yolov7_640_val
   
## Detection

 5. **To Detect Yolov7 model**
    ```sh
    python3 detect.py --weights yolov7.pt --conf 0.25 --img-size 640 --source picture.jpg



## Custom Dataset Preparation
#### To use your custom dataset with YOLOv7, follow these steps:
1.Organize your dataset: Structure your dataset in the following format:
 ```sh
dataset/
    images/
        train/
        val/
        test/
    labels/
        train/
        val/
        test/
```
2.Create a custom YAML file (data/custom.yaml):
```sh
train: /path/to/dataset/images/train
val: /path/to/dataset/images/val
test: /path/to/dataset/images/test

nc: 3
names: ['cat', 'dog', 'rabbit']
```

3.Label your data: Ensure each image has a corresponding .txt file with annotations in YOLO format.


## Results
The model achieves high accuracy on the COCO dataset, making it ideal for applications in autonomous driving, surveillance, and more. Detailed results and model performance metrics can be found in the evaluation output.


## Acknowledgements
- YOLOv7: YOLOv7 GitHub Repository
- COCO Dataset: COCO Dataset Website




