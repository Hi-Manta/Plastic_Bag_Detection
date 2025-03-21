# Plastic Bag Detection using YOLOv8

## Overview
This project focuses on detecting plastic bags in images and videos using YOLOv8, a state-of-the-art object detection model. The model is trained to identify plastic bags in various environments to support environmental monitoring and waste management efforts.

## Features
- **Real-time detection**: Uses YOLOv8 for fast and accurate plastic bag detection.
- **Custom dataset**: Trained on a dataset of plastic bags in different conditions.
- **Supports images and videos**: Can process static images as well as real-time video feeds.
- **Easy deployment**: Can be used with Python scripts or integrated into applications.

## Installation
### Prerequisites
Make sure you have Python installed (recommended version: 3.8+). Install the required dependencies:

```bash
pip install ultralytics opencv-python 
```

### Clone the Repository
```bash
git clone https://github.com/Hi-Manta/Plastic_Bag_Detection.git
cd Plastic_Bag_Detection
```

## Usage

### Running Detection on Images
```bash
python predict.py --source path/to/image.jpg --weights best.pt --conf 0.5
```

### Running Detection on Videos
```bash
python detect.py --source path/to/video.mp4 --weights best.pt --conf 0.5
```

## Model Training

If you want to train the model on your own dataset:

1. Prepare the dataset in YOLO format.
2. Modify the `data.yaml` file accordingly.
3. Run the training command:

```bash
python train.py --model yolov8n.pt --data data.yaml --epochs 50 --img 640
```

## Results
After training, the model will generate weights stored in the `runs/train/exp/weights/` directory. Use `best.pt` for inference.

## Acknowledgments
- [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- Open-source datasets for plastic bag detection

