---
# PARA 규칙: created/updated/due/related 사용 금지 (OS 메타 file.ctime/file.mtime 활용)
type: area
status: active
# review_cycle: monthly
# tags: [area/operations]
---
<!-- TEMPLATE-META (생성된 노트에서 이 주석은 삭제) · 레지스트리 SSOT: [[6. Templates/CLAUDE]]
target: area · status: approved · version: 1.0.0 · changelog: [[6. Templates/CHANGELOG]]
compat: templater >=1.24.0, obsidian >=1.0.0 · superseded_by: -
-->

# <% tp.file.title %>

## 목적
<!-- 이 영역이 담당하는 책임과 역할 -->
<% tp.file.cursor(1) %>

## 현황
<!-- 현재 상태, 주요 지표, KPI 등 -->

## 관련 프로젝트 (자동 집계)
```dataview
TABLE status, due
FROM "1. Projects"
WHERE contains(area, this.file.name)
SORT due ASC
```

## 리뷰 로그
- <% tp.date.now("YYYY-MM-DD") %>:

## 참조
- [[3. Resources/]]
- [[5. Zettelkasten/]]
