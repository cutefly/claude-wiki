# Superpowers Framework

**Summary**: obra/superpowers는 코딩 에이전트를 위한 완전한 소프트웨어 개발 방법론으로, 자동으로 발동되는 스킬 시스템을 중심으로 설계되었다.

**Sources**: `obrasuperpowers An agentic skills framework & software development methodology that works..md`

**Last updated**: 2026-05-08

---

## 개요

Superpowers는 Claude Code, Codex, Gemini CLI 등 다양한 코딩 에이전트 위에서 동작하는 방법론 레이어다. 에이전트가 즉흥적으로 코드를 작성하는 대신, 체계적인 스킬들이 자동으로 발동되어 소프트웨어 개발의 각 단계를 구조화한다. (source: obrasuperpowers...)

핵심 아이디어는 **에이전트가 특별한 지시 없이도 올바른 방식으로 동작하게 만드는 것**이다. 스킬이 자동으로 트리거되므로 개발자는 별도 조작 없이 방법론의 혜택을 누린다.

## 기본 워크플로우

1. **[[agentic-skills#brainstorming|brainstorming]]** — 코드 작성 전 소크라테스식 대화로 요구사항 명확화, 대안 탐색, 설계 문서 저장
2. **using-git-worktrees** — 설계 승인 후 새 브랜치에 격리된 작업 공간 생성, 프로젝트 셋업, 기준 테스트 검증
3. **writing-plans** — 승인된 설계를 2-5분 단위 태스크로 분해. 각 태스크에 정확한 파일 경로, 완전한 코드, 검증 단계 포함
4. **[[subagent-driven-development]]** 또는 **executing-plans** — 계획 실행. 서브에이전트 방식(2단계 검토)이나 체크포인트가 있는 일괄 실행
5. **[[test-driven-development]]** — RED-GREEN-REFACTOR 사이클 강제
6. **requesting-code-review** — 각 태스크 간 계획 준수 여부 검토, 심각도별 이슈 보고
7. **finishing-a-development-branch** — 태스크 완료 후 테스트 검증, 머지/PR/유지/폐기 옵션 제시

## 스킬 라이브러리

### 테스팅
- **test-driven-development** — RED-GREEN-REFACTOR 사이클 (테스팅 안티패턴 레퍼런스 포함)

### 디버깅
- **systematic-debugging** — 4단계 근본 원인 분석 프로세스
- **verification-before-completion** — 실제로 수정되었는지 확인

### 협업
- **brainstorming** — 소크라테스식 설계 정제
- **writing-plans** — 상세 구현 계획
- **executing-plans** — 체크포인트가 있는 일괄 실행
- **dispatching-parallel-agents** — 병렬 서브에이전트 워크플로우
- **requesting-code-review / receiving-code-review** — 코드 검토 요청 및 응답
- **using-git-worktrees** — 병렬 개발 브랜치 관리
- **finishing-a-development-branch** — 머지/PR 결정 워크플로우
- **[[subagent-driven-development]]** — 빠른 반복과 2단계 검토

### 메타
- **writing-skills** — 새 스킬 생성 가이드
- **using-superpowers** — 스킬 시스템 소개

## 철학

- **TDD 우선** — 항상 테스트를 먼저 작성
- **체계적 접근** — 추측이 아닌 프로세스
- **복잡성 감소** — 단순성이 최우선 목표
- **증거 기반** — 성공 선언 전에 검증

(source: obrasuperpowers...)

## 설치

Claude Code의 공식 플러그인 마켓플레이스에서 설치 가능하다:
```
/plugin install superpowers@claude-plugins-official
```

또는 Superpowers 마켓플레이스를 통해:
```
/plugin marketplace add obra/superpowers-marketplace
/plugin install superpowers@superpowers-marketplace
```

Codex, Gemini CLI, Cursor, Copilot CLI 등 다른 에이전트에도 각각의 설치 방법이 있다.

## Related pages

- [[agentic-skills]]
- [[subagent-driven-development]]
- [[test-driven-development]]
- [[coding-agent-workflows]]
- [[claude-code-subagents]]
