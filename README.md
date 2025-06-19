# 광진구 내 서울형 키즈카페 입지 선정
---
### ✔️ 파일 설명
# 프로젝트 파일 설명: 서울형 키즈카페 입지 분석

서울 광진구 내 서울형 키즈카페의 입지를 분석하고 최적화하기 위한 두 가지 주요 분석 방법론을 포함: **군집화 기반 비교 분석**, **최대커버리지 입지모형(MCLP)**.

---

# 📁 주요 코드 파일

- **Clustering_Final.ipynb**  
  → `data_for_clustering.csv`를 기반으로 군집화 알고리즘(KMeans, GMM, DBSCAN 등)을 비교하여 유사한 지역군을 도출하는 코드입니다. PCA 시각화, silhouette score 등을 포함하여 군집화 모델 간 성능을 비교합니다.

- **MCLP_result.ipynb**  
  → `candidate_data.csv`, `demand_data.csv`, `kidscafes.csv`를 이용해 최대 커버리지 입지모형(Maximum Coverage Location Problem, MCLP)을 적용하여 최적 입지 후보지를 도출하는 분석 코드입니다.

---

# 📂 데이터 파일 설명

- **data_for_clustering.csv**  
  → 군집화 분석에 사용되는 행정동 단위의 속성 데이터. 주요 변수로 수요층(0~9세, 출생현황), 경제성(가구평균소득, 월평균임대료), 안전성(CCTV, 어린이집), 접근성(지하철역, 버스정류소) 포함합니다.

- **candidate_data.csv**  
  → 입지 후보지로 선정된 격자별 중심 좌표 데이터. 각 후보지는 교통 접근성 점수를 기준으로 사전 필터링된 위치입니다.

- **demand_data.csv**  
  → 수요지로 사용되는 유아 인구 밀집 지역의 좌표 데이터. 각 좌표는 높은 유아 인구수를 기반으로 선정하였습니다.

- **kidscafes.csv**  
  → 현재 광진구 내에 존재하는 서울형 키즈카페 위치 데이터. 입지 중복 방지를 위해 기존 시설과의 거리 제한 조건에 사용합니다.

---

> 본 프로젝트는 서울시 공공 보육정책의 효율적 공간 배치를 위한 데이터 기반 접근을 목표로 합니다.


## 📁 서울시 공공데이터 (`/Data/`)

| 파일명 | 설명 |
|--------|------|
| `201603_202003_Seoul_BirthPopulation.csv` | 2016년 3월부터 2020년 3월까지의 서울시 출생 인구 데이터 |
| `202004_202503_Seoul_BirthPopulation.csv` | 2020년 4월부터 2025년 3월까지의 서울시 출생 인구 데이터 |
| `Seoul_BusStop.csv` | 서울시 버스정류장 위치 및 정보 |
| `Seoul_CCTV.csv` | 서울시 공공 CCTV 설치 현황 |
| `Seoul_Earnings.csv` | 서울시 지역별 평균 소득 자료 |
| `Seoul_KinderGarten.csv` | 서울시 어린이집 위치 정보 |
| `Seoul_Rent.csv` | 서울시 임대료 수준 정보 |
| `Seoul_ResisterPopulation.csv` | 서울시 주민등록 인구 정보 |
| `Seoul_SubwayStation.csv` | 서울시 지하철역 위치 및 관련 정보 |
| `Data_Source.txt` | 데이터 출처 |

---

## 📁 광진구 전처리 데이터 (`Data/Gwangjingu_DataProcessing/`)

| 파일명 | 설명 |
|--------|------|
| `Gwangjingu_BirthPopulation.csv` | 광진구 출생 인구 데이터 |
| `Gwangjingu_BusStop.csv` | 광진구 버스정류장 위치 및 정보 |
| `Gwangjingu_CCTV.csv` | 광진구 공공 CCTV 현황 |
| `Gwangjingu_Earnings.csv` | 광진구 소득 데이터 |
| `Gwangjingu_KinderGarten.csv` | 광진구 보육시설 (어린이집) |
| `Gwangjingu_ResisterPopulation.csv` | 광진구 주민등록 인구 정보 |
| `Gwangjingu_SeoulKidsCafe.csv` | 서울형 키즈카페의 광진구 위치 정보 |
| `Gwangjingu_SubwayStation.csv` | 광진구 지하철역 위치 정보 |
| `Total_data_for_clustering.csv` | 광진구 클러스터링 분석을 위한 통합 데이터셋 |

---

## 📁 광진구 유효유아수 (`Data/Positive_Child/`)

| 파일명 | 설명 |
|--------|------|
| `Gwangjingu_positive_child.shp` 외 (shx, dbf, prj 포함) | 광진구 내 공간격자(또는 구역)별 유효 유아수(`val` 필드 기준)를 담은 공간 정보 데이터셋. SHP 형식이며 QGIS, ArcGIS 등에서 시각화 및 분석 가능 |

> 참고: 일부 `val` 값은 비어 있으며, 유아 인구 밀도를 공간적으로 분석하는 데 활용함.


---

📌 **참고:** 데이터 출처는 각 행정기관 또는 공공 포털에서 수집, `Data_Source.txt` 파일에 출처가 포함되었습니다.

---
### ✔️ 가상환경 설정 (수업시간에 진행한 tfenv 환경 사용)
- python 3.10 버전 기반 환경 설치

  conda create -n tfenv python=3.10

- 환경 활성화

  conda activate tfenv

- tensorflow 설치

  pip install tensorflow==2.12

- ipykernel 설치

  pip install ipykernel

- 기본 패키지 설치

  pip install matplotlib scikit-learn gensim nltk pandas
---

### ✔️ 기타

꾸미팡팡 놀이터 1호점, 2호점은 같은 건물(서울특별시 광진구 능동로 87 3층)에 입점하고 있기에 기존 시설의 개수는 4개로 처리함
