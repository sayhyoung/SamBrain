---
# === 템플릿 메타데이터 (이 섹션은 실제 노트에 복사 안 됨) ===
type: template
target: project
status: approved
version: 1.1.0
compat:
  templater: ">=1.24.0"
  obsidian: ">=1.0.0"
changelog_url: "[[6. Templates/CHANGELOG]]"
superseded_by: ""
# ===============================================

# === 실제 노트 Frontmatter (아래부터 복사됨) ===
type: project
status: in-progress
due: <% tp.date.now("YYYY-MM-DD", 30) %>
# area: <% tp.file.cursor(1) %>
# tags: []
---

# <% tp.file.title %> — Hub

> 대형/다학제 프로젝트 허브. 하위 노트는 `1. Projects/<% tp.file.title %>/` 폴더에 두고 여기서 집계.
> Hub 운영 규칙: [[0. Docs/Hub-운영-가이드]]

## 목표(Outcome)
<% tp.file.cursor(2) %>

## 완료 기준(Definition of Done)
- [ ]

## 구성 / 하위 작업 (자동 집계)
```dataview
TABLE status, due, file.mtime as "최종 수정"
FROM "1. Projects/<% tp.file.title %>"
WHERE type = "project" AND file.name != this.file.name
SORT due ASC
```

## 마일스톤
- <% tp.date.now("YYYY-MM-DD", 14) %>:
- <% tp.date.now("YYYY-MM-DD", 30) %>:

## 리스크 & 대응
- 리스크: ... / 대응: ...

## 진행 로그
- <% tp.date.now("YYYY-MM-DD") %>:

## 참조
- [[2. Areas/]]
- 자료: [[]] · 문헌: [[]]
