# 서브에이전트 (Subagents)

**Summary**: 서브에이전트는 특정 도메인 작업을 위해 독립된 컨텍스트 윈도우에서 동작하는 특화 AI 어시스턴트다. 주 에이전트가 작업 유형에 따라 적절한 서브에이전트를 호출하며, 각 서브에이전트는 자신의 역할에 최적화된 시스템 프롬프트·도구·모델을 가진다.

**Sources**: `VoltAgentawesome-claude-code-subagents A collection of 100+ specialized Claude Code subagents covering a wide range of development use cases.md`

**Last updated**: 2026-05-10

---

## 개념

서브에이전트는 Claude Code가 특정 유형의 작업을 만났을 때 호출하는 전문 AI 어시스턴트다. (source: VoltAgentawesome...)

[[skill-md-pattern|스킬]]이 에이전트의 **작업 방식(HOW)**을 정의하는 것과 달리, 서브에이전트는 **작업을 수행하는 주체(WHO)**를 정의한다. 각 서브에이전트는 격리된 컨텍스트에서 동작하므로 주 대화가 태스크 세부 사항으로 오염되지 않는다.

## 핵심 장점

**독립 컨텍스트 윈도우**
서브에이전트마다 격리된 컨텍스트 공간을 가진다. 작업 간 교차 오염을 방지하고 주 대화를 깔끔하게 유지한다.

**도메인 특화 지능**
각 서브에이전트는 전문 분야에 맞게 세심하게 설계된 시스템 프롬프트를 가져, 해당 도메인에서 일반 에이전트보다 더 나은 결과를 낸다.

**프로젝트 간 공유**
한 번 만들면 여러 프로젝트에서 재사용하고 팀 전체에 배포할 수 있어 일관된 개발 방식을 보장한다.

**세밀한 도구 권한**
각 서브에이전트의 도구 접근 권한을 독립적으로 설정한다. 보안 감사 에이전트는 읽기만, 코드 작성 에이전트는 실행까지 허용하는 식이다.

(source: VoltAgentawesome...)

## 파일 구조

각 서브에이전트는 표준화된 마크다운 파일로 정의된다.

```markdown
---
name: subagent-name
description: 언제 이 에이전트가 호출되어야 하는지 (자동 호출의 트리거 조건)
tools: Read, Write, Edit, Bash, Glob, Grep
model: sonnet
---

You are a [역할 설명 및 전문 분야]...

[에이전트 특화 체크리스트, 패턴, 가이드라인]

## Communication Protocol
에이전트 간 통신 사양...

## Development Workflow
구조화된 실행 단계...
```

## 저장 위치

| 유형 | 경로 | 범위 | 우선순위 |
|---|---|---|---|
| 프로젝트 서브에이전트 | `.claude/agents/` | 현재 프로젝트만 | 높음 |
| 전역 서브에이전트 | `~/.claude/agents/` | 모든 프로젝트 | 낮음 |

이름 충돌 시 프로젝트 특화 서브에이전트가 전역 서브에이전트를 오버라이드한다.

## 도구 할당 원칙

최소 필요 권한(least privilege) 원칙을 따른다. (source: VoltAgentawesome...)

| 에이전트 유형 | 할당 도구 | 이유 |
|---|---|---|
| 읽기 전용 (검토자·감사자) | `Read, Grep, Glob` | 수정 없이 분석만 |
| 리서치 에이전트 | `Read, Grep, Glob, WebFetch, WebSearch` | 정보 수집 |
| 코드 작성 에이전트 | `Read, Write, Edit, Bash, Glob, Grep` | 생성 및 실행 |
| 문서화 에이전트 | `Read, Write, Edit, Glob, Grep, WebFetch, WebSearch` | 리서치 포함 문서화 |

## 모델 라우팅

각 서브에이전트는 frontmatter의 `model` 필드로 적절한 모델로 자동 라우팅된다. 자세한 기준은 [[model-routing]] 참고.

| 모델 | 사용 시점 |
|---|---|
| `opus` | 아키텍처 검토, 보안 감사, 금융 로직 등 심층 추론 |
| `sonnet` | 일상적인 코딩, 디버깅, 리팩토링 |
| `haiku` | 문서화, 검색, 의존성 확인 등 빠른 단순 작업 |

`model: inherit` 설정 시 주 대화의 모델을 그대로 사용한다.

## 서브에이전트 만들기

Claude Code에서 `/agents` 명령으로 서브에이전트 관리자에 접근한다.

1. `/agents` 실행
2. 프로젝트 전용 또는 전역 선택
3. 역할 및 발동 트리거 설명 작성
4. 도구 접근 권한 설정
5. 시스템 프롬프트 편집 (에디터에서 `e` 입력)

또는 기존 서브에이전트를 직접 호출:

```
> Have the code-reviewer subagent analyze my latest commits
```

## Related pages

- [[skill-md-pattern]]
- [[claude-code-subagents]]
- [[model-routing]]
- [[subagent-driven-development]]
- [[superpowers-framework]]
