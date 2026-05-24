# Helmet Detection using YOLOv8

## Project Overview
This project detects helmets using a custom-trained YOLOv8 model.

The model was trained using manually annotated images with Label Studio.

## Features
- Helmet detection
- Bounding box detection
- Custom dataset training
- Video inference support

## Tools Used
- Python
- YOLOv8
- Label Studio
- OpenCV
- Ultralytics

## Dataset Structure

```text
helmet_dataset/
├── images/
├── labels/
├── data.yaml
├── train.txt
└── val.txt
```

## Training

```bash
yolo task=detect mode=train model=yolov8n.pt data=data.yaml epochs=100 imgsz=384
```

## Prediction

```bash
yolo task=detect mode=predict model=best.pt source=video.mp4
```

## Results
The model successfully detects helmets in video streams using custom-trained weights.
