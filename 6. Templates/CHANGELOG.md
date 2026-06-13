# Templates CHANGELOG

> 템플릿 변경 이력 통합 문서. 운영 규칙: [[6. Templates/CLAUDE]]
> 형식: `## YYYY-MM-DD - <파일> v<버전>` + 변경 사항 / 마이그레이션 가이드 / Breaking Changes

## 2025-06-13 - Frontmatter 포맷 전환 (10개 템플릿)

### 변경 사항
- 기존 "2중 Frontmatter 블록"(한 YAML에 `type: template` + 실제 `type` 동시 기재) → **Frontmatter는 실제 노트 FM만, 템플릿 메타데이터는 본문 상단 `TEMPLATE-META` HTML 주석**으로 분리
- 대상 10개: project, project-hub, area, resource, literature, permanent, docs, archive, daily, hub
- `6. Templates/CLAUDE.md` 규격·예시·검증 대시보드·작업지침·안티패턴을 새 포맷에 맞게 갱신

### 사유 (왜)
- 한 YAML 블록에 `type` 중복 키 → Obsidian이 뒤 값으로 해석하여 생성된 노트의 `type`이 깨지고, `WHERE type="template"` 대시보드도 오작동

### 마이그레이션 가이드
- 생성된 기존 노트 없음 → 영향 없음
- 신규: 노트 생성 후 본문 상단 `TEMPLATE-META` 주석 삭제

### Breaking Changes
- 템플릿 파일 구조 변경(메타데이터 위치 이동). 단, 생성되는 노트의 결과 FM은 동일하므로 노트 호환성 영향 없음

## 2025-06-13 - 템플릿 시스템 초기 구축

### 변경 사항
- 레지스트리에 정의돼 있던 8개 템플릿 신규 생성:
  - `project` v1.2.0, `project-hub` v1.1.0, `area` v1.0.0, `resource` v1.0.0,
    `literature` v1.2.0, `permanent` v1.2.0, `docs` v1.0.0, `archive` v1.0.0
- 신규 템플릿 2종 추가:
  - `daily` v1.0.0 (Daily Notes 코어 플러그인 연계), `hub` v1.0.0 (폴더 인덱스 허브)
- 각 템플릿은 해당 폴더 CLAUDE.md의 Frontmatter 규칙을 반영
  - PARA(project/area/resource/archive): `created`/`updated` 미사용 (OS 메타)
  - ZK(literature/permanent): `created`/`updated` 사용 (지식 진화 추적)
- 누락 문서 [[0. Docs/Hub-운영-가이드]] 생성 (모든 폴더 CLAUDE.md가 참조)

### 마이그레이션 가이드
- 기존 노트 없음 (최초 구축) → 영향 없음

### Breaking Changes
- 없음
