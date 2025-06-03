
# Lunar Crater Detection Using YOLOv11

## Project Overview
This project implements an automated lunar crater detection system using a custom YOLOv11 object detection model. The goal is to identify and localize craters in high-resolution lunar surface imagery. The pipeline includes:
- Loading a pretrained/custom YOLOv11 model (`best.pt`).
- Performing inference on full images and sliding-window tiled images.
- Applying non-maximum suppression (NMS) to merge overlapping detections.
- Visualizing and saving annotated output images with bounding boxes and confidence scores.

## Table of Contents
1. [Prerequisites](#prerequisites)  
2. [Installation](#installation)  
3. [Project Structure](#project-structure)  
4. [Usage](#usage)  
   - [Single-Image Inference](#single-image-inference)  
   - [Sliding-Window Inference](#sliding-window-inference)  
5. [Code Explanation](#code-explanation)  
   - [Loading the Model](#loading-the-model)  
   - [Inference Parameters](#inference-parameters)  
   - [Drawing Bounding Boxes](#drawing-bounding-boxes)  
   - [Sliding-Window Approach](#sliding-window-approach)  
   - [Non-Maximum Suppression (NMS)](#non-maximum-suppression-nms)  
6. [Outputs](#outputs)  
7. [Troubleshooting](#troubleshooting)  
8. [Acknowledgments](#acknowledgments)  
9. [License](#license)

---

## Prerequisites
- **Python 3.8+**
- **CUDA-compatible GPU** (optional but recommended for faster inference)
- Installed system packages:  
  - `git`
  - `ffmpeg` (if using video inputs / outputs)

## Installation

1. **Clone the Repository (optional)**  
   If you have your code in a Git repository, clone it. Otherwise, create a project directory:
   ```bash
   mkdir lunar-crater-detection
   cd lunar-crater-detection
