---
# === 템플릿 메타데이터 (이 섹션은 실제 노트에 복사 안 됨) ===
type: template
target: literature
status: approved
version: 1.2.0
compat:
  templater: ">=1.24.0"
  obsidian: ">=1.0.0"
changelog_url: "[[6. Templates/CHANGELOG]]"
superseded_by: ""
# ===============================================

# === 실제 노트 Frontmatter (아래부터 복사됨) ===
# ZK 규칙: created/updated 사용(지식 진화 추적), related 금지
type: literature
status: active
created: <% tp.date.now("YYYY-MM-DD") %>
updated: <% tp.date.now("YYYY-MM-DD") %>
source: ""
author: ""
# tags: [literature]
---

# <% tp.file.title %>

> 문헌 노트 — 저자의 생각을 **객관적으로** 요약 (내 해석/통찰은 Permanent로 분리)

## 출처
- Source:
- Author:

## 핵심 요약 (저자의 주장)
<% tp.file.cursor(1) %>

## 주요 인용
>

## 메모
<!-- 떠오른 내 생각은 [[5. Zettelkasten/20. Permanent/...]]로 승격 -->
-
