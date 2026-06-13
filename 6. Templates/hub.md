---
type: hub
# tags: []
---
<!-- TEMPLATE-META (생성된 노트에서 이 주석은 삭제) · 레지스트리 SSOT: [[6. Templates/CLAUDE]]
target: hub · status: approved · version: 1.0.0 · changelog: [[6. Templates/CHANGELOG]]
compat: templater >=1.24.0, obsidian >=1.0.0 · superseded_by: -
-->

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
