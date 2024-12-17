# YOLOv8 and PaddleOCR Integration for Receipt Key Information Extraction

This project combines YOLOv8 and PaddleOCR to detect and extract key information from receipt images. The system identifies specific regions on the receipt, such as store name, date/time, items, and total amount, using YOLOv8, and then recognizes text in these regions using PaddleOCR.

## Features
- **Key Information Detection**: YOLOv8 is trained to detect specific regions on receipts, including:
  - **Store Name**
  - **Date/Time**
  - **Item Descriptions**
  - **Total Amount**
- **Text Recognition**: PaddleOCR extracts text from the detected regions with language-specific support (Korean in this example).
- **Visualization**: The results include bounding boxes for detected regions and the recognized text overlaid on the original receipt image.

## Project Structure
- `main.ipynb`: The Jupyter Notebook containing the implementation for detection and recognition.
- `best.pt`: YOLOv8 trained model for detecting receipt regions (not included; download link provided below).
- `PretendardVariable.ttf`: Korean font file used for text visualization.
- `test_image.jpeg`: Sample test image of a receipt for demonstration.
- AISW_project/
│
├── dataset/
│   ├── train/
│   │   ├── images/      # 훈련 이미지 파일들이 저장되는 디렉토리
│   │   │   ├── image1.jpg
│   │   │   ├── image2.jpg
│   │   │   └── ...      # 기타 훈련 이미지 파일들
│   │   ├── labels/      # 훈련 라벨 파일들이 저장되는 디렉토리 (YOLO 포맷)
│   │   │   ├── image1.txt
│   │   │   ├── image2.txt
│   │   │   └── ...      # 기타 훈련 이미지와 매칭되는 라벨 파일들
│   │
│   ├── valid/
│   │   ├── images/      # 검증 이미지 파일들이 저장되는 디렉토리
│   │   │   ├── image3.jpg
│   │   │   ├── image4.jpg
│   │   │   └── ...      # 기타 검증 이미지 파일들
│   │   ├── labels/      # 검증 라벨 파일들이 저장되는 디렉토리 (YOLO 포맷)
│   │   │   ├── image3.txt
│   │   │   ├── image4.txt
│   │   │   └── ...      # 기타 검증 이미지와 매칭되는 라벨 파일들
│
├── best.pt               # 학습된 YOLO 모델 가중치 파일


## Requirements
The following packages are required to run the project:
- `ultralytics`
- `paddleocr`
- `opencv-python-headless`
- `pillow`

Install them using:
```bash
pip install ultralytics paddleocr opencv-python-headless pillow
