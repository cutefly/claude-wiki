# Subagent-Driven Development

**Summary**: 서브에이전트 기반 개발(SDD)은 [[superpowers-framework]]의 핵심 실행 전략으로, 구현 계획의 각 태스크를 독립된 서브에이전트에게 위임하고 완료 후 2단계 검토(스펙 준수 → 코드 품질)를 거쳐 전진한다.

**Sources**: `obrasuperpowers An agentic skills framework & software development methodology that works..md`

**Last updated**: 2026-05-10

---

## 개념

Subagent-Driven Development(SDD)는 구현 계획이 준비된 후, 에이전트가 각 태스크에 대해 새로운 서브에이전트를 파견하고, 완료된 작업을 2단계로 검토하며 전진하는 방식이다. (source: obrasuperpowers...)

일반적인 에이전트 개발에서는 장시간 작업 중 컨텍스트가 오염되거나 계획에서 이탈하는 문제가 발생한다. SDD는 각 태스크를 격리된 서브에이전트에게 위임함으로써 이 문제를 해결한다.

## 2단계 검토 프로세스

각 태스크 완료 후:

**1단계: 스펙 준수 검토**
- 태스크가 계획된 요구사항을 충족했는가?
- 예상한 파일과 기능이 구현되었는가?
- 명세에서 벗어난 부분은 없는가?

**2단계: 코드 품질 검토**
- 코드가 clean하고 유지보수 가능한가?
- 테스트가 올바르게 작성되었는가?
- 보안 취약점이나 성능 문제는 없는가?

심각한 이슈가 발견되면 다음 태스크로 진행을 차단한다. (source: obrasuperpowers...)

## SDD vs Executing-Plans

[[superpowers-framework]]는 두 가지 실행 전략을 제공한다:

| | SDD | Executing-Plans |
|---|---|---|
| 태스크 실행 | 각 태스크에 별도 서브에이전트 | 에이전트가 직접 순차 실행 |
| 검토 방식 | 태스크마다 자동 2단계 검토 | 사람이 체크포인트에서 검토 |
| 속도 | 더 빠른 자율 실행 | 인간 감독 포함 |
| 적합한 상황 | 명세가 명확하고 독립적인 태스크들 | 검토가 필요한 복잡한 변경 |

## 병렬 서브에이전트 디스패치

**dispatching-parallel-agents** 스킬을 통해 독립적인 태스크들을 동시에 실행할 수 있다. 공유 상태나 순차적 의존성이 없는 태스크 2개 이상이 있을 때 활용한다.

## 자율 실행 능력

SDD를 통해 Claude Code가 별도 지시 없이 수 시간 동안 자율적으로 작업할 수 있다. 계획이 충분히 상세하면 에이전트가 계획에서 이탈하지 않고 독립적으로 진행한다. (source: obrasuperpowers...)

## 사전 조건

SDD가 잘 동작하려면:
1. **상세한 구현 계획** — 2-5분 단위의 명확한 태스크 (superpowers의 writing-plans 스킬로 생성)
2. **각 태스크에 정확한 파일 경로** 명시
3. **검증 단계** 포함 — 태스크 완료를 확인하는 방법
4. **[[test-driven-development|TDD 기반]]** — 테스트가 진실의 기준

## Related pages

- [[superpowers-framework]]
- [[skill-md-pattern]]
- [[test-driven-development]]
- [[subagents]]
- [[claude-code-subagents]]
