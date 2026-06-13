---
# === 템플릿 메타데이터 (이 섹션은 실제 노트에 복사 안 됨) ===
type: template
target: permanent
status: approved
version: 1.2.0
compat:
  templater: ">=1.24.0"
  obsidian: ">=1.0.0"
changelog_url: "[[6. Templates/CHANGELOG]]"
superseded_by: ""
# ===============================================

# === 실제 노트 Frontmatter (아래부터 복사됨) ===
# ZK 규칙: created/updated 사용, related 최소 2개 이상(고아 노트 방지), due/source/author 금지
type: permanent
status: active
created: <% tp.date.now("YYYY-MM-DD") %>
updated: <% tp.date.now("YYYY-MM-DD") %>
tags: []
related: []
---

# <% tp.file.title %>

> 영구 노트 — 하나의 명확한 주장(One Idea per Note). 제목이 곧 주장.

## 주장 / 핵심 아이디어
<% tp.file.cursor(1) %>

## 근거 / 전개
<!-- 내 언어로 재구성 -->

## 연결
<!-- 최소 2개 이상 다른 노트와 연결하고 위 related[] 필드에도 명시 -->
- [[]] 와의 관계:
- [[]] 와의 관계:

## 출처
<!-- Permanent는 본문에 출처 표기 (source/author 필드는 사용 금지) -->
-
