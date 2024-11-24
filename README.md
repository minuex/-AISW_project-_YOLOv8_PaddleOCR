# -AISW_project-_YOLOv8_PaddleOCR

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

## Requirements
The following packages are required to run the project:
- `ultralytics`
- `paddleocr`
- `opencv-python-headless`
- `pillow`

Install them using:
```bash
pip install ultralytics paddleocr opencv-python-headless pillow
