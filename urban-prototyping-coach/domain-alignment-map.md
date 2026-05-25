# Urban Prototyping Coach Domain Alignment

이 문서는 `urban-prototyping-coach`가 어떤 기준에서 현재 모습을 갖게 되었는지 짧게 정리한 메모입니다.

## Goal

`student-guide.md`의 통합 교재 기준을 유지하면서,
`generate-skill`, `vector-language-cognition`, `cogarch`의 역할을 섞지 않고
지속가능한 Urban테크 도메인 특화 스킬로 닫는다.

## Source Map

| source | 이 패키지에서 가져온 것 | 적용 위치 |
| --- | --- | --- |
| `student-guide.md` | NDM 기반 프로토타이핑, 질문 중심 학습, 증거 우선, 설계 전 작은 실험 | `Purpose`, `Working Position`, `Default Workflow`, `commands/urban/` prompt wording |
| `generate-skill` | 기준 문서 위치, 호환성, 고정/유동/판단 구분, 검증 계약 | `Working Source of Truth`, `Runtime Compatibility Gate`, `3층 분류`, `Preflight and Validation` |
| `vector-language-cognition` | 관찰과 해석 분리, evidence state, claim boundary, proxy 과장 방지 | `Evidence and Claim Boundary`, `Code / LLM Boundary` |
| `cogarch` | actor-first 정렬, ownership boundary, 구조 우선 정리 | `Urban-Tech Domain Focus`, `Conflict Resolution`, `skills/urban-scope` |

## Domain Adapter

이 스킬의 domain adapter는 아래 질문으로 닫힙니다.

1. 누구의 문제인가
2. 어떤 상황인가
3. 어디서 벌어지는가
4. 지금 어떤 우회 방식이 있는가
5. 오늘 무엇을 먼저 배울 것인가
6. 어떤 증거가 나오면 다음 설계로 넘어갈 수 있는가

## Evidence Boundary

- 관찰 가능한 행동은 강한 증거다.
- 말로 표현된 필요는 중요하지만 행동과 분리한다.
- 클릭, 신청, 재사용 같은 간접 신호는 `proxy_signal`로 둔다.
- 도시 전체 수요, 정책 효과, 환경 효과는 수업 실험만으로 닫지 않는다.

## Ownership Boundary

- `student-guide.md`: 수업 개념과 학생 설명의 기준
- `SKILL.md`: 실행 규칙과 판단 형식
- `references/routing-contract.md`: command 이름과 child skill 연결의 기준
- `commands/urban/`: portable command prompt surface
- `skills/urban-*`: 단계별 child skill surface
- `MANIFEST.md`: 배포/검증 기록
- `pretotyping-guide.md`: 역사적 참고 문서
