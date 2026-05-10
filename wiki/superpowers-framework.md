# Superpowers Framework

**Summary**: obra/superpowers는 코딩 에이전트를 위한 완전한 소프트웨어 개발 방법론이다. [[skill-md-pattern|SKILL.md 스킬]]들이 자동으로 발동되어 브레인스토밍부터 완료까지 7단계 워크플로우를 구조화하며, Claude Code·Codex·Gemini CLI 등 다양한 에이전트에 설치할 수 있다.

**Sources**: `obrasuperpowers An agentic skills framework & software development methodology that works..md`

**Last updated**: 2026-05-10

---

## 개요

Superpowers는 코딩 에이전트 위에서 동작하는 방법론 레이어다. 에이전트가 즉흥적으로 코드를 작성하는 대신, 스킬들이 자동으로 발동되어 소프트웨어 개발의 각 단계를 구조화한다. (source: obrasuperpowers...)

핵심 아이디어: **에이전트가 특별한 지시 없이도 올바른 방식으로 동작하게 만드는 것.** 스킬이 자동으로 트리거되므로 개발자는 별도 조작 없이 방법론의 혜택을 누린다.

## 두 가지 에이전트 확장 패턴

Superpowers는 에이전트 생태계의 두 가지 보완적 접근법 중 하나다.

| | Superpowers (스킬 기반) | [[claude-code-subagents\|VoltAgent]] (에이전트 기반) |
|---|---|---|
| 핵심 질문 | HOW to work | WHO does the work |
| 동작 방식 | 자동으로 발동되는 행동 지침 | 도메인 특화 전문가 에이전트 |
| 목적 | 개발 방법론 전체 구조화 | 특정 기술 영역의 깊은 전문성 |

두 접근법은 함께 사용할 때 가장 강력하다. Superpowers 스킬로 워크플로우를 구조화하고, VoltAgent 서브에이전트로 각 단계의 전문성을 높인다.

## 전체 워크플로우

```
사용자 요청
    ↓
1. [brainstorming]      요구사항 명확화, 설계 대안 탐색, 설계 문서 저장
    ↓
2. [using-git-worktrees] 격리된 작업 공간 생성, 기준 테스트 검증
    ↓
3. [writing-plans]      2-5분 단위 태스크로 분해 (파일 경로·코드·검증 포함)
    ↓
4. [SDD / executing-plans] 서브에이전트 파견 또는 일괄 실행
    ↓
5. [test-driven-development] RED-GREEN-REFACTOR 강제
    ↓
6. [requesting-code-review] 스펙 준수·코드 품질 검토
    ↓
7. [finishing-a-development-branch] 머지/PR/유지/폐기 결정
```

(source: obrasuperpowers...)

## 스킬 라이브러리

### 테스팅
- **[[test-driven-development]]** — RED-GREEN-REFACTOR 사이클 (안티패턴 레퍼런스 포함)

### 디버깅
- **systematic-debugging** — 4단계 근본 원인 분석 프로세스
- **verification-before-completion** — 실제로 수정되었는지 확인

### 협업
- **brainstorming** — 소크라테스식 설계 정제
- **writing-plans** — 상세 구현 계획 (2-5분 단위 태스크)
- **executing-plans** — 체크포인트가 있는 일괄 실행
- **[[subagent-driven-development]]** — 서브에이전트 파견 + 2단계 검토
- **dispatching-parallel-agents** — 독립 태스크 병렬 실행
- **requesting-code-review** / **receiving-code-review** — 코드 검토 요청 및 응답
- **using-git-worktrees** — 병렬 개발 브랜치 관리
- **finishing-a-development-branch** — 머지/PR 결정 워크플로우

### 메타
- **writing-skills** — 새 스킬 생성 가이드
- **using-superpowers** — 스킬 시스템 소개

## 철학

- **TDD 우선** — 항상 테스트를 먼저 작성
- **체계적 접근** — 추측이 아닌 프로세스
- **단순성** — YAGNI, 복잡성 감소가 최우선 목표
- **증거 기반** — 성공 선언 전에 실제 검증

(source: obrasuperpowers...)

## 설치

에이전트마다 별도 설치가 필요하다.

### Claude Code

```bash
# 공식 마켓플레이스
/plugin install superpowers@claude-plugins-official

# Superpowers 마켓플레이스
/plugin marketplace add obra/superpowers-marketplace
/plugin install superpowers@superpowers-marketplace
```

### 기타 에이전트

| 에이전트 | 설치 명령 |
|---|---|
| Codex CLI | `/plugins` → superpowers 검색 → Install Plugin |
| Gemini CLI | `gemini extensions install https://github.com/obra/superpowers` |
| Cursor | `/add-plugin superpowers` |
| GitHub Copilot CLI | `copilot plugin install superpowers@superpowers-marketplace` |

## Related pages

- [[skill-md-pattern]]
- [[subagent-driven-development]]
- [[test-driven-development]]
- [[claude-code-subagents]]
- [[subagents]]
- [[model-routing]]
