# DATA-AI

1. 의료 데이터 분석 & 머신러닝 
   01. diabetes
      - 사용 데이터 : Pima Indians Diabetes Database on #kaggle via @KaggleDatasets (https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)
      - 분석 코드 : diabetes_의료데이터_분석.ipynb
      - 실습 내용
          - 데이터 살펴보기
          - 라이브러리 사용 + 함수 만들기, 데이터 시각화 : subplot, heatmap, 파이차트
          - training || test : 학습할 수 있는 데이터셋으로 변경 후 패턴 찾아 데이터 예측
          - 머신러닝 학습 + hyper parameter tuning 
            : RogisticRegression, 앙상블학습 이론 - RandomForest, XGBoost
          - pairplot
          - 데이터 가공 후 예측
            : 데이터 불균형 처리 위한 가공 방법 - SMOTE
   02. heart_disease
      - 사용 데이터 : Heart Disease Dataset on #kaggle via @KaggleDatasets (https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset)
      - 분석 코드 : heart_disease_의료데이터_분석.ipynb
      - 실습 내용
          - 데이터 살펴보기
          - 라이브러리 사용 + 함수 만들기, 데이터 시각화 : subplot, heatmap, 파이차트, pairplot etc
          - hyper parameter 최적화 : GridSearchCV
          - 데이터 분류 : KNN + SVM 구현
 2. 딥러닝 분석
    01. face mask detection : 마스크 착용 여부 탐지 및 분류 
        - 사용 데이터 : https://www.kaggle.com/datasets/andrewmvd/face-mask-detection
        1. using VGG19
           - 분석 코드 : face_mask_detection_VGG19.ipynb
        2. using FasterRCNN
           - 분석 코드 : face_mask_detection_faster_R_CNN.ipynb
           - 실습 내용
                - (중간 코드 오류) 'TypeError: can't convert cuda:0 device type tensor to numpy. Use Tensor.cpu() to copy the tensor to host memory first' 오류 발생함
                  ㄴ 텐서가 GPU에 있는지 확인 -> 딕셔너리 내에서 텐서 추출, CPU로 텐서 이동시킴 + 이미지 텐서도 이동시키고 NumPy 배열로 변환해 해결
    02. covid19 detection : 흉부 방사선 사진에서 코로나19 탐지 및 분류 
        - 사용 데이터 : https://www.kaggle.com/competitions/siim-covid19-detection/overview 
        - using FasterRCNN
           - 분석 코드1. covid19_detection.ipynb
           - 분석 코드2. covid19_detection2.ipynb
           - 분석 코드3. covid19_detection_fasterRCNN.ipynb
        - 실습 내용 
           - EDA to prprocessing
                - check & visualize the relation
                - data analysis
                - visualize X-ray with bbox
                - resize the image
           - Basic Modeling
                - image pre-classification with data generator
                     : classify image id by opcity types
                     : sort image files
                     : data generation, split train/valid set
                - modeling : basic multiclass classifier
                - improving performance with an appropriate form 
           - 추가 : 불투명도 감지
                  - extraction position information & all box's information
                  - visualize resized image with boxes
                  - build function for reuse
         * 데이터 용량 커 (110G 넘음) error 발생
