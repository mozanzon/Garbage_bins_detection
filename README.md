# Garbage Bins Detection

This repository contains a dataset and trained models for detecting garbage bins.

## Dataset Information
- **Source:** [Roboflow Universe](https://universe.roboflow.com/finance-insitut/garbage-container-detection-sam7i)
- **License:** CC BY 4.0
- **Format:** YOLOv8

## Project Structure
- `train/`, `valid/`, `test/`: Dataset splits containing images and YOLO format labels.
- `data.yaml`: Configuration file for training.
- `best.pt`: Trained PyTorch model weights.
- `best.onnx`: Exported ONNX model for deployment.

## How to use
You can use the `best.pt` model with the Ultralytics YOLOv8 library:
```python
from ultralytics import YOLO
model = YOLO('best.pt')
results = model.predict('path/to/image.jpg')
```
