# **Receipt OCR solutions for document automation**  

---

## **프로젝트 개요**  
본 프로젝트는 **YOLOv8**과 **PaddleOCR**를 활용하여 영수증 이미지에서 주요 정보를 검출하고 구조화된 데이터로 변환하는 AI 모델을 구현하는 것입니다.  

---

## **주요 기능**  
- **YOLOv8 모델**을 활용한 날짜, 상호명, 총 금액, 품목 등 주요 영역 분류 및 검출  
- **PaddleOCR**를 활용한 텍스트 인식  
- 검출된 영역의 텍스트를 추출하여 **구조화된 형태**로 저장  
- **구조화된 데이터 출력**: 날짜, 상호명, 총 금액, 품목 리스트 제공  

---

## **Requirements**  
다음의 라이브러리 및 도구를 설치해야 프로젝트를 실행할 수 있습니다.

```bash
pip install easyocr
pip install ultralytics
pip install opencv-python-headless
pip install paddlepaddle
pip install paddleocr
```

---

## **프로젝트 구조**  

아래는 프로젝트의 디렉토리 구조입니다.

```plaintext
AISW_project/
├── dataset/
│   ├── train/            # 훈련 데이터셋
│   │   ├── images/       # 훈련 이미지 파일들
│   │   ├── labels/       # 훈련 라벨 파일들 (YOLO 포맷)
│   ├── valid/            # 검증 데이터셋
│   │   ├── images/       # 검증 이미지 파일들
│   │   ├── labels/       # 검증 라벨 파일들
├── best.pt               # 학습된 YOLOv8 모델 가중치 파일
├── YOLO_PaddleOCR.ipynb  # 프로젝트 실행 코드
└── README.md             # 프로젝트 설명 파일
```

---

## **참고 사항**  
- **YOLOv8**의 학습된 가중치는 `best.pt` 파일에 저장되어 있습니다.  
- **PaddleOCR**를 사용하기 때문에 다국어(한국어 포함) 텍스트 인식이 가능합니다.  

---
