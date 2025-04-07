# 🔌 Smart Tap (스마트 멀티탭 제어 시스템)

> Android 앱 + Arduino + Relay 모듈을 이용한 원격 전력 제어 졸업작품  
> **3인 팀 프로젝트 / 2017년 2학기 진행**

---

## 📌 프로젝트 개요

스마트 멀티탭(Smart Tap)은 콘센트의 전원을 원격으로 제어하고 실시간 전력 사용량을 시각화할 수 있는 IoT 기반 시스템입니다.  
Android 앱과 아두이노, 릴레이 모듈을 연동하여 구현했으며, 음성 인식 기능도 포함되어 사용자 편의성을 높였습니다.

---

## 🧠 주요 기능

- 📱 **Android 앱 제어**: 개별 콘센트 ON/OFF
- 🔊 **음성 인식 제어**: "전원 꺼줘", "전원 켜줘" 등 명령 수행
- 📈 **전력 사용량 실시간 시각화**
- 🕐 **탭별 전원 예약 기능**
- 🔋 **배터리 100% 충전 시 자동 OFF**
- 🌐 **내부 네트워크 기반 통신**
- 🔌 **아두이노 + 릴레이 회로 구성**

---

## 📆 개발 타임라인

| 주차 | 개발 내용 |
|------|-----------|
| 2주차 | 앱을 통한 멀티탭의 ON / OFF 기능 구현 |
| 3주차 | - MPAndroidChart 라이브러리로 전력 사용량 선형 그래프 표시<br>- 음성 인식("켜줘", "꺼줘") 앱 제어 기능 구현 |
| 4주차 | 각 구별 ON / OFF 예약 기능 구현 |
| 5주차 | 예약 항목을 리스트로 시각화 |
| 8주차 | 휴대폰 배터리 100% 도달 시 자동 전원 OFF 기능 추가 |
| 10주차 | 아두이노와 앱 연동 완료 (통신 테스트 포함) |

> 📊 사용 라이브러리: [MPAndroidChart](https://github.com/PhilJay/MPAndroidChart)

---

## 🛠️ 어려웠던 점 및 해결 방법

### ✅ 1. 앱 종료 시 Switch 상태 초기화 문제

- **문제**: 앱에서 탭별 ON/OFF 설정 후 종료하면 설정이 초기화됨
- **해결**: `SharedPreferences`를 사용하여 로컬 파일에 상태 저장 → 앱 재시작 후에도 이전 상태 유지

---

### ✅ 2. 예약 삭제 기능 오류

- **문제**: 예약 삭제 후 액티비티 전환 시 삭제한 예약이 복원되는 현상
- **원인**: Adapter의 `position` 값만으로 DB 기본키 매칭해 삭제 시 오류 발생
- **해결**: `info` 클래스에서 예약된 탭 번호와 시간 정보를 기준으로 정확히 조회 후 삭제 처리

---

## 🧑‍💻 팀원 및 역할

| 이름       | 역할                            |
|------------|---------------------------------|
| 백준현       | 회로 설계 및 하드웨어 구축       |
| 김우재       | 문서 작성 및 발표자료 정리       |
| **오철환(본인)** | Android 앱 개발, 음성 인식 기능, 아두이노 연동 총괄 |

---

## 📂 프로젝트 자료

### 📄 문서 (`docs/` 폴더)

- [`SmartTap_계획서.pdf`](docs/SmartTap_계획서.pdf) – 초기 기획서
- [`SmartTap_발표자료.pdf`](docs/SmartTap_발표자료.pdf) – 발표용 슬라이드

### 🖼️ 이미지 (`images/` 폴더)

- [`회로도_전체.png`](images/회로도_전체.png) – 아두이노 + 릴레이 회로도
- [`앱_화면_캡처.png`](images/앱_화면_캡처.png) – 안드로이드 앱 UI

> ⚠️ 본 프로젝트는 2017년에 진행되었으며, 개발 완료 후 소스코드는 분실되어 포함되지 않았습니다.

---

## 🎓 프로젝트 정보

- **수행 시기:** 2017년 2학기
- **소속:** 소프트웨어학과 졸업작품
- **팀 구성:** 3인

---

## 🙋‍♂️ 담당자

> 본 README는 프로젝트 개발자 오철환이 정리하였습니다.
