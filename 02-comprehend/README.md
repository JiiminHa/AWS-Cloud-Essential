# 02. Amazon Comprehend — 자연어 처리(NLP)

관리형 NLP 서비스 **Amazon Comprehend**로 텍스트에서 언어·감성·개체·PII·토픽을 추출하는 모듈.

## 핵심 API

| API | 하는 일 | 실습 |
|---|---|---|
| `detect_dominant_language` | 언어 감지 | Lab 1 |
| `detect_sentiment` | 감성 분석 (POSITIVE/NEGATIVE/NEUTRAL/MIXED + 점수) | Lab 1 |
| `detect_entities` | 개체 인식 (NER — PERSON, LOCATION, DATE …) | Lab 2 |
| `detect_key_phrases` | 핵심 문구 추출 | Lab 2 |
| `detect_targeted_sentiment` | 개체별(대상별) 감성 분석 | Lab 3 |
| `detect_pii_entities` | 개인정보(PII) 감지 | Lab 3 |
| `detect_syntax` | 구문 분석 (품사 태깅) | Lab 4 |
| 토픽 모델링 (배치 작업) | 문서 집합에서 숨은 주제 발견 (비지도 학습) | Lab 5 |

## 파일

| 파일 | 내용 | 상태 |
|---|---|---|
| `comprehend-lab1-student.ipynb` | 언어 감지 & 감성 분석 | ✅ 실행 결과 포함 |
| `comprehend-lab2-student.ipynb` | 개체 인식(NER) & 핵심 문구 추출 | ✅ 실행 결과 포함 |
| `comprehend-lab3-student.ipynb` | 대상 감성 분석 & PII 감지 | ✅ 실행 결과 포함 |
| `comprehend-lab4-student.ipynb` | 구문 분석 & 종합 텍스트 분석 파이프라인 | ⬜ 미실행 원본 (실습본 유실) |
| `comprehend-lab5-student.ipynb` | 토픽 모델링 & 비지도 학습 개념 | ✅ 실행 결과 포함 |
| `comprehend-lab6-challenge-solutions.ipynb` | Lab 1–5 심화 도전 **해답 모음** | ✅ 실행 결과 포함 |
| `outputs/` | lab02 결과 CSV, lab04 대시보드/결과, 위치 지도 HTML | |
| `docs/` | 슬라이드, 실습 가이드, 콘솔 실시간 분석 핸즈온 | |

## 복습 체크리스트

- [ ] `detect_sentiment` 응답에서 `Sentiment`와 `SentimentScore`의 관계는?
- [ ] 일반 감성 분석과 **대상(Targeted) 감성 분석**의 차이를 예시로 설명할 수 있는가? (한 문장에 대상이 2개일 때)
- [ ] PII 감지 결과로 마스킹 처리를 어떻게 구현했는가? (`BeginOffset`/`EndOffset` 활용)
- [ ] 지도학습 vs 비지도학습 차이, 토픽 모델링이 비지도인 이유는?
- [ ] 심화 해답(lab6)의 "부정 리뷰 필터링 → 점수 내림차순 정렬"을 직접 다시 짤 수 있는가?
