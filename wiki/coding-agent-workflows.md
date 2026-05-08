# Coding Agent Workflows

**Summary**: 코딩 에이전트 워크플로우는 AI 에이전트가 소프트웨어를 개발하는 전반적인 패턴으로, 계획 수립부터 완료까지 체계적인 단계를 따른다.

**Sources**: `obrasuperpowers An agentic skills framework & software development methodology that works..md`, `VoltAgentawesome-claude-code-subagents A collection of 100+ specialized Claude Code subagents covering a wide range of development use cases.md`

**Last updated**: 2026-05-08

---

## 개요

에이전트가 즉흥적으로 코드를 작성할 때 발생하는 문제는 일관성 없는 품질, 계획 이탈, 검증 없는 완료 선언이다. 체계적인 워크플로우는 이 문제를 구조적으로 해결한다. (source: obrasuperpowers...)

## 전체 워크플로우

```
사용자 요청
    ↓
[브레인스토밍] 요구사항 명확화, 설계 대안 탐색
    ↓
[Git Worktree] 격리된 작업 공간 생성
    ↓
[계획 수립] 2-5분 단위 태스크로 분해
    ↓
[실행] SDD 또는 일괄 실행
    ↓
[TDD] 각 태스크에서 RED-GREEN-REFACTOR
    ↓
[코드 검토] 스펙 준수 + 코드 품질
    ↓
[완료] 머지/PR/폐기 결정
```

## 두 가지 에이전트 확장 패턴

현재 에이전트 생태계는 에이전트를 확장하는 두 가지 보완적 접근법을 제공한다:

### 스킬 기반 (방법론)
**[[superpowers-framework|Superpowers]]** 방식. HOW to work에 집중.
- 자동으로 발동되는 행동 지침
- 개발 방법론 전체를 구조화
- 단일 에이전트의 작업 방식을 개선

### 에이전트 기반 (전문성)
**[[claude-code-subagents|VoltAgent]]** 방식. WHO does the work에 집중.
- 도메인 특화 전문가 에이전트
- 격리된 컨텍스트에서 병렬 실행 가능
- 특정 기술 영역의 깊은 지식 제공

두 접근법은 상호 보완적이다: Superpowers 스킬로 워크플로우를 구조화하고, VoltAgent 서브에이전트로 각 단계의 전문성을 높인다.

## 주요 원칙

**체계성 우선 (Systematic over ad-hoc)**  
추측이 아닌 프로세스를 따른다. 문제가 생기면 검증된 절차를 통해 해결한다.

**증거 기반 (Evidence over claims)**  
"작동하는 것 같다"가 아니라 실제로 테스트가 통과했음을 확인한다. [[test-driven-development|TDD]]와 **verification-before-completion**이 이를 보장한다.

**격리 (Isolation)**  
Git worktree와 서브에이전트의 독립 컨텍스트로 작업을 격리하여 교차 오염을 방지한다.

**단순성 (Simplicity)**  
YAGNI — 필요하지 않은 것은 만들지 않는다. 필요한 것보다 더 복잡하게 만들지 않는다.

## 자율 실행

체계가 갖춰진 워크플로우에서 에이전트는 수 시간 동안 자율적으로 작업할 수 있다. 명확한 계획과 [[subagent-driven-development|SDD]] 조합은 에이전트가 계획에서 이탈하지 않고 독립적으로 진행하도록 한다. (source: obrasuperpowers...)

## 모델 선택

각 단계에 적합한 모델을 사용하는 것이 중요하다. 자세한 내용은 [[model-routing]] 참고.

## Related pages

- [[superpowers-framework]]
- [[agentic-skills]]
- [[subagent-driven-development]]
- [[claude-code-subagents]]
- [[test-driven-development]]
- [[model-routing]]
