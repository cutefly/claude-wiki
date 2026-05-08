# Test-Driven Development (in Agentic Contexts)

**Summary**: 에이전트 개발에서의 TDD는 항상 실패하는 테스트를 먼저 작성한 후 최소한의 코드로 통과시키는 RED-GREEN-REFACTOR 사이클을 엄격하게 강제한다.

**Sources**: `obrasuperpowers An agentic skills framework & software development methodology that works..md`

**Last updated**: 2026-05-08

---

## 개념

[[superpowers-framework]]의 TDD 스킬은 전통적인 테스트 주도 개발을 에이전트 환경에 적용한 것이다. 에이전트는 기본적으로 테스트 없이 코드를 작성하려는 경향이 있기 때문에, 스킬이 이를 구조적으로 방지한다. (source: obrasuperpowers...)

핵심 원칙: **테스트 없이 작성된 코드는 삭제된다.**

## RED-GREEN-REFACTOR 사이클

### RED — 실패하는 테스트 작성
1. 구현하려는 기능에 대한 테스트를 먼저 작성
2. 테스트를 실행하여 **실패하는지 확인** (이 단계가 핵심)
3. 테스트가 통과하면 이미 구현되어 있거나 테스트가 잘못된 것

### GREEN — 최소한의 코드 작성
1. 테스트를 통과시키는 **최소한의** 코드만 작성
2. 완벽한 구현이 아니라 테스트 통과가 목표
3. 테스트 실행 후 **통과 확인**

### REFACTOR — 코드 정리
1. 테스트가 통과하는 상태를 유지하며 코드 개선
2. 중복 제거, 가독성 향상
3. 각 리팩토링 후 테스트 재실행

(source: obrasuperpowers...)

## 에이전트 TDD의 중요성

일반 개발자와 달리 에이전트는:
- 코드를 작성한 후 테스트를 추가하려는 강한 경향
- "작동하는 것 같으니 완료"라고 선언하는 패턴
- 테스트 실패를 무시하거나 우회하는 시도

**verification-before-completion** 스킬과 함께 사용하면 에이전트가 실제로 검증 전까지 완료를 선언하지 못하도록 한다.

## YAGNI와의 관계

TDD는 자연스럽게 YAGNI(You Aren't Gonna Need It) 원칙을 강제한다. 테스트가 요구하는 기능만 구현하면 되므로, 필요하지 않은 코드가 추가될 여지가 없다.

## 안티패턴

- 테스트 작성 전 코드 구현 → 발견 시 코드 삭제
- 테스트가 통과했다고 확인하지 않고 진행
- 실패를 확인하지 않고 GREEN 단계로 이동
- 리팩토링 중 테스트 생략

## [[subagent-driven-development]]과의 통합

SDD에서 각 서브에이전트는 자신이 담당하는 태스크에 TDD를 적용한다. 2단계 검토의 첫 번째 단계에서 테스트 커버리지와 TDD 준수 여부를 확인한다.

## Related pages

- [[superpowers-framework]]
- [[agentic-skills]]
- [[subagent-driven-development]]
- [[coding-agent-workflows]]
