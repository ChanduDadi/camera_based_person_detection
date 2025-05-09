# Camera-Based Queue Analysis in an Amusement Park

This project presents a real-time queue analysis system developed for an amusement park scenario. It leverages YOLO for person detection and Torchreid for robust cross-camera re-identification to ensure individuals are tracked without duplication.

## Overview

- **Goal**: Dynamically estimate the number of people in a queue using multi-camera feeds.
- **Challenge**: Accurately track people across overlapping or angled camera views, avoiding double counting.
- **Approach**: Use YOLO for initial person detection and Torchreid to maintain identity across camera transitions.

## System Pipeline

1. **Person Detection**: YOLO detects individuals in each frame from multiple camera streams.
2. **Feature Extraction**: Appearance features are extracted using Torchreid models.
3. **Re-Identification**: Cross-camera ID matching is performed to track individuals continuously.
4. **Queue Counting**: The number of unique individuals currently in view is updated in real-time.

## Tools Used

- Python
- YOLOv5 (for person detection)
- Torchreid (for re-identification)
- OpenCV (for video processing and visualization)

## Demo

The demo shows a live simulation where individuals are tracked across multiple camera views. Bounding boxes and ID labels illustrate successful re-identification and accurate queue length estimation.

