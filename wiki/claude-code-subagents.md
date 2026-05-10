# Claude Code Subagents (VoltAgent 컬렉션)

**Summary**: VoltAgent/awesome-claude-code-subagents는 100개+ 특화 서브에이전트를 10개 카테고리로 제공하는 오픈소스 컬렉션이다. 플러그인 마켓플레이스로 카테고리 단위 설치가 가능하며, 각 에이전트는 독립 컨텍스트·도메인 전문성·모델 라우팅을 갖춘다.

**Sources**: `VoltAgentawesome-claude-code-subagents A collection of 100+ specialized Claude Code subagents covering a wide range of development use cases.md`

**Last updated**: 2026-05-10

---

## 개요

VoltAgent 컬렉션은 Claude Code 서브에이전트의 표준 레퍼런스 컬렉션이다. 서브에이전트의 개념과 동작 원리는 [[subagents]] 참고. (source: VoltAgentawesome...)

## 카테고리별 에이전트 목록

### 01. Core Development (`voltagent-core-dev`) — 11개
일상적인 코딩 태스크를 위한 필수 서브에이전트.

`api-designer`, `backend-developer`, `design-bridge`, `electron-pro`, `frontend-developer`, `fullstack-developer`, `graphql-architect`, `microservices-architect`, `mobile-developer`, `ui-designer`, `websocket-engineer`

### 02. Language Specialists (`voltagent-lang`) — 29개
언어별 깊은 프레임워크 지식을 갖춘 전문가.

`typescript-pro`, `python-pro`, `golang-pro`, `rust-engineer`, `java-architect`, `react-specialist`, `nextjs-developer`, `flutter-expert`, `swift-expert`, `kotlin-specialist`, `vue-expert`, `angular-architect`, `cpp-pro`, `csharp-developer`, `django-developer`, `dotnet-core-expert`, `elixir-expert`, `fastapi-developer`, `javascript-pro`, `laravel-specialist`, `node-specialist`, `php-pro`, `rails-expert`, `spring-boot-engineer` 외 다수

### 03. Infrastructure (`voltagent-infra`) — 16개
DevOps, 클라우드, 배포 전문가.

`cloud-architect`, `kubernetes-specialist`, `terraform-engineer`, `devops-engineer`, `docker-expert`, `sre-engineer`, `azure-infra-engineer`, `deployment-engineer`, `network-engineer`, `platform-engineer`, `security-engineer`, `terragrunt-expert` 외 다수

### 04. Quality & Security (`voltagent-qa-sec`) — 16개
테스팅, 보안, 코드 품질 전문가.

`code-reviewer`, `security-auditor`, `qa-expert`, `penetration-tester`, `chaos-engineer`, `performance-engineer`, `accessibility-tester`, `architect-reviewer`, `compliance-auditor`, `debugger`, `test-automator`, `ui-ux-tester` 외 다수

### 05. Data & AI (`voltagent-data-ai`) — 13개
데이터 엔지니어링, ML, AI 전문가.

`ai-engineer`, `data-scientist`, `machine-learning-engineer`, `llm-architect`, `mlops-engineer`, `nlp-engineer`, `data-engineer`, `data-analyst`, `database-optimizer`, `postgres-pro`, `prompt-engineer`, `reinforcement-learning-engineer` 외 다수

### 06. Developer Experience (`voltagent-dev-exp`) — 14개
툴링 및 개발자 생산성 전문가.

`documentation-engineer`, `git-workflow-manager`, `refactoring-specialist`, `legacy-modernizer`, `mcp-developer`, `cli-developer`, `dx-optimizer`, `build-engineer`, `readme-generator`, `tooling-engineer` 외 다수

### 07. Specialized Domains (`voltagent-domains`) — 13개
특정 도메인 기술 전문가.

`blockchain-developer`, `game-developer`, `iot-engineer`, `fintech-engineer`, `embedded-systems`, `healthcare-admin`, `mobile-app-developer`, `payment-integration`, `quant-analyst`, `seo-specialist` 외 다수

### 08. Business & Product (`voltagent-biz`) — 12개
제품 관리 및 비즈니스 분석.

`product-manager`, `technical-writer`, `business-analyst`, `scrum-master`, `ux-researcher`, `content-marketer`, `project-manager`, `legal-advisor`, `sales-engineer`, `wordpress-master` 외 다수

### 09. Meta & Orchestration (`voltagent-meta`) — 14개
에이전트 조율 및 메타 프로그래밍.

`agent-organizer`, `multi-agent-coordinator`, `workflow-orchestrator`, `codebase-orchestrator`, `context-manager`, `task-distributor`, `agent-installer`, `error-coordinator`, `it-ops-orchestrator`, `knowledge-synthesizer` 외 다수

### 10. Research & Analysis (`voltagent-research`) — 8개
리서치, 검색, 분석 전문가.

`research-analyst`, `competitive-analyst`, `market-researcher`, `trend-analyst`, `data-researcher`, `project-idea-validator`, `search-specialist`, `scientific-literature-researcher`

(source: VoltAgentawesome...)

## 설치

```bash
# 마켓플레이스 등록 후 카테고리 단위 설치
claude plugin marketplace add VoltAgent/awesome-claude-code-subagents
claude plugin install voltagent-core-dev    # Core Development
claude plugin install voltagent-lang        # Language Specialists
claude plugin install voltagent-infra       # Infrastructure

# 수동 설치 (전역)
cp agent-file.md ~/.claude/agents/

# 수동 설치 (프로젝트)
cp agent-file.md .claude/agents/

# 인터랙티브 설치 스크립트
./install-agents.sh
```

## subagent-catalog 도구

카탈로그 내 에이전트를 Claude Code 내에서 직접 검색·설치하는 스킬.

| 명령 | 설명 |
|---|---|
| `/subagent-catalog:search <query>` | 이름·설명·카테고리로 에이전트 검색 |
| `/subagent-catalog:fetch <name>` | 에이전트 전체 정의 가져오기 |
| `/subagent-catalog:list` | 전체 카테고리 탐색 |

## Related pages

- [[subagents]]
- [[skill-md-pattern]]
- [[model-routing]]
- [[subagent-driven-development]]
- [[superpowers-framework]]
