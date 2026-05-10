# Model Context Protocol (MCP)

**Summary**: Anthropic이 만든 오픈 표준으로, Claude를 외부 도구·API·데이터 소스에 연결하는 프로토콜. MCP 서버를 구축하면 Claude가 실제 내부 시스템을 직접 조작할 수 있다.

**Sources**: `🚀 12 Claude Skills Every👨🏻‍💻Developer Should Be Using Right Now.md`, `VoltAgentawesome-claude-code-subagents A collection of 100+ specialized Claude Code subagents covering a wide range of development use cases.md`

**Last updated**: 2026-05-10

---

## 개념

MCP는 Claude와 외부 시스템 사이의 표준화된 연결 인터페이스다. MCP 서버는 Claude가 호출할 수 있는 **도구(tool)**를 노출하며, Claude는 이 도구를 통해 데이터베이스 조회·API 호출·파일 시스템 접근 등을 수행한다. (source: `🚀 12 Claude Skills...md`)

일반적인 웹 브라우징이나 파일 읽기와 달리, MCP는 팀의 **실제 내부 시스템**에 Claude를 직접 연결한다는 점이 핵심이다.

## MCP 서버 구성 요소

- **Tool 정의** — Claude가 호출할 수 있는 함수 목록과 입출력 스키마
- **연결 로직** — 외부 시스템(DB, API 등)과의 실제 통신
- **에러 처리** — Claude가 실패를 인식하고 대응할 수 있도록 구조화된 에러 응답
- **인증 패턴** — API 키, OAuth 등 자격증명 관리

## 활용 사례

```
예: PostgreSQL 읽기 전용 MCP 서버
Claude → MCP 서버 → PostgreSQL
         (쿼리 검증, 커넥션 풀링 포함)
```

내부 시스템에 MCP를 연결하면:
- Claude가 실제 데이터를 기반으로 분석·제안
- 반복적인 데이터 조회 작업 자동화
- 팀 전용 AI 도구 내재화

## MCP 관련 도구

**[[developer-skills-catalog#MCP Builder|MCP Builder 스킬]]** — SKILL.md 형태의 스킬. 도구 정의부터 README까지 MCP 서버 스캐폴드를 자동 생성한다. (source: `🚀 12 Claude Skills...md`)

**mcp-developer 서브에이전트** — [[claude-code-subagents|VoltAgent]] Developer Experience 카테고리 소속. MCP 서버 개발 전반을 담당하는 특화 서브에이전트다. (source: VoltAgentawesome...)

## Related pages

- [[developer-skills-catalog]]
- [[subagents]]
- [[skill-md-pattern]]
- [[superpowers-framework]]
