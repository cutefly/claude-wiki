# Model Routing

**Summary**: 모델 라우팅은 태스크의 복잡도와 특성에 따라 적절한 Claude 모델(Opus/Sonnet/Haiku)을 자동으로 선택하여 품질과 비용을 최적화하는 전략이다.

**Sources**: `VoltAgentawesome-claude-code-subagents A collection of 100+ specialized Claude Code subagents covering a wide range of development use cases.md`

**Last updated**: 2026-05-08

---

## 개념

[[claude-code-subagents|VoltAgent 서브에이전트]] 컬렉션은 각 에이전트에 `model` 필드를 포함하여 태스크 유형에 맞는 Claude 모델로 자동 라우팅한다. 모든 태스크에 가장 강력한 모델을 사용하면 불필요한 비용이 발생하고, 모든 태스크에 가장 빠른 모델을 사용하면 품질이 저하된다. (source: VoltAgentawesome...)

## 라우팅 기준

| 모델 | 사용 시점 | 예시 에이전트 |
|---|---|---|
| **Opus** | 심층 추론 — 아키텍처 검토, 보안 감사, 금융 로직 | security-auditor, architect-reviewer, fintech-engineer |
| **Sonnet** | 일상적인 코딩 — 작성, 디버깅, 리팩토링 | python-pro, backend-developer, devops-engineer |
| **Haiku** | 빠른 태스크 — 문서화, 검색, 의존성 확인 | documentation-engineer, seo-specialist, build-engineer |

(source: VoltAgentawesome...)

## 모델 특성

### Opus
- 가장 강력한 추론 능력
- 복잡한 트레이드오프 분석에 적합
- 비용이 높고 응답이 느림
- 오답의 비용이 큰 작업에 사용

### Sonnet
- 균형 잡힌 성능과 비용
- 대부분의 코딩 태스크에 적합
- 기본값으로 권장

### Haiku
- 가장 빠르고 저렴
- 단순하고 반복적인 태스크에 적합
- 창의적 판단보다 정보 검색/변환에 적합

## 설정 방법

서브에이전트 파일의 frontmatter에서 설정:

```yaml
---
name: my-agent
model: sonnet    # opus, sonnet, haiku 중 선택
---
```

`model: inherit` 설정 시 주 대화에서 사용 중인 모델을 그대로 사용한다.

개발자가 에이전트 파일의 `model` 필드를 직접 수정하여 기본값을 오버라이드할 수 있다.

## 라우팅 결정 기준

적절한 모델을 선택할 때 고려할 요소:
- **오류 비용**: 잘못된 결정이 얼마나 큰 문제를 일으키는가?
- **반복 빈도**: 자주 호출되는 에이전트일수록 비용 최적화가 중요
- **컨텍스트 양**: 대규모 코드베이스 분석은 더 강력한 모델이 필요
- **창의성 요구**: 단순 변환 vs. 설계 결정

## Related pages

- [[claude-code-subagents]]
- [[coding-agent-workflows]]
- [[superpowers-framework]]
