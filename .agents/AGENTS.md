# 🤖 Antigravity AI 워크스페이스 에이전트 지침 (AGENTS.md)

이 지침 파일은 **Antigravity AI가 이 워크스페이스(프로젝트)를 열 때 자동으로 감지하고 로드하는 프로젝트 전용 커스텀 규칙 문서**입니다.

---

## 📌 1. 빠른 프롬프트 명령어 (Prompt Shortcuts)
사용자가 다음과 같은 구문이나 프롬프트를 입력하면 아래 동작을 즉시 수행합니다:

* **`"프롬프트 불러와"`** 또는 **`"프롬프트 보여줘"`**:
  - 프로젝트 관리용 핵심 프롬프트 지시어 및 명령어 목록(`PROMPT_GUIDE.md` 및 `TEMP_DATA_LOG.md`)을 사용자에게 간결하게 출력합니다.

* **`"TEMP_DATA_LOG.md 파일 읽고 현재 대시보드에 반영된 임시 데이터 현황 확인해줘"`**:
  - [TEMP_DATA_LOG.md](file:///c:/Users/user/Desktop/AI%20Coding/06%20KCCENC-KMI-Dashboard-Roughdraft-main/KCCENC-KMI-Dashboard-Roughdraft-main/TEMP_DATA_LOG.md) 파일 전체를 읽어서 현재 대시보드 및 엑셀(`외주구매 백데이터.xlsx`)에 반영된 4가지 주요 임시(Mock) 데이터 목록과 교체 가이드를 정리하여 보고합니다.

---

## 📋 2. 임시(Mock) 데이터 현황 요약
1. **`02.03.02` 2024년(전기) 신용/현금흐름 등급**: `외주구매 백데이터.xlsx` M, N, O, P 열 (711개사 85% 유지 15% 미세조정)
2. **자재 단가계약 변동시점 현장 손실 영향액**: `index.html` 2.1 우측 패널 (레미탈, 케이블, 시멘트, 석고보드, 강관류 추정 손실액)
3. **1억원 이상 자재/하도급 입찰계약 절감액 리스트**: `index.html` 2.2 우측 패널 (`CONTRACT_BD` 객체 8개 계약건 억 단위 데이터)
4. **자재별 2020~2026년 단가 인덱스**: `index.html` 2.1 좌측 차트 (`MAT_DATA` 객체 범례 클릭 인터랙티브 차트)

---

## 🛠 3. 대시보드 구조 및 배포 원칙
- **주요 데이터 파일**: `index.html` 내 자바스크립트 객체(`GONGJEONG`, `JAGEUM`, `IIK`, `UNYEONG`) 및 `renderCustom21`, `renderCustom22`
- **검증 규칙**: `index.html` 수정 후 반드시 `node --check`로 script 구문 오류 100% 검증 후 Git Commit & Push 진행
