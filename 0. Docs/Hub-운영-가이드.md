---
title: "Hub 운영 가이드"
doc_type: "howto"
created: "2025-06-13"
updated: "2025-06-13"
owner: "kamwoo"
summary: "폴더별 인덱스 허브(00_XXX_Hub.md)의 목적·명명·구성·유지보수 규칙"
scope: "전체 Vault의 Hub 노트"
audience: "본인"
keywords: ["hub", "index", "dataview", "navigation"]
related: ["CLAUDE.md", "6. Templates/CLAUDE.md"]
status: "active"
---

# Hub 운영 가이드

## Hub란
- 각 폴더의 **진입점(인덱스) 노트**. 폴더 내용을 Dataview로 집계하고 주요 링크를 모아 탐색을 돕는다.
- **1 폴더 = 1 Hub** 원칙. Hub는 콘텐츠 저장소가 아니라 길잡이다.

## 명명 규칙
- `00_<영역>_Hub.md` — 접두사 `00_`로 파일 탐색기 최상단에 정렬.
- 표준 이름:
  - `00_Projects_Hub.md` · `00_Areas_Hub.md` · `00_Resources_Hub.md`
  - `00_ZK_Hub.md` (Zettelkasten) · `00_Docs_Hub.md` · `00_Templates_Hub.md`
- 대형 프로젝트는 프로젝트 폴더 안에 `project-hub` 템플릿으로 별도 허브 운용.

## 생성
- 템플릿: `6. Templates/hub.md` (`type: hub`)
- 생성 후 Dataview 쿼리의 `FROM "..."` 경로를 담당 폴더로 수정.

## 구성 요소
1. **개요** — 폴더의 목적 한 줄
2. **집계 쿼리** — 최근/활성 항목 Dataview
3. **빠른 링크** — 자주 접근하는 핵심 노트 모음

## 폴더별 집계 쿼리 예시

### Projects (진행 중)
```dataview
TABLE status, due
FROM "1. Projects"
WHERE type = "project" AND status = "in-progress"
SORT due ASC
```

### Areas (활성)
```dataview
TABLE status, file.mtime as "최종 리뷰"
FROM "2. Areas"
WHERE type = "area" AND status = "active"
SORT file.mtime DESC
```

### Zettelkasten (최근 Permanent)
```dataview
TABLE updated, length(related) as "연결 수"
FROM "5. Zettelkasten/20. Permanent"
WHERE type = "permanent"
SORT updated DESC
LIMIT 10
```

## 유지보수
- **월 1회**: 쿼리 정상 작동 확인, 죽은 링크 정리.
- `type: hub`는 일반 노트 집계(`WHERE type != "hub"`)에서 제외되도록 쿼리 작성.
- Hub 자체는 본문 콘텐츠를 최소화 (링크/쿼리 중심 유지).

## Changelog
- 2025-06-13: 초기 작성 (Hub 명명·구성·유지보수 규칙 정의)
