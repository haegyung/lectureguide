# Urban Prototyping Coach Domain Alignment

이 문서는 `urban-prototyping-coach`가 어떤 기준에서 현재 모습을 갖게 되었는지 짧게 정리한 메모입니다.

## 목표

`student-guide.md`의 통합 교재 기준을 유지하면서,
`generate-skill`, `vector-language-cognition`, `cogarch`의 역할을 섞지 않고
지속가능한 Urban테크 수업에 맞는 스킬로 닫는다.

## 기준 문서와 받아온 역할

| 기준 | 이 패키지에서 가져온 것 | 적용 위치 |
| --- | --- | --- |
| `student-guide.md` | NDM 기반 프로토타이핑, 질문 중심 학습, 증거 우선, 설계 전 작은 실험 | `Purpose`, `Working Position`, `Default Workflow` |
| `generate-skill` | 기준 문서 고정, 실행 도구 호환성, 고정 기준/현재 기록/이번 판단 구분, 검증 방식 | `Working Source of Truth`, `Runtime Compatibility Gate`, `3층 분류`, `Preflight and Validation` |
| `vector-language-cognition` | 관찰과 해석 분리, 증거 상태, 말할 수 있는 범위, 간접 신호 과장 방지 | `Evidence and Claim Boundary`, `Code / LLM Boundary` |
| `cogarch` | 행위자를 먼저 좁히기, 책임 범위 정리, 구조 우선 정리 | `Urban-Tech Domain Focus`, `Conflict Resolution` |

## Urban테크에 맞게 좁히는 질문

이 스킬은 도시 문제를 크게 말하지 않고 아래 질문으로 줄입니다.

1. 누구의 문제인가
2. 어떤 상황인가
3. 어디서 벌어지는가
4. 지금 어떤 우회 방식이 있는가
5. 오늘 무엇을 먼저 배울 것인가
6. 어떤 증거가 나오면 다음 설계로 넘어갈 수 있는가

## 증거와 주장 범위

- 관찰 가능한 행동은 강한 증거다.
- 말로 표현된 필요는 중요하지만 행동과 분리한다.
- 클릭, 신청, 재사용 같은 간접 신호는 별도 상태(`proxy_signal`)로 둔다.
- 도시 전체 수요, 정책 효과, 환경 효과는 수업 실험만으로 닫지 않는다.

## 문서별 역할

- `student-guide.md`: 수업 개념과 학생 설명의 기준
- `SKILL.md`: 실행 규칙과 판단 형식
- `MANIFEST.md`: 배포/검증 기록
- `pretotyping-guide.md`: 역사적 참고 문서
