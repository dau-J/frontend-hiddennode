# HiddenNode 프로젝트

> **잊힌 이름, 숨겨진 기록**  
> 판결문 기반 독립운동 인물·사건의 시각화 플랫폼

---

## 🔍 프로젝트 개요

HiddenNode는 일제강점기 **판결문 속 인물·사건·장소 정보를 구조화**하고,  
**지식그래프 기반 시각화**를 통해 잊힌 독립운동 기록을 되살리는 웹 애플리케이션입니다.

- STI(Semantic Table Interpretation)를 활용한 의미 관계 추출
- 시각적 탐색이 가능한 UI 구성
- 독립운동사 데이터 기반 지식그래프 탐색

---

## 🖼️ 메인 화면 구성

| 섹션 | 설명 |
|------|------|
| Hero Section | 배경 이미지 + 탐색 버튼 |
| 판결문 소개 | 판결문의 중요성 설명 |
| 3단계 카드 섹션 | 데이터 정규화 → 지식그래프 → 탐색 방식 소개 |
| 시각화 사례 | 특정 인물의 판결문 기반 탐색 사례 소개 |
| 팀 소개 & 철학 | HiddenNode 팀과 프로젝트 방향성 설명 |
| Stepper Section | 기능 단계별 안내 섹션 |

---

## 🧭 그래프 페이지 화면 구성

| 섹션 | 설명 |
|------|------|
| 상단 툴바 | 그래프 리셋, 확대, 축소, 중심 이동 등 탐색 기능 버튼 |
| 데이터셋 전환 버튼 | 다양한 JSON 데이터셋 간 전환 지원 (코드 내 파일명 지정) |
| 검색/자동완성 | 노드 이름 검색 및 자동완성, 검색 시 그래프 하이라이트 및 카메라 이동 |
| 시각화 영역 | sigma.js 기반 지식그래프 시각화. 노드 클릭 시 정보 표시 |
| 사이드바 | 선택한 노드(인물, 사건 등)에 대한 주요 정보(주소, 년도, 이름, 죄명, 사건개요) 및 관계 정보(이웃 노드 이름) 표시 |
| 토글 버튼 | 사이드바를 열고 닫는 toggle 버튼 제공 |

> 그래프 페이지 역시 **반응형**으로 설계되어 데스크탑 및 태블릿 화면에서 최적화된 시각 탐색을 지원합니다.

---

## 🗂️ 자료실 화면 구성

| 섹션 | 설명 |
|------|------|
| 상단 제목 | 자료실 페이지 타이틀 및 간단 설명 |
| 테이블 헤더 | 사건명, 작성자, 조회수, 날짜 등 컬럼명 표시 |
| 테이블 본문 | 독립운동 사건별 데이터(사건명, author, views, id, date 등) 행 단위로 출력 |
| 페이지네이션(선택) | 자료가 많을 경우 페이지 이동 버튼 제공 |

> 자료실 화면은 독립운동 사건별 판결문 요약, 작성자(teamhiddennode), 조회수, 날짜 등 주요 정보를 표 형태로 제공합니다.

---

## ⚡ 주요 기능 (그래프 페이지)

- **대용량 JSON 데이터셋 동적 import 및 SSR-safe 시각화**
- **sigma.js/graphology** 기반 노드/엣지 무결성 처리
- **노드 선택 시 사이드바에 고정된 주요 정보(주소, 년도, 이름, 죄명, 사건개요)만 표시**
- **관계 정보(이웃 노드)는 이름만 간결하게 표시**
- **데이터셋 전환 버튼**으로 다양한 그래프 탐색 (코드 내 파일명 지정)
- **검색/자동완성**: 노드 이름 검색, 하이라이트, 카메라 이동
- **사이드바/검색 UX**: X버튼 클릭 시에만 정보 초기화, 검색창 blur/외부클릭 시 정보 유지
- **다크테마 최적화**: 검색 입력창, X아이콘, 텍스트 컬러 등 시인성 개선
- **SSR-safe**: Next.js App Router 환경에서 안전하게 동작


---

## 🛠️ 기술 스택

- **Next.js (App Router)**
- **Tailwind CSS**
- **Radix UI + ShadCN**
- **sigma.js, graphology**
- **Dynamic Import** for SSR control

---

## 🧩 Figma 프로토타입

디자인은 Figma를 기반으로 제작되었습니다.

[🖼️ Figma 프로토타입 보기](https://www.figma.com/design/nUWkq3RUz0uDMKt7DdBsbx/%EB%8F%85%EB%A6%BD%ED%8C%90%EA%B2%B0%EB%AC%B8?node-id=168-412&p=f&t=YUW3n9AmeuGdd019-0)

---

## 📦 GitHub 저장소

- [🔗 HiddenNode 프론트엔드 GitHub 바로가기](https://github.com/dau-J/frontend-hiddennode.git)

---

## 🚀 배포 및 실행 방법

```bash
git clone https://github.com/Donga-SW/frontend.git
cd frontend
npm install
npm run dev
```

# requirements
-----------------------------------------------------------------------
npm install next react react-dom --legacy-peer-deps <br>
npm install sigma graphology --legacy-peer-deps <br>
npm install graphology-serialization --legacy-peer-deps<br>
npm install -D @types/react @types/react-dom --legacy-peer-deps
------------------------------------------------------------------------
