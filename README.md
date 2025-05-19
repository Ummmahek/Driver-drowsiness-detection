# Driver-drowsiness-detection

# Driver Drowsiness Detection

This project implements a real-time Driver Drowsiness Detection system using computer vision and deep learning. It utilizes YOLOv8 for face detection and computes Eye Aspect Ratio (EAR) and Mouth Aspect Ratio (MAR) from facial landmarks to detect signs of drowsiness such as eye closure and yawning.

## Features

- Real-time face detection using YOLOv8
- Eye Aspect Ratio (EAR) for blink detection
- Mouth Aspect Ratio (MAR) for yawn detection
- Drowsiness alert logic based on EAR/MAR thresholds
- Combines deep learning (YOLO) with classical computer vision techniques

## Methodology

1. **Face Detection**: YOLOv8 detects and crops the driver’s face in each frame.
2. **Facial Landmark Extraction**: MediaPipe Face Mesh is used to extract 468 facial landmarks.
3. **EAR/MAR Calculation**:
   - EAR is computed using eye landmarks to monitor eye closure duration.
   - MAR is computed using mouth landmarks to detect yawning.
4. **Drowsiness Criteria**:
   - If EAR falls below a threshold for a set number of consecutive frames, the driver is considered drowsy.
   - If MAR exceeds a threshold, yawning is detected.
5. **Alert System**: A warning message or alarm is triggered if drowsiness is detected.

## Project Structure

driver-drowsiness-detection/
│
├── YOLO2.ipynb # Main notebook with detection pipeline
├── requirements.txt # List of Python dependencies
├── README.md # Project documentation

## Dataset

This project uses videos from the [NTHU Driver Drowsiness Detection Dataset](https://github.com/TNT-NTHU/DDD), which includes recordings of over 30 drivers under drowsy and non-drowsy conditions.

The system also supports real-time testing using webcam or video files.
