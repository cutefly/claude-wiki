# Wiki Log

Append-only record of all operations.

---

## 2026-05-10 — 전체 위키 재작성 (3개 소스 통합)

**Sources**:
- `obrasuperpowers An agentic skills framework & software development methodology that works..md`
- `VoltAgentawesome-claude-code-subagents A collection of 100+ specialized Claude Code subagents covering a wide range of development use cases.md`
- `🚀 12 Claude Skills Every👨🏻‍💻Developer Should Be Using Right Now.md`

**Pages deleted**:
- `agentic-skills.md` → `skill-md-pattern.md`으로 교체
- `coding-agent-workflows.md` → `superpowers-framework.md`에 통합

**Pages created**:
- `skill-md-pattern.md` — SKILL.md 4요소, Rigid/Flexible 구분, Skills vs Subagents 비교 (3개 소스 통합)
- `subagents.md` — 서브에이전트 개념 전체: 독립 컨텍스트, 파일 구조(frontmatter), 저장 위치, 도구 권한 (VoltAgent 소스)

**Pages rewritten**:
- `superpowers-framework.md` — 두 가지 확장 패턴 비교표·전체 워크플로우 다이어그램 추가, coding-agent-workflows 내용 흡수, Related pages 정리
- `subagent-driven-development.md` — 파손된 [[writing-plans]] 링크 수정, Related pages 정리
- `test-driven-development.md` — Related pages 정리 (agentic-skills → skill-md-pattern)
- `claude-code-subagents.md` — 카테고리별 에이전트 전체 목록 확장, Related pages 정리
- `model-routing.md` — Related pages 정리
- `developer-skills-catalog.md` — skill-md-pattern 링크 추가, 설명 개선
- `mcp.md` — mcp-developer 서브에이전트 추가 (VoltAgent 소스), 소스 2개로 확장
- `index.md` — 3섹션(개념·프레임워크·카탈로그) 구조로 전면 재편

---

## 2026-05-10 — Ingestion: 12 Claude Skills Every Developer Should Be Using Right Now

**Source**: `🚀 12 Claude Skills Every👨🏻‍💻Developer Should Be Using Right Now.md`

**Pages created**:
- `developer-skills-catalog.md` — 개발자용 12가지 Claude 스킬 카탈로그 (지식·문서, 메타, 프론트엔드, 백엔드/인프라, 아키텍처 도메인별 정리, 권장 도입 순서 포함)
- `mcp.md` — Model Context Protocol 개념, MCP 서버 구성 요소, MCP Builder 스킬 연결

**Pages updated**:
- `agentic-skills.md` — SKILL.md 파일 4요소(Role, Methodology, Constraints, Output format) 섹션 추가; 두 번째 소스 및 developer-skills-catalog 링크 추가
- `index.md` — Developer Skills 섹션 신설; developer-skills-catalog, mcp 추가

---

## 2026-05-08

**Ingested**: `obrasuperpowers An agentic skills framework & software development methodology that works..md`  
**Ingested**: `VoltAgentawesome-claude-code-subagents A collection of 100+ specialized Claude Code subagents covering a wide range of development use cases.md`

**Created pages**:
- `wiki/index.md` — 위키 전체 목차 (신규 생성)
- `wiki/log.md` — 작업 기록 (신규 생성)
- `wiki/superpowers-framework.md` — obra/superpowers 프레임워크 전체 개요
- `wiki/agentic-skills.md` — 에이전트 스킬 개념 (rigid vs flexible, 스킬 vs 서브에이전트 비교)
- `wiki/claude-code-subagents.md` — VoltAgent 100개+ 서브에이전트 컬렉션, 10개 카테고리, 구조 및 설치
- `wiki/subagent-driven-development.md` — SDD 워크플로우, 2단계 검토 프로세스
- `wiki/test-driven-development.md` — 에이전트 환경 TDD, RED-GREEN-REFACTOR
- `wiki/coding-agent-workflows.md` — 전반적 워크플로우 패턴, 두 가지 확장 패턴 비교
- `wiki/model-routing.md` — Opus/Sonnet/Haiku 라우팅 전략
