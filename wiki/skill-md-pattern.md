# SKILL.md 패턴

**Summary**: SKILL.md는 Claude를 포함한 AI 코딩 에이전트에게 특정 전문가 역할·방법론·제약·출력 형식을 부여하는 재사용 가능한 마크다운 파일 형식이다. 스킬이 로드되면 에이전트는 해당 작업 유형을 만날 때마다 자동으로 전문가처럼 행동한다.

**Sources**: `obrasuperpowers An agentic skills framework & software development methodology that works..md`, `🚀 12 Claude Skills Every👨🏻‍💻Developer Should Be Using Right Now.md`

**Last updated**: 2026-05-10

---

## 개념

SKILL.md 파일은 AI 에이전트에게 "이 유형의 작업을 만나면 이렇게 행동하라"고 사전에 정의한 지침 모듈이다. 일반 프롬프트와 달리 스킬은 매번 지시하지 않아도 **자동으로 발동**되도록 설계되어 있다. (source: obrasuperpowers...)

핵심 가치는 **일관성**과 **복리 효과**다. 스킬이 쌓일수록 에이전트가 더 다양한 상황에서 전문가처럼 동작한다.

## SKILL.md의 4가지 구성 요소

각 스킬 파일은 네 가지 요소를 정의한다. (source: `🚀 12 Claude Skills...md`)

| 요소 | 역할 | 예시 |
|---|---|---|
| **Role** | 에이전트에게 부여할 전문가 정체성 | "You are a senior database optimizer" |
| **Methodology** | 단계별 사고·실행 프로세스 | RED-GREEN-REFACTOR 사이클 |
| **Constraints** | 피해야 할 것, 반드시 지켜야 할 것 | "Never write code before a test exists" |
| **Output format** | 출력 스키마·파일 구조·다이어그램 형식 | OpenAPI spec, Mermaid C4 diagram |

## 스킬의 종류

### Rigid(엄격한) 스킬
프로세스 순서를 반드시 따르는 스킬. 규율이 핵심이다.
- [[test-driven-development]] — RED-GREEN-REFACTOR를 순서대로 강제
- **systematic-debugging** — 4단계 근본 원인 분석
- **verification-before-completion** — 완료 선언 전 실제 검증

### Flexible(유연한) 스킬
원칙을 상황에 맞게 적용하는 스킬.
- **brainstorming** — 소크라테스식 대화로 설계 정제
- **writing-plans** — 프로젝트 특성에 맞는 구현 계획 수립

## 스킬 vs 서브에이전트

| | 스킬 (SKILL.md) | [[subagents\|서브에이전트]] |
|---|---|---|
| 핵심 질문 | HOW to work (방법론) | WHO does the work (전문가) |
| 트리거 | 작업 유형에 따라 자동 발동 | 도메인·태스크에 따라 호출 |
| 컨텍스트 | 주 에이전트와 공유 | 독립된 격리 컨텍스트 |
| 예시 | TDD, 브레인스토밍, 코드 검토 | python-pro, security-auditor |

두 접근법은 상호 보완적이다. Superpowers 스킬로 **워크플로우를 구조화**하고, VoltAgent 서브에이전트로 **각 단계의 전문성**을 높인다.

## 스킬이 해결하는 문제

스킬 없이 에이전트를 사용할 때 반복되는 나쁜 패턴:

- 테스트 없이 코드를 먼저 작성
- 성공 여부 확인 없이 "완료" 선언
- 계획 없이 바로 구현에 착수
- 문제 발생 시 추측에 의존한 디버깅

스킬은 이런 패턴을 구조적으로 방지한다. (source: obrasuperpowers...)

## 스킬 만드는 방법

**Skill Creator** — Anthropic 공식 메타 스킬. 반복 작업을 설명하면 배포 가능한 SKILL.md를 자동 생성한다.

```
사용자 → 반복 작업·역할 설명
    ↓
Skill Creator → SKILL.md 생성
    ↓
에이전트 → 해당 작업마다 전문가처럼 행동
```

## Related pages

- [[superpowers-framework]]
- [[subagents]]
- [[test-driven-development]]
- [[subagent-driven-development]]
- [[developer-skills-catalog]]
- [[claude-code-subagents]]
