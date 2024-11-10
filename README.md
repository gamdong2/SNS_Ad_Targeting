# SNS 광고 타겟 설정을 위한 고객 클러스터링 모델 개발

## Skills
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white"/>&nbsp;
<img src="https://img.shields.io/badge/pandas-150458.svg?style=for-the-badge&logo=pandas&logoColor=white"/>&nbsp;
<img src="https://img.shields.io/badge/numpy-4d77cf.svg?style=for-the-badge&logo=numpy&logoColor=white"/>&nbsp;
<img src="https://img.shields.io/badge/Matplotlib-11557c.svg?style=for-the-badge&logo=Matplotlib&logoColor=white"/>&nbsp;
<img src="https://img.shields.io/badge/Seaborn-11557c.svg?style=for-the-badge&logo=Seaborn&logoColor=white"/>&nbsp;

## 프로젝트 상세

- **진행 기간**: 2024년 8월 30일 ~ 2024년 9월 2일
- **프로젝트 유형**: 개인 프로젝트

## 프로젝트 목표
구매율이 높은 고객층을 식별하고, 이를 대상으로 효과적인 SNS 타겟 마케팅 전략을 구축하여 마케팅 효율성을 극대화하고 고객 만족도를 높임

## 사용한 데이터 셋
- **데이터**: SNS 사용자 정보 및 제품 구매 여부 데이터
   - 고객의 나이와 연소득을 기반으로 구매 패턴을 분석하여, 다양한 고객 군집을 클러스터링하고 타겟 고객을 식별

## 워크플로우

1. **패키지 임포트**
   - 사용한 주요 패키지: pandas, seaborn, numpy, matplotlib, scikit-learn, SciPy

2. **데이터 로드 및 요약**
   - 데이터를 로드하여 변수 간 상관관계와 데이터 분포를 파악하고, 결측치와 이상치를 확인하여 전처리 준비

3. **데이터 전처리**
   - 나이와 연소득 데이터를 중심으로 이상치를 처리하고, 'Gender' 변수를 인코딩하여 클러스터링 모델에 적합한 형태로 변환

4. **스케일링 및 변수 변환**
   - 'Age'와 'EstimatedSalary'에 표준화를 적용하고 연소득에 로그 변환을 통해 이상치 영향을 줄임

5. **탐색적 데이터 분석(EDA)**
   - t-SNE와 히스토그램, 산점도 등을 사용하여 데이터의 잠재적 클러스터 구조와 변수 간 관계를 시각화

6. **클러스터링 모델 학습**
   - K-Means와 Hierarchical Clustering을 적용하여 최적의 클러스터 수(k)를 탐색하고, 각 클러스터의 특성과 구매율을 비교 평가

7. **성능 평가 및 시각화**
   - Elbow Method와 실루엣 점수를 통해 최적의 k를 선정하고, 각 클러스터의 특성 및 구매율에 따른 타겟 고객층을 시각화

## 프로젝트 결과

### 구현 기능
- K-Means와 Hierarchical Clustering을 통한 고객 클러스터링 수행
- 최적의 클러스터(k=4)를 찾고, 타겟 고객층을 기반으로 효과적인 마케팅 전략 도출
- 실루엣 점수와 구매율을 바탕으로 각 클러스터 성능 평가

## 트러블 슈팅

- **오류**: "ValueError: array must not contain infs or NaNs"
  - 데이터의 연소득에 이상치가 포함되어 발생한 오류
- **해결 방법**: 연소득 변수에 로그 변환 후 표준화를 통해 이상치 영향 제거

## 프로젝트를 통해 얻은 역량

- 클러스터링 모델을 통해 고객을 분류하고 타겟 고객을 식별
- 실루엣 점수와 구매율 기반의 성능 평가
- EDA 기법 활용

