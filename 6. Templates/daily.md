---
# === 템플릿 메타데이터 (이 섹션은 실제 노트에 복사 안 됨) ===
type: template
target: daily
status: approved
version: 1.0.0
compat:
  templater: ">=1.24.0"
  obsidian: ">=1.0.0"
changelog_url: "[[6. Templates/CHANGELOG]]"
superseded_by: ""
# ===============================================

# === 실제 노트 Frontmatter (아래부터 복사됨) ===
type: daily
created: <% tp.date.now("YYYY-MM-DD") %>
# tags: []
---

# <% tp.date.now("YYYY-MM-DD (ddd)") %>

## 오늘의 초점
-

## 할 일
- [ ]

## 메모 / 캡처
<!-- 발전시킬 생각은 [[5. Zettelkasten/00. Inbox/...]]로 이동 -->
-

## 로그
-

## 회고
-

---
어제: [[<% tp.date.now("YYYY-MM-DD", -1) %>]] · 내일: [[<% tp.date.now("YYYY-MM-DD", 1) %>]]
