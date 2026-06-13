---
# === 템플릿 메타데이터 (이 섹션은 실제 노트에 복사 안 됨) ===
type: template
target: doc
status: approved
version: 1.0.0
compat:
  templater: ">=1.24.0"
  obsidian: ">=1.0.0"
changelog_url: "[[6. Templates/CHANGELOG]]"
superseded_by: ""
# ===============================================

# === 실제 노트 Frontmatter (0. Docs 스키마, 아래부터 복사됨) ===
title: '<% tp.file.title %>'
doc_type: 'policy'   # policy | procedure | howto | reference | decision
created: '<% tp.date.now("YYYY-MM-DD") %>'
updated: '<% tp.date.now("YYYY-MM-DD") %>'
owner: 'kamwoo'
summary: ''
scope: ''
audience: '본인'
keywords: []
related: []
status: 'active'     # active | deprecated
---

# <% tp.file.title %>

## 개요
<% tp.file.cursor(1) %>

## 내용

## Changelog
- <% tp.date.now("YYYY-MM-DD") %>: 초기 작성
