# Developer Skills Catalog

**Summary**: 개발자 생산성을 높이는 12가지 Claude SKILL.md 파일 카탈로그 — API 설계, DB 최적화, 아키텍처, 프론트엔드, MCP 서버 구축 등 도메인별 전문가 역할을 Claude에게 부여한다. [[skill-md-pattern|SKILL.md 패턴]]의 실전 적용 사례 모음이다.

**Sources**: `🚀 12 Claude Skills Every👨🏻‍💻Developer Should Be Using Right Now.md`

**Last updated**: 2026-05-10

---

## 개요

아래 12가지 스킬은 각각 독립적으로 사용할 수 있는 공개 SKILL.md 파일이다. [[skill-md-pattern]]에서 정의한 4요소(Role·Methodology·Constraints·Output format)를 갖추고 있으며, Claude Code 또는 호환 에이전트에 로드하여 사용한다. (source: `🚀 12 Claude Skills...md`)

---

## 지식·문서 관리

### Obsidian Skills
- **링크**: [kepano/obsidian-skills](https://github.com/kepano/obsidian-skills)
- **역할**: Obsidian vault(개인 지식 그래프)를 Claude에 연결. 일반적인 모범 사례 대신 사용자 자신의 노트를 참조해 응답한다.
- **적합 대상**: 문서를 많이 작성하는 솔로 개발자, 테크 리드

### NotebookLM-py
- **링크**: [teng-lin/notebooklm-py](https://github.com/teng-lin/notebooklm-py)
- **역할**: Python으로 구현한 RAG(검색 증강 생성)를 Claude에 연결. 팀의 내부 문서·RFC·런북을 Claude가 직접 참조한다.
- **적합 대상**: 대규모 내부 문서, 온보딩 워크플로우를 가진 팀

---

## 메타 스킬

### Skill Creator
- **링크**: [anthropics/skills — skill-creator](https://github.com/anthropics/skills/blob/main/skills/skill-creator)
- **역할**: 스킬을 만드는 스킬. 반복 작업·역할·워크플로우를 설명하면 배포 가능한 SKILL.md를 생성한다.
- **워크플로우**: 사용자가 작업 설명 → Skill Creator가 SKILL.md 생성 → Claude가 매번 전문가처럼 동작
- **적합 대상**: 반복 워크플로우를 가진 팀, 개인 AI 툴킷을 구축하려는 개발자

---

## 프론트엔드·모바일·디자인

### Frontend Design
- **링크**: [anthropics/skills — frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design)
- **역할**: Anthropic 공식 스킬. 코드 생성 전에 미적 방향을 먼저 결정한다. Inter 폰트·보라색 그라데이션 같은 AI 기본값을 거부하고, 개성 있는 타이포그래피·모션·공간 구성을 강제한다.
- **적합 대상**: 사용자 대면 제품을 출시하는 모든 개발자

### Stitch Skills (Google Labs)
- **링크**: [google-labs-code/stitch-skills](https://github.com/google-labs-code/stitch-skills)
- **역할**: Figma 디자인 설명을 입력하면 디자인 토큰(간격 스케일·타이포그래피·컬러 토큰)이 정확히 매핑된 코드를 출력한다.
- **적합 대상**: 프론트엔드 개발자, 디자인 시스템 엔지니어

### iOS Simulator Skill
- **링크**: [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill)
- **역할**: iOS 시뮬레이터 상태·기기 컨텍스트·플랫폼 특성을 Claude에 인식시켜, 실제 기기에서 동작하는 코드를 제안하게 한다.
- **적합 대상**: iOS 개발자, Swift/SwiftUI 팀

---

## 백엔드·인프라

### MCP Builder
- **링크**: [anthropics/skills — mcp-builder](https://github.com/anthropics/skills/tree/main/skills/mcp-builder)
- **역할**: [[mcp|Model Context Protocol]] 서버를 처음부터 구축하는 과정을 안내한다. 도구 정의·에러 처리·인증 패턴·연결 로직까지 포함한 서버 스캐폴드를 생성한다.
- **적합 대상**: 플랫폼 엔지니어, DevOps, Claude 기반 내부 도구 개발자

### API Designer
- **링크**: [Jeffallan/claude-skills — api-designer](https://github.com/Jeffallan/claude-skills/tree/main/skills/api-designer)
- **역할**: REST 컨벤션·OpenAPI/Swagger 스펙·버전 관리·폐기 전략·인증 흐름(OAuth 2.0, API 키, JWT)을 갖춘 API를 설계한다.
- **적합 대상**: 백엔드 개발자, API-first 팀, SDK 빌더

### Database Optimizer
- **링크**: [Jeffallan/claude-skills — database-optimizer](https://github.com/Jeffallan/claude-skills/tree/main/skills/database-optimizer)
- **역할**: 쿼리 실행 계획·인덱스 사용·스키마 정규화·파티셔닝·커넥션 풀링·캐싱 레이어(Redis, Memcached) 전략을 분석한다. N+1 쿼리, 누락된 인덱스, 과부하 조인을 진단한다.
- **적합 대상**: 백엔드 개발자, SQL을 자주 작성하는 엔지니어

---

## 아키텍처

### Software Architecture
- **링크**: [davila7/claude-code-templates — software-architecture](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/development/software-architecture)
- **역할**: 코드 작성 전 아키텍처 패턴(모놀리스 vs 마이크로서비스, 이벤트 드리븐 vs 요청-응답)을 평가하고 C4 모델 스타일 다이어그램(Mermaid)·확장성 병목·단일 장애점을 도출한다.
- **적합 대상**: 테크 리드, 시니어 엔지니어, 스타트업 CTO

### Architecture Designer
- **링크**: [Jeffallan/claude-skills — architecture-designer](https://github.com/Jeffallan/claude-skills/tree/main/skills/architecture-designer)
- **역할**: 의사결정보다 산출물 중심. 시스템 컨텍스트 다이어그램·컴포넌트 아키텍처 문서·데이터 흐름 다이어그램·인프라 레이아웃·ADR(Architecture Decision Records)을 생성한다.
- **적합 대상**: 솔루션 아키텍트, 시스템 설계 검토를 준비하는 팀

### Microservices Architect
- **링크**: [Jeffallan/claude-skills — microservices-architect](https://github.com/Jeffallan/claude-skills/tree/main/skills/microservices-architect)
- **역할**: 서비스 경계 정의·통신 패턴(동기 REST/gRPC vs 비동기 메시징: Kafka, RabbitMQ)·Saga 패턴·서비스 메시(Istio, Linkerd)·배포 토폴로지를 다룬다. Conway's Law를 고려한 조직 확장성까지 분석한다.
- **적합 대상**: 시니어 엔지니어, 플랫폼 팀, 분산 시스템 아키텍트

---

## 권장 도입 순서

| 단계 | 스킬 | 이유 |
|---|---|---|
| **Week 1** | Skill Creator, Frontend Design, API Designer | 즉각적인 품질 향상 |
| **Month 1** | Software Architecture, Database Optimizer, MCP Builder | 깊이 있는 시스템 개선 |
| **지속** | Architecture Designer, Microservices Architect, Obsidian Skills, NotebookLM-py | 복잡한 시스템·지식 관리 |

## Related pages

- [[skill-md-pattern]]
- [[mcp]]
- [[superpowers-framework]]
- [[claude-code-subagents]]
