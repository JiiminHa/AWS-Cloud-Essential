# 06. Bedrock 멀티모달 — 이미지 이해 (Nova)

**Amazon Nova** 모델의 멀티모달 능력으로 이미지를 입력받아 분석하는 모듈. 음식 사진을 보고 메뉴 설명/분석을 생성하는 파이썬 스크립트 실습.

## 파일

| 파일 | 내용 |
|---|---|
| `lab07_bedrock_nova.py` | 이미지 → Nova 모델 분석 스크립트 (Converse API에 이미지 바이트 전달) |
| `food_images/` | 실습용 음식 이미지 4장 |
| `docs/[교안] Lab07_bedrock_image_처리-r.docx` | 실습 교안 |

## 실행 방법

```bash
pip install boto3
# AWS 자격 증명 설정 후 (us-east-1)
python lab07_bedrock_nova.py
```

## 복습 체크리스트

- [ ] Converse API에서 이미지를 어떻게 전달하는가? (content 블록에 `image` 타입 + bytes)
- [ ] 이미지와 텍스트 프롬프트를 한 메시지에 같이 넣는 구조는?
- [ ] 지원 이미지 포맷과 크기 제한은?
- [ ] Rekognition의 이미지 분석과 멀티모달 LLM의 이미지 이해는 어떻게 다른가? (정형 라벨 vs 자유 서술)
