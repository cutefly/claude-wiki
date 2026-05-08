# Claude Code Subagents

**Summary**: 서브에이전트는 특정 개발 태스크를 위해 격리된 컨텍스트에서 동작하는 특화 AI 어시스턴트로, VoltAgent 컬렉션은 100개+ 서브에이전트를 제공한다.

**Sources**: `VoltAgentawesome-claude-code-subagents A collection of 100+ specialized Claude Code subagents covering a wide range of development use cases.md`

**Last updated**: 2026-05-08

---

## 개념

서브에이전트는 Claude Code가 특정 유형의 작업을 만났을 때 호출하는 전문 AI 어시스턴트다. 각 서브에이전트는 자신의 독립적인 컨텍스트 윈도우를 가지고 있어, 주 대화 스레드가 태스크 세부사항으로 오염되지 않는다. (source: VoltAgentawesome...)

## 핵심 특성

**독립 컨텍스트 윈도우**  
각 서브에이전트는 격리된 컨텍스트 공간에서 동작한다. 서로 다른 태스크 간 교차 오염을 방지하고 주 대화를 깔끔하게 유지한다.

**도메인 특화 지능**  
전문 분야에 맞게 세심하게 설계된 지침을 갖추고 있어 특화 태스크에서 더 나은 결과를 낸다.

**프로젝트 간 공유 가능**  
서브에이전트를 한 번 만들면 여러 프로젝트에서 사용하고 팀원들과 공유할 수 있어 일관된 개발 방식을 보장한다.

**세밀한 도구 권한**  
각 서브에이전트에 특정 도구 접근 권한을 부여할 수 있어 역할 유형에 따라 어떤 기능을 사용할 수 있는지 세밀하게 제어한다. (source: VoltAgentawesome...)

## VoltAgent 컬렉션 카테고리

### 01. Core Development (`voltagent-core-dev`)
일상적인 코딩 태스크를 위한 필수 서브에이전트.
api-designer, backend-developer, frontend-developer, fullstack-developer, microservices-architect, mobile-developer 등 11개

### 02. Language Specialists (`voltagent-lang`)
언어별 깊은 프레임워크 지식을 갖춘 전문가.
typescript-pro, python-pro, golang-pro, rust-engineer, java-architect, react-specialist, nextjs-developer, flutter-expert 등 29개

### 03. Infrastructure (`voltagent-infra`)
DevOps, 클라우드, 배포 전문가.
cloud-architect, kubernetes-specialist, terraform-engineer, devops-engineer, docker-expert, sre-engineer 등 16개

### 04. Quality & Security (`voltagent-qa-sec`)
테스팅, 보안, 코드 품질 전문가.
code-reviewer, security-auditor, qa-expert, penetration-tester, chaos-engineer, performance-engineer 등 16개

### 05. Data & AI (`voltagent-data-ai`)
데이터 엔지니어링, ML, AI 전문가.
ai-engineer, data-scientist, machine-learning-engineer, llm-architect, mlops-engineer, nlp-engineer 등 13개

### 06. Developer Experience (`voltagent-dev-exp`)
툴링 및 개발자 생산성 전문가.
documentation-engineer, git-workflow-manager, refactoring-specialist, legacy-modernizer, mcp-developer 등 14개

### 07. Specialized Domains (`voltagent-domains`)
특정 도메인 기술 전문가.
blockchain-developer, game-developer, iot-engineer, fintech-engineer, embedded-systems 등 13개

### 08. Business & Product (`voltagent-biz`)
제품 관리 및 비즈니스 분석.
product-manager, technical-writer, business-analyst, scrum-master, ux-researcher 등 12개

### 09. Meta & Orchestration (`voltagent-meta`)
에이전트 조율 및 메타 프로그래밍.
agent-organizer, multi-agent-coordinator, workflow-orchestrator, codebase-orchestrator 등 14개

### 10. Research & Analysis (`voltagent-research`)
리서치, 검색, 분석 전문가.
research-analyst, competitive-analyst, market-researcher, trend-analyst 등 8개

(source: VoltAgentawesome...)

## 서브에이전트 구조

```
---
name: subagent-name
description: 언제 이 에이전트가 호출되어야 하는지
tools: Read, Write, Edit, Bash, Glob, Grep
model: sonnet
---

You are a [역할 설명]...
[에이전트 특화 체크리스트, 패턴, 가이드라인]
```

## [[model-routing|스마트 모델 라우팅]]

각 서브에이전트는 `model` 필드로 적절한 Claude 모델로 자동 라우팅된다. (source: VoltAgentawesome...)

- **opus** — 심층 추론이 필요한 작업 (security-auditor, architect-reviewer, fintech-engineer)
- **sonnet** — 일상적인 코딩 (python-pro, backend-developer, devops-engineer)
- **haiku** — 빠른 작업 (documentation-engineer, seo-specialist, build-engineer)

`model: inherit` 설정 시 주 대화와 동일한 모델 사용.

## 도구 할당 철학

- **읽기 전용 에이전트** (검토자, 감사자): `Read, Grep, Glob` — 수정 없이 분석
- **리서치 에이전트**: `Read, Grep, Glob, WebFetch, WebSearch` — 정보 수집
- **코드 작성 에이전트**: `Read, Write, Edit, Bash, Glob, Grep` — 생성 및 실행
- **문서화 에이전트**: `Read, Write, Edit, Glob, Grep, WebFetch, WebSearch` — 리서치 포함 문서화

(source: VoltAgentawesome...)

## 저장 위치

| 유형 | 경로 | 범위 | 우선순위 |
|---|---|---|---|
| 프로젝트 서브에이전트 | `.claude/agents/` | 현재 프로젝트만 | 높음 |
| 전역 서브에이전트 | `~/.claude/agents/` | 모든 프로젝트 | 낮음 |

이름 충돌 시 프로젝트 특화 서브에이전트가 전역 서브에이전트를 오버라이드한다.

## 설치

```bash
claude plugin marketplace add VoltAgent/awesome-claude-code-subagents
claude plugin install voltagent-core-dev   # Core Development
claude plugin install voltagent-lang       # Language specialists
claude plugin install voltagent-infra      # Infrastructure & DevOps
```

## Related pages

- [[agentic-skills]]
- [[model-routing]]
- [[subagent-driven-development]]
- [[superpowers-framework]]
- [[coding-agent-workflows]]
