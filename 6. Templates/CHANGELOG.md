# Templates CHANGELOG

> 템플릿 변경 이력 통합 문서. 운영 규칙: [[6. Templates/CLAUDE]]
> 형식: `## YYYY-MM-DD - <파일> v<버전>` + 변경 사항 / 마이그레이션 가이드 / Breaking Changes

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
