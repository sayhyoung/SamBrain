---
# === 템플릿 메타데이터 (이 섹션은 실제 노트에 복사 안 됨) ===
type: template
target: area
status: approved
version: 1.0.0
compat:
  templater: ">=1.24.0"
  obsidian: ">=1.0.0"
changelog_url: "[[6. Templates/CHANGELOG]]"
superseded_by: ""
# ===============================================

# === 실제 노트 Frontmatter (아래부터 복사됨) ===
# PARA 규칙: created/updated/due/related 사용 금지 (OS 메타 file.ctime/file.mtime 활용)
type: area
status: active
# review_cycle: monthly
# tags: [area/operations]
---

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
