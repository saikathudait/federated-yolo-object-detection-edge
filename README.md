# Federated Object Detection on Smart Cameras at the Edge Using YOLO

## Overview
This project presents a federated learning framework for object detection in smart surveillance systems. It uses a YOLO-based deep learning model trained collaboratively across distributed edge clients such as cameras, CCTV systems, and drones, without sharing raw image data.

## Motivation
Traditional centralized training for surveillance object detection suffers from privacy risks, high bandwidth usage, and poor scalability. Federated learning addresses these challenges by enabling local training on edge devices and aggregating only model parameters.

## Key Features
- YOLO-based real-time object detection
- Federated learning using Federated Averaging (FedAvg)
- Multi-source surveillance support (Camera, CCTV, Drone)
- Privacy-preserving training (no raw data sharing)
- Edge-friendly CPU/GPU compatible implementation
- Gradio-based inference demo

## Dataset Structure
dataset/
├── images/
│ ├── train/
│ ├── val/
│ └── test/
├── labels/
│ ├── train/
│ ├── val/
│ └── test/


Each split contains subfolders for:
- camera
- cctv
- drone

Annotations follow the YOLO format.

## Methodology
1. Initialize a shared YOLO model using pre-trained weights  
2. Train separate local models for each surveillance source  
3. Aggregate client models using Federated Averaging  
4. Update the global model iteratively across federated rounds  

## Technologies Used
- Python
- PyTorch
- Ultralytics YOLOv8
- OpenCV
- Gradio
- Google Colab

## How to Run
1. Upload the dataset ZIP file
2. Install dependencies
3. Run federated training
4. Perform inference on test images
5. Launch Gradio interface for real-time detection

## Output
- Trained federated YOLO model
- Visual object detection results
- Interactive Gradio demo

## Use Cases
- Smart surveillance systems
- Traffic monitoring
- Public safety analytics
- Privacy-preserving edge AI applications

## License
This project is intended for academic and research purposes.

