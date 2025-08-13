# Number Plate Detection using YOLOv8

## 📌 Project Overview

This project implements **automatic vehicle number plate detection** using the **YOLOv8 object detection model**. The goal is to detect and extract number plates from vehicle images or video streams in real-time. The detected plates can further be processed using **OCR (Optical Character Recognition)** to retrieve the text.

## 📂 Dataset

* **Source:** [Kaggle Number Plate Dataset](https://www.kaggle.com/)
* The dataset contains labeled images of vehicles with annotated bounding boxes around number plates.
* Images are preprocessed and split into **training, validation, and testing** sets.

## 🛠️ Tech Stack

* **Programming Language:** Python
* **Framework:** [YOLOv8] 
* **Libraries:**

  * `ultralytics` – YOLOv8 model training and inference
  * `opencv-python` – image processing and video handling
  * `pandas`, `numpy` – data handling
  * `matplotlib` – result visualization
  * `pytesseract` (optional) – OCR for plate text extraction

## 🚀 Features

* Real-time number plate detection from images and videos
* High accuracy YOLOv8 model
* Easy-to-train on custom datasets
* Optional OCR integration for text recognition

## 📊 Model Training

1. Download the dataset from Kaggle.
2. Prepare the dataset in **YOLO format** (images + labels).
3. Train the YOLOv8 model:

   ```bash
   yolo detect train data=dataset.yaml model=yolov8n.pt epochs=50 imgsz=640
   ```
4. Evaluate model performance on the test set.

## ▶️ Inference

Run detection on an image:

```bash
yolo detect predict model=best.pt source=path/to/image.jpg
```

Run detection on a video:

```bash
yolo detect predict model=best.pt source=path/to/video.mp4
```
 
