---
type: archive
status: archived
archived_date: <% tp.date.now("YYYY-MM-DD") %>
original_folder: "1. Projects"   # 1. Projects | 2. Areas | 3. Resources | 0. Docs
# completed_date:                 # Projects만 선택적
return_candidates: ["1. Projects", "2. Areas", "3. Resources", "5. Zettelkasten"]
return_target: "none"            # 1. Projects | 2. Areas | 3. Resources | 5. Zettelkasten | none
recyclable: partial              # yes | no | partial
# tags: [archive/project]
---
<!-- TEMPLATE-META (생성된 노트에서 이 주석은 삭제) · 레지스트리 SSOT: [[6. Templates/CLAUDE]]
target: archive · status: approved · version: 1.0.0 · changelog: [[6. Templates/CHANGELOG]]
compat: templater >=1.24.0, obsidian >=1.0.0 · superseded_by: -
-->

# <% tp.file.title %>

> ⚠️ Append Only — Archive 파일은 수정하지 않음 (재활용 시 복사 후 새 파일로 작업)

## 보관 사유
<!-- 왜 Archive로 이동했는가? -->
<% tp.file.cursor(1) %>

## 원본 정보
- Original folder: [[]]
- Archived: <% tp.date.now("YYYY-MM-DD") %>

## 복귀 계획
- 복귀 대상:
- 재활용 가능 여부:
- 복귀 시점: 필요 시
