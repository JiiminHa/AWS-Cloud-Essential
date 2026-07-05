# 01. Cloud & AWS 소개 + SageMaker Canvas

클라우드 컴퓨팅 기본 개념과 AWS를 소개하고, 코드 없이 ML 모델을 만드는 **SageMaker Canvas**로 영화 흥행 예측 모델을 만든 모듈.

## 배운 것

- 클라우드 컴퓨팅 개념, AWS 주요 서비스 지형도
- ML 워크플로: 데이터 준비 → 학습 → 평가 → 예측
- **SageMaker Canvas**: 노코드로 표 형태 데이터 회귀/분류 모델 구축
- 모델 평가 지표 (RMSE, MAE, R² 등) — `docs/ML_모델평가_강의노트.pdf`

## 파일

| 파일 | 내용 |
|---|---|
| `tmdb-dataset-preprocessing.ipynb` | TMDB 영화 데이터셋 전처리 (Canvas 입력용 CSV 만들기) |
| `data/tmdb_5000_movies.csv`, `data/tmdb_5000_credits.csv` | 원본 데이터셋 (Kaggle TMDB 5000) |
| `data/movie_box_office_prediction_tmdb_like.csv` | 전처리 완료본 — Canvas에 업로드해서 흥행(revenue) 예측 |
| `docs/[교안] 01_...pdf` | 강의 슬라이드 |
| `docs/[실습교재] 01_...pdf` | Canvas 실습 단계별 가이드 |

## 복습 체크리스트

- [ ] IaaS / PaaS / SaaS 차이를 예시 서비스와 함께 설명할 수 있는가?
- [ ] JSON 문자열 컬럼(genres, cast 등)을 판다스로 파싱해서 피처로 만드는 과정을 설명할 수 있는가?
- [ ] Canvas에서 타깃 컬럼 지정 → Quick build vs Standard build 차이는?
- [ ] 회귀 모델 평가에서 RMSE와 MAE의 차이, R²의 의미는?
