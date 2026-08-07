# 안녕하세요, 임대진(LimDaeJin-Agent)입니다 👋

AI 직무 전환을 목표로 공부하며, n8n 워크플로우 자동화와 프론트엔드 웹앱 프로젝트를 기록하고 있습니다.
이 프로필은 제가 GitHub에 올린 모든 프로젝트를 한눈에 볼 수 있도록 정리한 페이지입니다.

---

## 📋 프로젝트 전체 요약

| # | 프로젝트 | 생성일 | 최근 업데이트 | 주요 기술 | 한줄 요약 |
|---|---|---|---|---|---|
| 1 | [Mini_Project_2](https://github.com/LimDaeJin-Agent/Mini_Project_2) | 2026-08-07 | 2026-08-07 | n8n · Google Gemini | 매일 아침 금융 RSS를 수집·요약해 디스코드로 브리핑하는 자동화 에이전트 |
| 2 | [Mini_Project_1](https://github.com/LimDaeJin-Agent/Mini_Project_1) | 2026-08-07 | 2026-08-07 | n8n · Gemini · LangChain | 고객 문의(VOC)를 자동 분류·기록하고 긴급 건은 즉시 알림 발송하는 에이전트 |
| 3 | [eat-break-up](https://github.com/LimDaeJin-Agent/eat-break-up) | 2026-08-04 | 2026-08-04 | JavaScript · Gemini API | 수원 맛집 리스트 웹앱 고도화판 — 도장깨기 + AI 맞춤 추천 ([데모](https://limdaejin-agent.github.io/eat-break-up/)) |
| 4 | [eat_break](https://github.com/LimDaeJin-Agent/eat_break) | 2026-08-04 | 2026-08-04 | JavaScript | 수원 맛집 리스트 관리 웹앱 초기 버전 (CRUD·예약·알림) |
| 5 | [portfolio](https://github.com/LimDaeJin-Agent/portfolio) | 2026-07-29 | 2026-08-04 | HTML/CSS/JS | 개인 포트폴리오 페이지 ([데모](https://limdaejin-agent.github.io/portfolio/)) |
| 6 | [target-game](https://github.com/LimDaeJin-Agent/target-game) | 2026-07-29 | 2026-07-29 | HTML/CSS/JS | 어린이 대상 동물 과녁 맞추기 브라우저 게임 ([플레이](https://limdaejin-agent.github.io/target-game/)) |
| 7 | [AI-Agents-1M](https://github.com/LimDaeJin-Agent/AI-Agents-1M) | 2026-07-24 | 2026-07-24 | Markdown | AI 부트캠프 실습 기록 (강점 분석 등) |
| 8 | [TIL](https://github.com/LimDaeJin-Agent/TIL) | 2026-07-22 | 2026-07-22 | Markdown | Today I Learned — 매일 배운 내용 정리 |

---

## 📂 프로젝트 상세 설명

### 1. [Mini_Project_2](https://github.com/LimDaeJin-Agent/Mini_Project_2) — 금융 뉴스 브리핑 Agent
자산운용사 리서치팀이 매일 아침 여러 매체를 돌아다니며 금융 기사를 직접 찾아 읽는 비효율을 해결하기 위한 n8n 워크플로우입니다.
- 한국경제·매일경제·연합인포맥스·블룸버그통신·머니투데이 등 **5개 RSS**를 매일 08:30에 수집
- 기사 링크(URL)를 기준으로 구글 시트 이력과 대조해 **중복 발송 방지**
- 키워드 1차 필터 → Gemini 기반 AI Agent가 요약/중요도/카테고리를 JSON으로 구조화 출력 → 2차 안전망 필터
- 중요도 4 이상 기사만 Discord 임베드로 묶어 발송, 발송 이력은 구글 시트에 자동 기록
- 워크플로우 JSON 파일 포함 (n8n에서 바로 Import 가능)

### 2. [Mini_Project_1](https://github.com/LimDaeJin-Agent/Mini_Project_1) — 고객 VOC 분석 Agent
쇼핑몰에 하루 수십 건씩 들어오는 고객 문의를 사람이 일일이 읽고 분류하는 문제(담당자 부재 시 방치, 담당자마다 다른 분류 기준)를 해결하기 위한 n8n 워크플로우입니다.
- 구글 폼으로 접수된 문의를 **접수 → 중복 제거 → 분류 → 기록 → 알림** 전 과정 자동화
- Gemini + LangChain 기반 AI Agent가 문의 내용을 분석해 카테고리 분류
- 긴급 문의는 즉시 알림, 나머지는 표로 취합해 일괄 보고

### 3. [eat-break-up](https://github.com/LimDaeJin-Agent/eat-break-up) — 먹GO (고도화 버전)
[eat_break](https://github.com/LimDaeJin-Agent/eat_break)의 CRUD 완성 버전을 기반으로 **맛집 도장깨기**와 **Gemini AI 맞춤 추천** 기능을 추가한 버전입니다.
- 수원시 맛집을 대분류·소분류·상황(어르신/연인/친구/날씨)별로 탐색
- 메뉴 체크, 방문 예약, 방문일 알림, 맛집 도장깨기(스탬프) 기능
- Gemini AI에게 상황을 입력하면 맞춤 맛집을 추천받는 기능 추가
- 백엔드 서버 없이 브라우저 localStorage로 데이터 관리 (relational schema로 설계 문서화)
- **[라이브 데모 보기](https://limdaejin-agent.github.io/eat-break-up/)**

### 4. [eat_break](https://github.com/LimDaeJin-Agent/eat_break) — 먹GO (초기 버전)
`eat-break-up`의 베이스가 된 초기 버전으로, 수원 맛집 리스트를 카테고리·상황별로 탐색하고 메뉴 체크·방문 예약·알림까지 관리하는 여름 테마 반응형 웹앱입니다.

### 5. [portfolio](https://github.com/LimDaeJin-Agent/portfolio) — 개인 포트폴리오
개인 포트폴리오를 정리하는 페이지입니다. **[라이브 데모 보기](https://limdaejin-agent.github.io/portfolio/)**

### 6. [target-game](https://github.com/LimDaeJin-Agent/target-game) — 동물 과녁 맞추기 게임
어린이 대상의 밝고 재미있는 브라우저 과녁 맞추기 게임으로, 외부 라이브러리/서버 없이 단일 `index.html`로 동작합니다.
- 포인터 선택 → 옵션 설정(과녁 이미지, 효과음, 마우스 감도) → 게임 방법 안내 → 3-2-1 카운트다운 → 30초 게임 플레이(5x7 과녁판, 최대 동시 15개 과녁) → 결과/순위표
- 민첩도 테스트 모드 별도 제공
- **[플레이하기](https://limdaejin-agent.github.io/target-game/)**

### 7. [AI-Agents-1M](https://github.com/LimDaeJin-Agent/AI-Agents-1M) — AI 에이전트 부트캠프 학습 기록
AI 직무 전환을 위한 부트캠프 실습 기록입니다. AI와 함께 자신의 강점을 분석하는 실습(day01) 등을 정리했습니다.

### 8. [TIL](https://github.com/LimDaeJin-Agent/TIL) — Today I Learned
매일 배운 내용을 기록하는 학습 저장소입니다. Git/GitHub 사용법, Markdown 문법 연습 등을 담고 있습니다.

---

<sub>이 README는 GitHub 프로필 메인 화면에 표시되는 소개 페이지입니다.</sub>
