# 4종 기능사 필기 CBT 기출문제 & 핵심 요약노트 통합 수험관

국가기술자격 4종 기능사(임베디드기능사, 정보기기운용기능사, 프로그래밍기능사, 웹디자인개발기능사)의 필기 기출문제 모의시험 및 2026년 개정 출제기준 단권화 요약노트를 제공하는 정적 웹 애플리케이션입니다. 빌드 과정 없이 GitHub Pages에서 바로 동작합니다.

🔗 **사이트 바로가기**: https://alicia6-6.github.io/Craftsman/index.html

---

## 📚 지원 종목

### 1. 임베디드기능사 (`embedded/`)
- **개정사항**: 전자계산기기능사 통합·개편, 2026년 신설된 **시스템소프트웨어 및 펌웨어구현** 전면 반영
- **문항 구성**: 60문항 60분 (기출 1,320문제, 22개 회차 수록)
- **주요 영역**: 전자회로, 컴퓨터구조, 디지털논리회로, 프로그래밍언어, 마이크로프로세서, 펌웨어/시스템SW

### 2. 정보기기운용기능사 (`infoeq/`)
- **개정사항**: 네트워크 엔지니어 실무형 전면 개편
- **문항 구성**: 60문항 60분 (기출 및 2026 개정 예상문제 360문제, 6개 회차 수록)
- **주요 영역**: 전기통신·OSI 7계층, LAN 구성, 스위치/라우터 구성(CLI), VLAN/ACL/NAT, 무선랜, 서버 가상화·클라우드

### 3. 프로그래밍기능사 (`programming/`)
- **개정사항**: 정보처리기능사 개편 기준, 실무 프로그래밍 역량 중심
- **문항 구성**: 60문항 60분 (기출 및 개정 실전 311문제, 21개 회차 수록)
- **주요 영역**: C/Java/Python 문법, SQL 데이터베이스, 객체지향 설계(OOP), 웹 기초(HTML/CSS/JS), 자료구조/알고리즘, SW 테스트·DevOps

### 4. 웹디자인개발기능사 (`webdesign/`)
- **개정사항**: 2025~2026년 신출제기준 반영 (UX/UI 및 웹 프론트엔드 표준)
- **문항 구성**: 60문항 60분 (기출 1,080문제, 18개 회차 및 단권화 요약노트 15장 완비)
- **주요 영역**: 디자인 원리·조형 요소, 색채학(조색/배색), 웹그래픽스, UX/UI·와이어프레임·사용성 평가, 웹 표준·저작권

---

## 🚀 주요 기능

- **회차별 실전 모의시험 (`quiz.html?mode=round`)**  
  실제 시험과 동일한 60분 타이머 + 60문항 답안 이동 맵(Navigator)을 통해 실전처럼 풀고 한 번에 자동 채점
- **랜덤 모드 (`quiz.html?mode=random`)**  
  전체 기출 풀에서 무작위로 한 문제씩 즉시 정답/해설 확인하며 가볍게 학습
- **빈출문제 모드 (`quiz.html?mode=frequent`)**  
  여러 회차에서 중복·유사 출제된 필수 문제만 자동으로 추출하여 압축 학습
- **오답노트 (`quiz.html?mode=wrong`)**  
  틀린 문제를 브라우저 `localStorage`에 자동 저장하고, 다시 맞히면 자동으로 제거되는 지능형 복습
- **단권화 요약노트 (`summary.html`)**  
  2026 최신 개정 출제기준을 반영한 핵심 개념, 암기 치트키, 기출 함정, 필수 표 정리

---

## 📁 프로젝트 폴더 구조

```text
Craftsman/
├── index.html                  # 4종 기능사 통합 메인 포털
├── css/style.css               # 공통 스타일 (라이트/다크 모드 지원)
├── js/theme.js                 # 다크모드 토글 스크립트
├── embedded/                   # [임베디드기능사]
│   ├── index.html / quiz.html / summary.html
│   ├── js/ (data.js, quiz.js, theme.js, summary-footnotes.js)
│   └── data/ (questions.json, images/)
├── infoeq/                     # [정보기기운용기능사]
│   ├── index.html / quiz.html / summary.html
│   ├── js/
│   └── data/ (questions.json)
├── programming/                # [프로그래밍기능사]
│   ├── index.html / quiz.html / summary.html
│   ├── js/
│   └── data/ (questions.json)
├── webdesign/                  # [웹디자인개발기능사]
│   ├── index.html / quiz.html / summary.html
│   ├── js/
│   └── data/ (questions.json)
└── cbt/                        # 국가자격 원본 기출문제(HWP) 및 출제기준 원문
```

---

## 💻 로컬 실행 방법

정적 HTML/CSS/JS로 구성되어 있어 간단한 로컬 웹 서버로 바로 실행할 수 있습니다:

```bash
# 파이썬 내장 웹 서버 실행
python -m http.server 8000

# 브라우저에서 http://localhost:8000 접속
```
*(참고: JSON 비동기 fetch를 수행하므로 로컬 웹 서버를 경유해야 합니다.)*
