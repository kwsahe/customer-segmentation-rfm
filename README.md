# customer-segmentation-rfm
RFM analysis for customer segmentation

# 🛍️ 온라인 쇼핑몰 고객 세분화 (RFM 분석)

![Python](https://img.shields.io/badge/python-3.11-blue?logo=python)
![Jupyter](https://img.shields.io/badge/jupyter-notebook-orange?logo=jupyter)
![Pandas](https://img.shields.io/badge/pandas-2.0.3-blue?logo=pandas)
![Matplotlib](https://img.shields.io/badge/matplotlib-3.7.2-blue?logo=matplotlib)
![Seaborn](https://img.shields.io/badge/seaborn-0.12.2-blue?logo=seaborn)

---

## 1. 프로젝트 개요

온라인 쇼핑몰의 고객 데이터를 활용하여 고객 가치를 평가하고, 이를 바탕으로 효과적인 마케팅 전략을 수립하기 위한 RFM 기반 고객 세분화 분석을 진행했습니다.

###  분석 배경
- 고객 개개인에 대한 이해 없이 진행되는 마케팅은 비용 효율이 낮고 고객 만족도 또한 떨어뜨릴 수 있습니다.
- 데이터를 기반으로 고객을 여러 그룹으로 분류하고, 각 그룹의 특성에 맞는 맞춤형 전략을 제공하여 마케팅 효율을 극대화하고자 합니다.

### 분석 목표
- 고객의 **최근성(Recency)**, **빈도(Frequency)**, **구매 금액(Monetary)**을 나타내는 RFM 지표를 생성합니다.
- 생성된 RFM 지표를 바탕으로 K-Means 클러스터링을 활용하여 고객을 의미 있는 그룹으로 세분화합니다.
- 각 고객 그룹의 특성을 파악하고, 그룹별 맞춤 마케팅 전략을 제안합니다.

### 사용 데이터
- [UCI Machine Learning Repository: Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail)

### 분석 도구
- `Python 3.11`
- `Jupyter Notebook`
- `Pandas`, `NumPy`
- `Matplotlib`, `Seaborn`
- `Scikit-learn`

---

## 2. 분석 절차
1.  **데이터 불러오기 및 전처리:** 결측치, 이상치 처리 및 분석에 적합한 데이터 타입으로 변환
2.  **탐색적 데이터 분석 (EDA):** 국가별/상품별/시간별 데이터 분포 및 매출 트렌드 파악
3.  **RFM 지표 생성:** 각 고객별 Recency, Frequency, Monetary 값 계산
4.  **클러스터링 및 고객 세분화:** K-Means 알고리즘을 활용하여 RFM 데이터를 기반으로 고객 그룹화
5.  **분석 결과 시각화:** 각 고객 세그먼트의 특징 및 분포 시각화
6.  **결론 및 마케팅 전략 제언:** 분석 결과를 바탕으로 비즈니스 인사이트 및 액션 아이템 도출

---

## 3. 주요 분석 결과

### EDA 주요 결과
- **국가별 주문 분포:** 전체 주문의 약 80% 이상이 영국(United Kingdom)에서 발생하는 것을 확인했습니다.
  
  `[여기에 국가별 주문 수 그래프 이미지를 넣어주세요]`

- **월별 매출 트렌드:** 연말(11월, 12월)로 갈수록 매출이 급격하게 증가하는 경향을 보였습니다. 이는 연말 선물 시즌의 영향으로 해석됩니다.

  `[여기에 월별 매출액 추이 그래프 이미지를 넣어주세요]`

### RFM 기반 고객 세분화 결과
K-Means 클러스터링을 통해 고객을 4개의 그룹으로 세분화했습니다.

| 세그먼트 | 특징 | 비율 |
| :--- | :--- | :--- |
| **VIP 고객** | 최근 방문, 구매 빈도 높음, 총 구매액 높음 | 15% |
| **충성 고객** | 구매 빈도는 높지만, 최근 방문이 뜸하거나 구매액이 평균 수준 | 30% |
| **잠재 고객** | 최근에 가입했거나 구매 경험이 적은 고객 | 40% |
| **이탈 우려 고객** | 마지막 구매일이 오래되고, 구매 빈도와 금액 모두 낮은 고객 | 15% |

---

## 4. 결론 및 마케팅 전략 제언

### 🎯 그룹별 맞춤 전략

- **VIP 고객 (VIP Customers):**
  - **전략:** 충성도 유지 및 강화
  - **액션 아이템:** 신제품 우선 체험 기회 제공, VIP 전용 할인/쿠폰, 감사 선물 발송

- **충성 고객 (Loyal Customers):**
  - **전략:** 구매 촉진 및 관계 유지
  - **액션 아이템:** 구매 금액 기반의 포인트 제도, 관련 상품 추천 이메일 발송

- **잠재 고객 (Potential Customers):**
  - **전략:** 첫 구매 유도 및 재방문 장려
  - **액션 아이템:** 첫 구매 할인 쿠폰, 신규 회원 대상 이벤트 안내

- **이탈 우려 고객 (At-Risk Customers):**
  - **전략:** 재방문 유도 및 이탈 방지
  - **액션 아이템:** 파격적인 할인 쿠폰 발송, 관심 상품 재입고 알림 등 적극적인 리마인드 메시지

---
## 5. 프로젝트 실행 방법

```bash
# 1. 저장소 복제
git clone [https://github.com/YourUsername/your-repo-name.git](https://github.com/YourUsername/your-repo-name.git)

# 2. 폴더로 이동
cd your-repo-name

# 3. 필요한 라이브러리 설치
pip install -r requirements.txt

# 4. 주피터 노트북 실행
jupyter notebook RFM_Analysis.ipynb