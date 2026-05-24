# Week 2 – YOLOv8 Setup and Object Detection

## Overview
In Week 2, a Python virtual environment was created and the Ultralytics YOLOv8 package was installed to perform pretrained object detection.

---

## Tasks Completed

### 1. Created Virtual Environment

```bash
python -m venv venv
```

### 2. Activated Virtual Environment

```bash
venv\Scripts\activate
```

### 3. Installed YOLOv8

```bash
pip install ultralytics
```

### 4. Performed Object Detection

```bash
yolo task=detect mode=predict model=yolov8n.pt source="image.jpg"
```

---

## Learning Outcomes

- Python virtual environment setup
- Installing AI frameworks
- Running pretrained YOLOv8 models
- Understanding object detection workflow

---

## Technologies Used

- Python
- YOLOv8
- Ultralytics
- OpenCV

---

## Conclusion

Week 2 provided practical experience in setting up an AI environment and running pretrained object detection using YOLOv8.
