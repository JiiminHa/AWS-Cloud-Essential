# 03. Amazon Rekognition — 이미지 분석

관리형 컴퓨터 비전 서비스 **Amazon Rekognition**으로 이미지에서 객체·얼굴·텍스트·보호장구를 탐지하는 모듈.

## 핵심 API

| API | 하는 일 | 실습 |
|---|---|---|
| `detect_labels` | 객체/장면 탐지 (라벨 + Confidence + BoundingBox) | Lab 1 |
| `detect_moderation_labels` | 부적절 콘텐츠 감지 (콘텐츠 조정) | Lab 2 |
| `detect_faces` | 얼굴 탐지 + 속성 분석 (나이·감정·안경 등 FaceDetail) | Lab 3 |
| `compare_faces` | 두 이미지 얼굴 비교 (Similarity) | Lab 4 |
| `detect_text` | 이미지 속 텍스트 탐지 (LINE / WORD) | Lab 5 |
| `recognize_celebrities` | 유명인 인식 | Lab 6 |
| `detect_protective_equipment` | 개인 보호 장구(PPE) 착용 감지 | Lab 7 |

## 파일

- `1~7-*-exercise.ipynb` — 실습 노트북 (✅ 대부분 실행 결과 포함, TODO 채움 방식)
- `images/` — 실습용 이미지 (lab별 매칭)
- `docs/` — 교안 + 실습교재 PDF

## 복습 체크리스트

- [ ] `detect_labels` 응답 구조에서 `Instances`가 있는 라벨과 없는 라벨의 차이는?
- [ ] BoundingBox 좌표(0~1 비율)를 실제 픽셀 좌표로 변환하는 법은?
- [ ] `MinConfidence` 파라미터는 어떤 트레이드오프를 만드는가?
- [ ] `compare_faces`에서 `SimilarityThreshold` 아래인 얼굴은 어디에 담겨 오는가? (`UnmatchedFaces`)
- [ ] Rekognition `detect_text` vs Textract — 언제 무엇을 쓰는가? (장면 텍스트 vs 문서)
- [ ] PPE 탐지 응답에서 사람별 → 신체부위별 → 장구별 구조를 그릴 수 있는가?
