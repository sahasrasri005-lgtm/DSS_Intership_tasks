# DSS_Intership_tasks
# Internship Tasks

## Task 01: Frame Generation
In this task, a sequence of image frames was prepared to be used for video creation.

The frames were generated and organized in a sequential naming format (e.g., frame1.png, frame2.png, ...), ensuring proper ordering during video processing. These frames serve as the input for creating a continuous video in the next task.

### Outcome:
A set of ordered image frames was successfully prepared for video generation.

### Outcome: 
frame181.png
frame2.png
frame522.png

## Task 02: Video Creation from Frames
In this task, a video was generated using a sequence of image frames created in Task 01.

The frames were arranged in sequential order and converted into a video using FFmpeg at a frame rate of 20 frames per second (fps). This ensured smooth playback and proper synchronization of frames.

### Command Used:
ffmpeg -r 20 -i frame%d.png -pix_fmt yuv420p task02_video.mp4

### Outcome:
A video file was successfully created from the input frames, demonstrating the process of frame-to-video conversion using FFmpeg.
### Outcome:
myvideo.mp4

## Task 03: Audio Integration with Video
In this task, a one-minute audio track was selected from a public domain source and integrated with the video created in Task 02.

### Outcome:
The audio was trimmed to exactly one minute using Audacity and then merged with the video using FFmpeg. The final output ensures synchronization between audio and video.

### Command Used:
ffmpeg -i task02_video.mp4 -i audio.mp3 -c:v copy -c:a aac -shortest task03_final_video.mp4

### Outcome:
A final video was successfully created with an integrated audio track, demonstrating multimedia merging using FFmpeg.

### Output:
output.pm4

### Tools Used:
- FFmpeg
- Audacity
- Pixabay (for audio source)
