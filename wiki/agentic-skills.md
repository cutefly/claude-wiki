# Agentic Skills

**Summary**: 에이전트 스킬은 코딩 에이전트의 행동 방식을 구조화하는 재사용 가능한 지시 모듈로, 특정 상황에서 자동으로 발동된다.

**Sources**: `obrasuperpowers An agentic skills framework & software development methodology that works..md`

**Last updated**: 2026-05-08

---

## 개념

에이전트 스킬은 에이전트가 특정 유형의 작업을 만났을 때 따라야 할 구조화된 지침이다. 일반 프롬프트와 달리, 스킬은 **자동으로 발동**되도록 설계되어 있어 개발자가 매번 지시하지 않아도 된다. (source: obrasuperpowers...)

스킬의 핵심 가치는 **일관성**이다. 동일한 유형의 작업이 매번 같은 방식으로 처리되고, 검증된 절차가 반복적으로 적용된다.

## 스킬의 종류

### Rigid(엄격한) 스킬
정확히 따라야 하는 스킬. 프로세스의 규율이 핵심이다.
- [[test-driven-development]] — RED-GREEN-REFACTOR를 반드시 순서대로 수행
- **systematic-debugging** — 4단계 근본 원인 분석

### Flexible(유연한) 스킬
원칙을 상황에 맞게 적용하는 스킬.
- **brainstorming** — 대화 흐름에 따라 유연하게 설계 정제
- **writing-plans** — 프로젝트 특성에 맞는 계획 수립

## Superpowers 스킬 우선순위

여러 스킬이 동시에 적용될 수 있을 때 순서가 중요하다:

1. **프로세스 스킬 먼저** — brainstorming, debugging 등 접근 방식을 결정하는 스킬
2. **구현 스킬 다음** — 실제 실행을 안내하는 스킬

예: "X를 만들자" → brainstorming 먼저, 그 다음 구현 스킬

## 스킬이 해결하는 문제

에이전트가 즉흥적으로 동작할 때 발생하는 문제들:
- 코드를 테스트 전에 작성하는 패턴
- 성공 여부 확인 없이 "완료"라고 선언
- 계획 없이 바로 구현에 뛰어들기
- 문제가 발생했을 때 추측에 의존한 디버깅

스킬은 이런 나쁜 패턴을 구조적으로 방지한다. (source: obrasuperpowers...)

## 스킬과 서브에이전트의 차이

| | 스킬 | [[claude-code-subagents|서브에이전트]] |
|---|---|---|
| 목적 | HOW to work (방법론) | WHO does the work (전문가) |
| 트리거 | 작업 유형에 따라 자동 발동 | 도메인/태스크 특성에 따라 호출 |
| 컨텍스트 | 주 에이전트 컨텍스트 공유 | 격리된 컨텍스트 윈도우 |
| 예시 | TDD, 브레인스토밍, 코드 검토 | python-pro, security-auditor |

## Related pages

- [[superpowers-framework]]
- [[test-driven-development]]
- [[subagent-driven-development]]
- [[claude-code-subagents]]
- [[coding-agent-workflows]]
