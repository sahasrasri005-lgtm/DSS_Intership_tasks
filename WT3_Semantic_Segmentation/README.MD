# Week 3 – Semantic Segmentation and Video Processing

## Overview
In Week 3, semantic segmentation was performed using YOLOv8 to identify objects at pixel level. Segmented outputs were converted into videos and combined using FFmpeg.

---

## Tasks Completed

### 1. Performed Semantic Segmentation
- Applied YOLOv8 segmentation on images
- Generated segmented outputs with colored masks

### 2. Created Segmented Video
- Converted segmented frames back into video using FFmpeg

### 3. Stacked Videos
- Combined raw, detected, and segmented videos vertically

```bash
ffmpeg -i raw.mp4 -i detect.mp4 -i segment.mp4 -filter_complex vstack=inputs=3 output.mp4
```

### 4. Added Background Music
- Added soundtrack to final output video

---

## Technologies Used

- YOLOv8
- FFmpeg
- Python
- OpenCV

---

## Learning Outcomes

- Semantic segmentation
- Pixel-level object understanding
- Video stacking using FFmpeg
- Multimedia processing

---

## Conclusion

Week 3 introduced semantic segmentation and advanced video processing techniques using YOLOv8 and FFmpeg.
