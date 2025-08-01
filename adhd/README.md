
# 🧠 음성 AI 기반 ADHD 조기 진단 지원 시스템

**시각장애인, 아동, 학습장애인을 위한 접근성 강화 음성 설문 시스템**  
음성 합성과 인식을 결합한 UX 친화적 설문 도구

---

## 📌 프로젝트 개요

기존 ADHD 설문은 텍스트 중심으로 시각 정보에 의존하고 있어 시각장애인, 아동, 고령자 등 **정보 접근이 어려운 사용자**에게 불리합니다.  
본 프로젝트는 **음성 AI 기술**을 활용해 텍스트 설문을 보조함으로써 **모두가 접근 가능한 설문 환경**을 제공하는 것을 목표로 합니다.

---

## 🎯 프로젝트 목표

- 음성 기반 ADHD 설문 보조 시스템 구축
- Zonos 및 gTTS를 통한 **맞춤형 TTS 음성 제공**
- Whisper 기반 실시간 **음성 응답 인식(STT)**
- **시각 정보의 의존성 감소**, 설문 접근성 향상
- 연령대별 적합한 **캐릭터 보이스**로 참여도 증가

---

## 🛠️ 기술 스택

### 📍 프론트엔드
- **SvelteKit**: 빠른 렌더링, SPA 구조
- 사용자 흐름:  
  1. 버튼 클릭으로 설문 시작  
  2. 문항 음성 출력 (Zonos or gTTS)  
  3. 음성 응답 녹음 및 전송  
  4. 결과 시각화

### 📍 백엔드
- **FastAPI** 기반 REST API
- TTS: `Zonos v0.1`, `gTTS`
- STT: `Whisper (medium)` 모델
- 전처리: `ffmpeg`로 wav 변환
- 응답 보정: `RapidFuzz`로 유사도 기반 응답 정규화
- JSON 응답 결과 제공

---

## 🔁 시스템 흐름도

```
[문항 준비] → [Zonos로 음성 출력]  
→ [사용자 응답 녹음] → [서버로 전송]  
→ [Whisper로 텍스트 변환] → [응답 유사도 분석]  
→ [진단 결과 반환]
```

---

## 🧪 Zonos 모델 특징

| 항목              | Zonos           | gTTS             |
|------------------|------------------|------------------|
| 음성 합성 품질   | 고품질, 감정 표현 가능 | 단조로운 TTS |
| 사용자 맞춤       | 나이별/톤별 설정 가능 | 없음             |
| 다국어 지원       | 지원함           | 일부 제한         |
| 보이스 클로닝     | 제로샷 가능      | 불가능            |

---

## 🎉 기대 효과

- **시각 기반 설문에 어려움을 겪는 사용자**에 대한 접근성 향상  
- **어린이 및 고령자**에게 친숙한 음성 인터페이스 제공  
- **감정/속도/톤 조절**을 통한 이해도 및 응답 정확도 개선  
- **자가 진단 → 조기 대응** 유도  
- 키오스크, 모바일, 병원, 학교 등 다양한 환경에서 적용 가능

---

## 📺 시연 영상
👉 [유튜브 링크 바로가기](https://youtu.be/WOPnH7aNvE8)

---

## 👨‍👩‍👦 팀 소개

- 김석호 (팀장) - [kimseockho93@gmail.com]  
- 석지원 (팀원) - [wb00102681@gmail.com]  
- 이지훈 (팀원) - [ezh737@gmail.com]
