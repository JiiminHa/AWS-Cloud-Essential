# 04. Amazon Bedrock — 생성형 AI 기초

**Amazon Bedrock**으로 파운데이션 모델(FM)을 호출하고, 프롬프트 엔지니어링과 멀티턴 챗봇을 실습한 모듈.

## 배운 것

- Bedrock 아키텍처: 단일 API로 여러 FM(Claude, Nova, Llama 등) 호출
- 주요 모델 ID와 모델 선택 기준 (성능 vs 비용)
- **Converse API**: messages 구조, role(user/assistant), 멀티턴 대화, 컴플리션 개념
  → `docs/[교안] LLM 대화 이해- 메시지, 멀티턴, 컴플리션.docx`
- 프롬프트 엔지니어링: 역할 부여, 예시 제공(few-shot), 출력 형식 지정, 단계적 사고
- `temperature`, `maxTokens` 등 인퍼런스 파라미터

## 파일

| 파일 | 내용 |
|---|---|
| `bedrock-p1-lab1-student.ipynb` | Bedrock 기초 & Foundation Model 탐색 (✅ 실행 결과 포함) |
| `bedrock-p1-lab2-student.ipynb` | NLP 기초 & 프롬프트 엔지니어링 — 업무 자동화 시나리오 (✅) |
| `bedrock-p1-lab3-student.ipynb` | 학교 FAQ 챗봇 구현 — 멀티턴 + 시스템 프롬프트 (✅) |
| `docs/` | 슬라이드, 실습 가이드, LLM 대화 이해 교안 |

## 복습 체크리스트

- [ ] `invoke_model` vs `converse` API의 차이는? 왜 Converse를 권장하는가?
- [ ] messages 배열에서 멀티턴 대화가 유지되는 원리는? (이전 대화를 매번 다시 보내는 구조)
- [ ] system 프롬프트와 user 메시지의 역할 차이는?
- [ ] temperature를 높이면/낮추면 어떤 상황에 유리한가?
- [ ] FAQ 챗봇에서 "모르는 질문에 지어내지 않게" 하려고 어떤 프롬프트 장치를 썼는가?
- [ ] on-demand 모델 ID와 inference profile(`us.` 접두사)의 차이는?
