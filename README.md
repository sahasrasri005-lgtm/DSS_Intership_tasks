# IIITH DSS Internship – Computer Vision using YOLOv8

# Overview

This internship focused on learning the complete workflow of Computer Vision using YOLOv8 and related tools. The internship covered video processing, object detection, segmentation, dataset preparation, annotation, custom model training, and deployment on real-world applications.

The final project developed during this internship is:

# AI Helmet Detection System

A custom-trained YOLOv8-based Computer Vision system capable of detecting helmets in traffic videos using deep learning techniques.

---

# Week 1 – Video Processing using FFmpeg

## Task 1 – Extracting Frames from Video

### Objectives
- Download a short YouTube video
- Extract multiple image frames using FFmpeg

### Tools Used
- FFmpeg
- yt-dlp
- Python

### Work Done
- Downloaded traffic-related YouTube video
- Used FFmpeg to convert video into image frames
- Generated multiple images from video stream

### FFmpeg Command Used

```bash
ffmpeg -i input_video.mp4 frame_%04d.png
```

### Learning Outcomes
- Understanding video decomposition
- Frame extraction pipeline
- Basics of multimedia processing

---

## Task 2 – Reconstructing Video from Frames

### Objectives
- Generate ~1800 images from video
- Reconstruct video at 30 FPS

### Work Done
- Extracted frames at 30 FPS
- Recombined images into video using FFmpeg

### FFmpeg Command Used

```bash
ffmpeg -framerate 30 -i frame_%04d.png output_video.mp4
```

### Learning Outcomes
- Video reconstruction from image sequences
- Understanding frame rate concepts

---

## Task 3 – Adding Audio to Video

### Objectives
- Download royalty-free music
- Clip audio to one minute
- Merge audio with generated video

### Tools Used
- FFmpeg
- Audacity
- Pixabay Audio

### FFmpeg Command Used

```bash
ffmpeg -i output_video.mp4 -i music.mp3 -c:v copy -c:a aac final_video.mp4
```

### Learning Outcomes
- Audio-video synchronization
- Multimedia editing pipeline

---

# Week 2 – YOLOv8 Environment Setup and Pretrained Detection

## Task 1 – Virtual Environment Creation

### Objectives
- Create isolated Python environment

### Tools Used
- Python venv

### Commands Used

```bash
python -m venv venv
```

```bash
venv\Scripts\activate
```

### Learning Outcomes
- Python environment management
- Dependency isolation

---

## Task 2 – Installing Ultralytics YOLOv8

### Objectives
- Install YOLOv8 package

### Command Used

```bash
pip install ultralytics
```

### Learning Outcomes
- Installing AI frameworks
- Package management

---

## Task 3 – Running Pretrained YOLOv8 Detection

### Objectives
- Run object detection using pretrained YOLOv8 model

### Work Done
- Tested pretrained model on sample images/videos
- Generated bounding box detections

### Learning Outcomes
- Understanding object detection
- Using pretrained AI models

---

# Week 3 – Semantic Segmentation

## Task 1 – Semantic Segmentation using YOLOv8

### Objectives
- Perform semantic segmentation
- Generate segmented output videos

### Work Done
- Applied segmentation model on images
- Generated segmented outputs
- Reconstructed segmented videos

### Learning Outcomes
- Pixel-wise object classification
- Semantic understanding of scenes

---

## Task 2 – Stacking Videos using FFmpeg

### Objectives
- Stack raw, detected, and segmented videos

### FFmpeg Command Used

```bash
ffmpeg -i raw.mp4 -i detected.mp4 -i segmented.mp4 \
-filter_complex vstack=inputs=3 stacked.mp4
```

### Learning Outcomes
- Advanced FFmpeg operations
- Comparative visualization

---

# Week 4 – Understanding YOLO Dataset Structure and Annotation

## Task 1 – Exploring YOLO Dataset Configuration

### Objectives
- Study dataset configuration files
- Understand YOLO metadata

### Files Explored
- data.yaml
- train.txt
- val.txt
- label files

### Key Learnings
- Dataset paths
- Class definitions
- Normalized bounding box coordinates
- Training and validation structure

---

## Task 2 – Labeling Custom Dataset using Label Studio

### Objectives
- Create custom labeled dataset
- Prepare dataset for training

### Tools Used
- Label Studio

### Work Done
- Installed Label Studio in separate virtual environment
- Imported extracted frames
- Created custom annotations
- Exported YOLO-format labels

### Dataset Structure

```text
helmet_dataset/
│
├── images/
│   ├── train/
│   ├── val/
│   └── test/
│
├── labels/
│   ├── train/
│   └── val/
│
├── data.yaml
├── train.txt
└── val.txt
```

### Learning Outcomes
- Dataset annotation workflow
- Importance of high-quality labels
- YOLO label formatting

---

# Week 5 – Custom YOLOv8 Helmet Detection Project

## Project Title
# AI Helmet Detection System

---

## Objectives
- Train custom YOLOv8 model
- Detect helmets in traffic videos
- Generate real-time AI detection outputs

---

## Work Done

### Dataset Preparation
- Created custom helmet detection dataset
- Organized train, validation, and test data

### Model Training
- Configured `data.yaml`
- Trained YOLOv8 custom model

### Training Details

- Model: YOLOv8n
- Epochs: 100
- Image Size: 384

### Outputs Generated
- best.pt
- training graphs
- validation metrics
- bounding box predictions

---

## Video Inference

### Work Done
- Ran trained model on traffic videos
- Generated helmet detection outputs
- Added background music
- Created final demo video

### Final Features
- Real-time helmet detection
- Bounding box visualization
- Video-based AI inference
- Multimedia presentation

---

# Technologies Used

- Python
- YOLOv8
- OpenCV
- FFmpeg
- Label Studio
- Git
- GitHub
- Audacity

---

# Key Learning Outcomes

Through this internship, I learned:

- Video processing using FFmpeg
- Object detection using YOLOv8
- Semantic segmentation
- Dataset preparation and annotation
- Training custom AI models
- Bounding box labeling
- Real-world Computer Vision workflows
- GitHub project management
- Multimedia AI deployment

---

# Future Improvements

Future extensions of this project may include:

- No-helmet detection
- Vehicle counting
- Traffic monitoring system
- Smart surveillance
- Real-time webcam detection
- Multi-class road safety analysis

---

# Final Conclusion

This internship provided practical exposure to real-world Computer Vision workflows using YOLOv8 and related multimedia tools. The final AI Helmet Detection System demonstrates the application of deep learning for intelligent traffic safety monitoring and custom object detection.

The project successfully integrates:
- Video processing
- Dataset creation
- Annotation
- Deep learning model training
- AI inference
- Multimedia presentation

This internship significantly improved my understanding of AI, Computer Vision, and real-world deployment workflows.
