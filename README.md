# 👤 송지승 | Backend & AI Recommendation Developer

## 🧑‍💼 About Me

사용자의 문제를 기술로 해결하는 개발자를 지향합니다.
데이터를 기반으로 구조를 설계하고, 실제로 동작하는 기능을 구현하는 과정에 흥미를 느낍니다.

현재는 컴퓨터 비전과 AI를 활용한 **체형 분석 및 스타일 추천 시스템**을 개발하며,
단순한 기능 구현을 넘어 **서비스 구조 설계와 확장성**을 고려한 개발 경험을 쌓고 있습니다.

---

## 👥 Team Project - FashionPeople (팀명: 무명)

### 👨‍👩‍👧‍👦 팀 구성

* 조영재
* 홍석현
* 송지승

---

### 📌 프로젝트 소개

FashionPeople은 사용자의 신체 데이터를 기반으로 체형을 분석하고,
AI를 활용하여 개인 맞춤형 스타일을 추천하는 서비스입니다.

사용자가 사진을 촬영하면 OpenCV와 MediaPipe를 통해 신체 좌표를 추출하고,
이를 바탕으로 체형을 분석한 뒤 AI가 스타일을 추천합니다.

👉 온라인 쇼핑에서 발생하는 **사이즈 선택 문제와 스타일 고민을 해결하는 것**을 목표로 합니다.

---

## 🧑‍💻 나의 역할 (Backend / AI Recommendation)

### 🔹 1. 체형 데이터 처리 및 분석

* MediaPipe로 추출된 신체 좌표 데이터를 JSON 형태로 입력받아 처리
* 어깨, 허리, 팔 길이, 상하체 비율 등 핵심 지표 기반 데이터 구조 설계

---

### 🔹 2. 체형 분류 시스템 구현 (Rule-Based)

* 신체 비율 데이터를 기반으로 체형을 분류하는 알고리즘 구현

* 주요 기준:

  * shoulder_waist_ratio
  * upper_lower_ratio
  * arm_length / leg_length_avg

* 분류 결과:

  * Body Type (inverted_triangle / rectangle / balanced)
  * Proportion (상하체 비율)
  * Limb Type (팔다리 비율)

---

### 🔹 3. 스타일 추천 구조 설계 (핵심 기여)

* 기존 dictionary 기반 추천 방식에서
  👉 **AI 기반 추천 구조로 개선**

* 역할 분리:

```text id="p3eh6r"
체형 분석 (Rule-based)
→ 스타일 판단 (AI)
→ 스타일 추천 및 설명 생성 (AI)
```

---

### 🔹 4. AI 추천 시스템 구현

* 체형 분류 결과를 AI API에 전달하여 스타일 추천 생성
* 생성 결과:

  * 추천 상의 / 하의
  * 스타일 방향
  * 피해야 할 스타일
  * 스타일 설명 및 팁

---

### 🔹 5. 전체 추천 파이프라인 구현

```text id="v4rjgx"
body_result.json
→ classifier.py (체형 분류)
→ ai_recommender.py (AI 추천)
→ sample_test.py (결과 통합)
```

* 입력부터 출력까지 자동화된 처리 흐름 구축

---

## ⚙️ 기술 스택

| 분야              | 기술                |
| --------------- | ----------------- |
| Language        | Python            |
| AI              | OpenAI API        |
| Computer Vision | OpenCV, MediaPipe |
| Backend         | FastAPI           |
| Frontend        | React             |
| Database        | MySQL             |
| Hardware        | Raspberry Pi      |

---

## 💡 핵심 성과

* 체형 분석 → 추천 → 설명까지 이어지는 **End-to-End 시스템 구현**
* Rule-based + AI Hybrid 구조 설계
* AI API를 활용한 실제 서비스 수준 추천 시스템 구현
* 기능 중심이 아닌 **서비스 구조 중심 개발 경험 확보**

---

## 🚀 향후 발전 방향

* 3D 모델 기반 체형 분석 고도화 (SMPL-X 등)
* 사용자 데이터 기반 개인화 추천 시스템
* 실제 쇼핑몰 데이터 연동

---
