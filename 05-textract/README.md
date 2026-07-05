# 05. Amazon Textract — 문서 AI

**Amazon Textract**로 문서 이미지/PDF에서 텍스트·폼·표·영수증·신분증 정보를 구조적으로 추출하는 모듈. 마지막에 문서 자동 분류 캡스톤 프로젝트 포함.

## 핵심 개념: Block

Textract의 모든 응답은 **Block** 트리 구조 — `PAGE → LINE → WORD`, 폼은 `KEY_VALUE_SET`, 표는 `TABLE → CELL`. `Relationships`로 부모-자식을 따라간다.

## 핵심 API

| API | 하는 일 | 실습 |
|---|---|---|
| `detect_document_text` | 텍스트 감지 (OCR — LINE/WORD) | Lab 1 |
| `analyze_document` + `FORMS` | 폼(키-값 쌍) 추출 | Lab 2 |
| `analyze_document` + `TABLES` | 표 추출 → CSV | Lab 2 |
| `analyze_document` + `QUERIES` | 자연어 질문으로 원하는 값만 추출 | Lab 3 |
| `analyze_expense` | 영수증/인보이스 분석 (SummaryFields, LineItems) | Lab 4 |
| `analyze_id` | 신분증 분석 | Lab 5 |
| `start_document_analysis` (비동기) | 다중 페이지 PDF 처리 (S3 + Job 폴링) | Lab 6 |

## 파일

- `0-overview-setup.ipynb` — 과정 개요 + 환경 설정
- `1~7-*-exercise.ipynb` — 실습 노트북 (✅ 실행 결과 포함)
- `7-capstone-project-exercise.ipynb` — **캡스톤**: 문서 유형 자동 감지 → 유형별 추출 파이프라인
- `images/`, `lab06_pages/` — 실습용 문서 이미지/PDF
- `outputs/` — 폼 추출 JSON, 표 CSV 산출물

## 복습 체크리스트

- [ ] Block의 `Relationships`(CHILD)로 KEY_VALUE_SET에서 키 텍스트와 값 텍스트를 각각 조립하는 과정을 설명할 수 있는가?
- [ ] QUERIES 기능은 FORMS와 무엇이 다른가? 언제 더 유리한가?
- [ ] `analyze_expense`는 왜 별도 API인가? (영수증 특화 필드)
- [ ] 동기 API vs 비동기 API의 제약 차이는? (파일 크기, 페이지 수, S3 필요 여부)
- [ ] 비동기 파이프라인의 흐름: S3 업로드 → `start_*` → JobId → 폴링 → 페이지네이션(`NextToken`)
- [ ] 캡스톤에서 문서 유형(영수증/신분증/일반 폼)을 어떤 신호로 분류했는가?
