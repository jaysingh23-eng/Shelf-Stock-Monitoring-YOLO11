# Shelf Stock Monitoring using YOLO11

A computer vision project that uses **YOLO11** to detect empty shelf spaces and monitor stock availability in retail environments.

## Project Overview

This project uses a trained YOLO11 object detection model to identify shelf conditions from images. It can detect empty or available shelf spaces and help monitor product stock in real-world retail environments.

## Features

* Empty shelf/void detection
* YOLO11 object detection
* Real-world image testing
* Model training and validation
* Prediction results with bounding boxes
* Performance evaluation using standard detection metrics

## Technologies Used

* Python
* YOLO11
* Ultralytics
* OpenCV
* NumPy
* Matplotlib
* Jupyter Notebook

## Model Performance

| Metric    | Score |
| --------- | ----: |
| Precision | 86.1% |
| Recall    | 83.6% |
| mAP50     | 90.0% |
| mAP50-95  | 51.4% |

## Project Structure

```text
Shelf-Stock-Monitoring-YOLO11/
│
├── models/
│   └── best.pt
│
├── src/
│   ├── train.py
│   └── predict.py
│
├── notebooks/
│
├── dataset/
│   └── data.yaml
│
├── results/
│
├── test_image.jpg
├── Shelf_Stock_Monitoring.ipynb
├── requirements.txt
├── verify_setup.py
└── README.md
```

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/jaysingh23-eng/Shelf-Stock-Monitoring-YOLO11.git
cd Shelf-Stock-Monitoring-YOLO11
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the model

```python
from ultralytics import YOLO

model = YOLO("models/best.pt")

results = model("test_image.jpg", save=True)

for result in results:
    print(result)
```

## Results

The trained model was tested on real-world shelf images to evaluate its ability to identify empty shelf spaces outside the training dataset.

## Future Improvements

* Real-time camera-based shelf monitoring
* Product-level stock detection
* Automatic stock alerts
* Integration with retail inventory systems
* Improved detection under different lighting conditions

## Author

**Jay Narayan Singh**

Data Science Student
Karnavati University
