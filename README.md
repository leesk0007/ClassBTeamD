# 광진구 내 서울형 키즈카페 입지 선정
---
### ✔️ 파일 설명
- Clustering_result.ipynb
  :
  
- MCLP_result.ipynb
  :
  
- data_for_clustering.csv
  :
  
- candidate_data.csv
  :
  
- kidscafes.csv
  :

## 📁 서울시 공공데이터 (`/Data/`)

| 파일명 | 설명 |
|--------|------|
| `201603_202003_Seoul_BirthPopulation.csv` | 2016년 3월부터 2020년 3월까지의 서울시 출생 인구 데이터 |
| `202004_202503_Seoul_BirthPopulation.csv` | 2020년 4월부터 2025년 3월까지의 서울시 출생 인구 데이터 |
| `Seoul_BusStop.csv` | 서울시 버스정류장 위치 및 정보 |
| `Seoul_CCTV.csv` | 서울시 공공 CCTV 설치 현황 |
| `Seoul_Earnings.csv` | 서울시 지역별 평균 소득 자료 |
| `Seoul_KinderGarten.csv` | 서울시 어린이집 위치 정보 |
| `Seoul_Rent.csv` | 서울시 임대료 수준 정보 (상가/주거 등 가능성 있음) |
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
| `Gwangjingu_KinderGarten.csv` | 광진구 보육시설 (유치원, 어린이집 등) |
| `Gwangjingu_ResisterPopulation.csv` | 광진구 주민등록 인구 정보 |
| `Gwangjingu_SeoulKidsCafe.csv` | 서울형 키즈카페의 광진구 위치 정보 |
| `Gwangjingu_SubwayStation.csv` | 광진구 지하철역 위치 정보 |
| `Total_data_for_clustering.csv` | 광진구 클러스터링 분석을 위한 통합 데이터셋 |
| `Gwangjingu_positive_child.zip` | 광진구 내 유아 수 격자화 |

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
