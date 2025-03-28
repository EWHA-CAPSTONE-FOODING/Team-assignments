# Team-Info
| (1) 과제명 | *YOLOv8을 이용한 1인 가구 식재료 낭비 방지 서비스*
|:---  |---  |
| (2) 팀 번호 / 팀 이름 | *40-판타지* |
| (3) 팀 구성원 | 김민주 (1971009): 리더, *FE* <br> 문이현 (2176134): 팀원, *BE* <br> 안채연 (2276184) : 팀원, *AI*			 |
| (4) 팀 지도교수 | 오세은 교수님 |
| (5) 과제 분류 | *산학과제* |
| (6) 과제 키워드 | *생성형 AI, 식재료 낭비 방지, 사물인식*  |
| (7) 과제 내용 요약 | *1인 가구의 식재료 재고 효율화를 통해 식재료 낭비를 최소화하는 것을 목표로 합니다. 사용자는 간편한 식재료 등록 기능을 통해 보유 식재료를 관리할 수 있으며, 이를 기반으로 메뉴 및 레시피 추천 서비스를 제공받습니다. 또한, 소비 데이터를 시각화한 주간 레포트와 구매 목록 제안 기능을 통해 체계적인 관리가 가능합니다. 식재료 인식 및 자동 등록 기능에는 YOLOv8과 OCR 기술을, 메뉴 및 레시피 추천 기능에는 GPT-4o, 주간 레포트 및 구매 목록 제안 기능에는 SQL과 구매 주기 예측 알고리즘을 적용하였습니다.* |

<br>

# Project-Summary
| 항목 | 내용 |
|:---  |---  |
| (1) 문제 정의 | *본 과제는 1인 가구 증가에 따른 식재료 관리의 비효율성과 이로 인한 낭비, 불필요한 비용 발생 문제를 해결하고자 합니다. 자체 IDI 결과에 따르면, 1인 가구는 식재료를 제대로 관리하지 못해 유통기한이 지난 후 폐기하는 경우가 빈번하며, KREI 연구보고서에서는 이러한 낭비가 비용 손실과 환경적 자원 낭비로 이어진다고 지적하고 있습니다. 또한, 한국농촌경제연구원의 조사 결과 1인 가구는 불규칙한 식습관과 영양 불균형 문제를 겪고 있어, 건강한 식단 가이드의 제공이 시급한 상황입니다. 본 과제는 이러한 문제점을 해소하여 타깃 고객인 1인 가구에게 효율적인 식재료 관리 및 건강한 식습관 형성을 지원하는 솔루션을 제공하는 것을 목표로 합니다.*  |
| (2) 기존연구와의 비교 | <br>1. 원더 프리지<br> - 소개: 냉장고, 냉동실, 실온에 보관된 식재료를 체계적으로 정리하고 소비기한 알림을 제공하는 앱 <br>- 장점: 식재료 등록 시 유통기한이 자동으로 입력되며, 보관장소(냉장실, 냉동실 등) 분류와 가족과의 공동 관리 기능을 제공 <br>- 단점: 식재료 자동 등록, 메뉴 추천, 주간 레포트, 구매 제안, 챗봇 등의 고도화된 기능이 부재<br> - 기능 비교: 식재료 자동 등록: X, 냉장고 기능: O, 메뉴 추천 기능: X, 주간 레포트 기능: X, 구매 제안 기능: X, 챗봇 기능: X <br><br>2. 냉장고 파먹기 <br>- 소개: 냉장고에 보관된 재료를 활용하여 만들 수 있는 레시피를 제안하는 앱 <br>- 장점: 등록된 냉장고 재료를 기반으로 다양한 레시피를 조회 및 추천받을 수 있으며, 최신 트렌드의 레시피를 제공 <br>- 단점: 앱에 등록되지 않은 재료는 활용이 어려워 제한된 재료 내에서만 레시피 추천이 가능<br> - 기능 비교: 식재료 자동 등록: X, 냉장고 기능: O, 메뉴 추천 기능: O, 주간 레포트 기능: X, 구매 제안 기능: X, 챗봇 기능: X <br><br>3. 만개의 레시피<br>- 소개: 10만여 개의 레시피와 커뮤니티 기능을 통해 다양한 요리법을 공유하는 앱<br>- 장점: 여러 사용자들의 다양한 레시피를 선택하여 개인 맞춤형 요리법을 활용할 수 있음<br>- 단점: 다수의 광고로 인한 UI/UX 불편 및 레시피 관련 문의는 Q&A 게시판을 통해 해결해야 함<br> - 기능 비교: 식재료 자동 등록: X, 냉장고 기능: O, 메뉴 추천 기능: O, 주간 레포트 기능: X, 구매 제안 기능: X, 챗봇 기능: X<br><br> 4. 유리트 식단<br>- 소개: 식단 구성 및 관리에 도움을 주는 앱으로, AI 식단 추천과 비용 관리 기능을 제공<br>- 장점: AI 기반 식단 추천, 식단 기록, 식재료 및 외식/배달 비용 관리 기능을 통해 1인 가구의 요구를 충족<br>- 단점: 식단 및 레시피 관련 문의를 실시간으로 해결할 수 있는 기능(예: 챗봇)이 미흡<br> - 기능 비교: 식재료 자동 등록: O, 냉장고 기능: O, 메뉴 추천 기능: O, 주간 레포트 기능: O, 구매 제안 기능: X, 챗봇 기능: X<br><br> 본 과제의 차별화 포인트:<br> 본 과제는 1인 가구를 위한 식재료 관리 솔루션으로, 기존 서비스들이 제공하지 못한 식재료 자동 등록, 사용량 차감, 메뉴 추천, 주간 레포트, 구매 제안 및 챗봇 기능을 통합하여 제공함으로써, 보다 체계적이고 효율적인 식재료 관리와 건강한 식습관 형성을 지원합니다. |
| (3) 제안 내용 | *사용자가 보유한 식재료를 효율적으로 관리할 수 있도록 식재료 등록 및 사용량 자동 차감 기능을 갖춘 재고 관리 서비스를 제공합니다. 또한, 보유 식재료 중 우선 활용해야 할 항목을 반영한 메뉴 추천 기능을 통해 식재료 낭비를 최소화합니다. 1인 가구 특성에 맞춘 소비 데이터를 기반으로 최적의 구매 목록을 제안하여 불필요한 낭비를 줄이고 효율적인 식재료 관리 전략을 지원합니다. 마지막으로, 챗봇을 도입하여 사용자의 실시간 문의 사항을 신속하게 해결할 수 있도록 합니다.* |
| (4) 기대효과 및 의의 | *1인 가구의 식재료 재고 관리 편의성이 대폭 향상되어 효율성이 극대화되고, 불필요한 식재료 낭비를 예방할 수 있습니다. 또한, 건강한 식습관 유도와 비용 절감을 통해 지속가능한 소비 문화를 형성하는 데 기여할 것으로 기대됩니다.* |
| (5) 주요 기능 리스트 | *식재료 등록 기능, 냉장고 기능, 메뉴 추천 기능, 주간 레포트 기능, 구매 제안 기능, 챗봇 기능 <br><br> 1. 식재료 등록 기능* <br> * YOLO v8 기반 이미지 인식, OCR을 활용한 영수증 인식, 그리고 텍스트 입력 기능을 통해 사용자가 손쉽게 식재료를 등록할 수 있도록 구현하였습니다. <br><br> *2. 냉장고 기능* <br> * FIFO(선입선출) 알고리즘을 적용하여 등록 순서대로 식재료를 체계적으로 관리하고, 실시간 재고 목록을 제공하여 효율적인 식재료 사용과 낭비 최소화를 구현합니다. <br><br> *3. 메뉴 추천 기능* <br> * GPT-4o 기반 프롬프트 엔지니어링 기법을 활용하여 우선 사용해야 할 식재료를 반영한 메뉴를 추천, 식재료 낭비를 줄이는 데 기여합니다. <br><br> *4. 주간 레포트 기능* <br> * SQL 데이터 분석과 시각화를 통해 주간 소비 데이터를 도출하고, 가장 많이 사용된 재료와 소비 패턴을 파악하여 효율적인 식재료 관리 방안을 제시합니다. <br><br> *5. 구매 제안 기능* <br> * 구매 주기 예측 알고리즘을 활용해 사용자 맞춤형 식재료 구매 목록을 제공, 최적의 구매 시점을 예측하여 재고 관리 효율을 향상시킵니다. <br><br> *6. 챗봇 기능* <br> * 대화형 AI를 통해 사용자가 식재료, 메뉴, 레시피 등에 대해 실시간으로 문의할 수 있도록 지원하며, 맞춤형 레시피 가이드를 제공합니다. <br>|

<br>

# Project-Design & Implementation
| 항목 | 내용 |
|:---  |---  |
| (1) 요구사항 정의 | *프로젝트를 완성하기 위해 필요한 요구사항을 설명하기에 가장 적합한 방법을 선택하여 기술* <br> 예) <br> - 기능별 상세 요구사항(또는 유스케이스) <br> - 설계 모델(클래스 다이어그램, 클래스 및 모듈 명세서) <br> - UI 분석/설계 모델 <br> - E-R 다이어그램/DB 설계 모델(테이블 구조) |
| (2) 전체 시스템 구성 | *프로젝트를 위하여, SW 전체 시스템의 구조를 보인다. (가능하다면, 사용자도 포함) <br> 주요 SW 모듈을 보이고, 각각의 역할을 기술한다. <br>만약, 오픈소스 혹은 외부 모듈을 사용한다면 이또한 기술한다.* |
| (3) 주요엔진 및 기능 설계 | *프로젝트의 주요 기능 혹은 모듈의 설계내용에 대하여 기술한다 <br> SW 구조 그림에 있는 각 Module의 상세 구현내용을 자세히 기술한다.* |
| (4) 주요 기능의 구현 |1. 식재료 이미지 인식 기능<br> 사용자가 업로드한 식재료 이미지를 인공지능을 활용하여 자동으로 인식하고 분류하는 시스템을 구축하는 것을 목표로 한다. 이를 위해 최신 객체 탐지 모델인 **YOLOv8**을 활용하여 다양한 식재료를 인식할 수 있도록 구현하였다.<br><br>1-2. 데이터셋 구축<br>1-2.1 데이터 수집<br>- 데이터 출처: 인터넷 크롤링<br>- 수집 개수: 총 4,500장 이상의 이미지<br>- 식재료 종류: 15가지 (*당근, 양파, 대파, 버섯, 콩나물, 양배추, 달걀, 우유, 치즈, 버터, 닭고기, 돼지고기, 소고기, 고등어, 갈치*)<br><br>1-2.2 데이터 증강(Augmentation)<br>- 랜덤 회전<br>- 밝기 조절<br>- 크롭 및 확대<br>- 노이즈 추가<br><br>1-2.3 데이터 라벨링<br>- 라벨링 툴 사용: Roboflow<br>- Bounding Box 기준: 식재료의 중심을 포함하도록 설정<br>- Train / Validation / Test 데이터 분할:<br>Train: 4,149장<br>Validation: 161장<br>Test: 164장<br><br>1-3. 모델 학습<br>  1-3.1 환경 설정<br>- 개발 환경: Google Colab Pro (Tesla T4 GPU 활용)<br>- 필요 라이브러리 설치:<br>  
  ```bash  
  !pip install ultralytics roboflow  
  ```<br><br> 1-3.2 YOLOv8 모델 설정<br>- YOLOv8 모델 다운로드 및 학습 설정:<br>  
  ```python  
  from ultralytics import YOLO  

  # YOLOv8 모델 로드  
  model = YOLO("yolov8n.pt")  

  # 모델 학습  
  model.train(  
      data="/content/drive/MyDrive/dataset/data.yaml",  # 데이터셋 설정 파일  
      epochs=50,   # 학습 횟수  
      batch=16,    # 배치 크기  
      imgsz=640,   # 이미지 크기  
      device="cuda" # GPU 사용  
  )  
  ```<br><br>  

### **4. 모델 평가**<br>  
- **Precision (정밀도)**: 0.64 ~ 0.90<br>  
- **Recall (재현율)**: 0.44 ~ 1.0<br>  
- **mAP@50 (Mean Average Precision)**: 평균 0.77<br><br>  

### **5. 모델 테스트 및 결과 분석**<br>  
#### **5.1 테스트 이미지 예측 실행**<br>  
```python  
model = YOLO("/content/runs/detect/train2/weights/best.pt")  
model.predict(source="/content/drive/MyDrive/dataset/test/images", save=True)  
```<br><br>  

#### **5.2 결과 시각화**<br>  
```python  
from IPython.display import Image  
Image(filename=f"/content/runs/detect/predict/{predicted_images[0]}")  
``` |
| (5) 기타 | *기타 사항을 기술*  |

<br>
