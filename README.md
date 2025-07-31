# SiamFC - Single Object Tracking (SOT)

This folder contains the implementation and training/inference pipeline of the **SiamFC** (Fully Convolutional Siamese Network) tracker, evaluated on the OTB100 dataset.

## 📁 Folder Structure

SiamFC/
 ```bash
├── siamfc_train.ipynb # Jupyter Notebook for training and inference
├── siamfc_weights.pth # Saved PyTorch model weights
├── input1.mp4 # Sample input video
├── output1.mp4 # Tracking result video (full sequence)
├── output.mp4 # Tracking result video (subset or preview)
├── data/ # Dataset director OTB100 Dataset need to be manually download through (https://opendatalab.com/OpenDataLab/OTB100)
 ```



## Features

- SiamFC implemented using PyTorch
- Performs depthwise cross-correlation between template and search image
- Evaluation through IoU plots and response map visualization
- Tracking results saved as `.mp4` output videos

## Dataset Used

- **OTB100** benchmark
- Evaluation Set: `Basketball`



## How to Run

1. Open the notebook:
 ```bash
 jupyter notebook siamfc_train.ipynb
  ```
Make sure siamfc_weights.pth and the video/data files are present

Run all cells to:
 ```
Initialize model （CELL3)

Load video (CELL 8)

Predict and draw bounding boxes

Visualize response maps

Export video
 ```
 Evaluations: 


- Response heatmap showing matching region
- Bounding box overlays per frame
- IoU trend over frames
