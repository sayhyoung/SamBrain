---
# === 템플릿 메타데이터 (이 섹션은 실제 노트에 복사 안 됨) ===
type: template
target: hub
status: approved
version: 1.0.0
compat:
  templater: ">=1.24.0"
  obsidian: ">=1.0.0"
changelog_url: "[[6. Templates/CHANGELOG]]"
superseded_by: ""
# ===============================================

# === 실제 노트 Frontmatter (아래부터 복사됨) ===
type: hub
# tags: []
---

# <% tp.file.title %>

> 폴더 인덱스 허브(`00_XXX_Hub.md`). 운영 규칙: [[0. Docs/Hub-운영-가이드]]
> 아래 Dataview의 `FROM "..."` 경로를 이 허브가 담당하는 폴더로 수정해서 사용.

## 개요
<% tp.file.cursor(1) %>

## 최근 항목 (자동 집계)
```dataview
TABLE status, file.mtime as "최종 수정"
FROM "1. Projects"
WHERE type != "template" AND type != "hub" AND file.name != this.file.name
SORT file.mtime DESC
LIMIT 20
```

## 빠른 링크
-
