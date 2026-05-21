# Urban Prototyping Multi-Skill System

## Goal

`urban-prototyping-coach`를 단일 동반 스킬이 아니라,
지속가능한 Urban테크 프로젝트에서 여러 스킬이 역할을 나눠 함께 작동하는 시스템으로 정의한다.

## System Role Split

| role | owner | 하는 일 | 언제 들어오는가 |
| --- | --- | --- | --- |
| student-facing coaching owner | `urban-prototyping-coach` | 아이디어를 질문, 작은 실험, 증거, 다음 결정으로 바꾼다 | 기본 진입점 |
| actor-first structure helper | `cogarch` | 행위자, 상황, 장소, ownership boundary를 정리한다 | 문제 범위가 크거나 여러 행위자가 섞일 때 |
| evidence boundary helper | `vector-language-cognition` | 관찰, proxy, 해석, claim boundary를 구분한다 | 증거가 약한데 주장이 커질 때 |
| package and validation owner | `generate-skill` | 스킬 구조, runtime compatibility, validation contract를 관리한다 | 스킬 파일이나 시스템 구조를 바꿀 때 |

## Single Visible Owner Rule

학생이나 강의 참가자에게는 항상 `urban-prototyping-coach`가
보이는 주 스킬로 동작합니다.

다른 스킬은 아래 역할만 맡습니다.

- `cogarch`: 구조 정렬
- `vector-language-cognition`: 증거 경계 정렬
- `generate-skill`: 패키징과 검증 정렬

즉, 시스템은 멀티 스킬이지만
**사용자 표면은 하나의 코칭 흐름**으로 유지합니다.

## Shared Packet

모든 스킬은 아래 패킷을 공유합니다.

```text
project_name:
urban_domain:
primary_actor:
situation:
place_or_touchpoint:
current_workaround:
friction:
learning_question:
sustainability_hypothesis:
prototype_method:
evidence_targets:
evidence_state:
claim_boundary:
next_decision:
```

## Stage Routing

### Stage 1. Problem framing

- owner: `urban-prototyping-coach`
- output: `learning_question`이 있는 1문장 문제 정의

### Stage 2. Actor and place reduction

- owner: `urban-prototyping-coach`
- helper: `cogarch`
- output: `primary_actor`, `situation`, `place_or_touchpoint`, `current_workaround`

### Stage 3. Prototype method selection

- owner: `urban-prototyping-coach`
- output: `prototype_method`, `today's smallest artifact`

### Stage 4. Evidence boundary check

- owner: `urban-prototyping-coach`
- helper: `vector-language-cognition`
- output: `evidence_targets`, `evidence_state`, `claim_boundary`

### Stage 5. System and package maintenance

- owner: `generate-skill`
- helper: `cogarch`
- output: updated `SKILL.md`, routing docs, manifest, validation evidence

## Routing Rules

- 아이디어를 바로 실험 질문으로 줄일 수 있으면 `urban-prototyping-coach`만 사용합니다.
- 행위자가 2개 이상 섞이거나 도시 전체 문제처럼 커지면 `cogarch`를 호출해 actor-first로 줄입니다.
- 클릭이나 인터뷰 반응만 있는데 도시 효과나 정책 효과를 말하려 하면 `vector-language-cognition` 규칙으로 claim boundary를 낮춥니다.
- 스킬 구조, companion docs, validation contract를 바꾸면 `generate-skill`이 owner가 됩니다.

## Closeout Contract

한 번의 반복은 항상 아래 3줄로 닫습니다.

1. 결론
2. 근거
3. 다음 행동

그리고 시스템 레벨에서는 아래 3개가 함께 남아야 합니다.

- 어떤 스킬이 owner였는가
- 어떤 helper가 개입했는가
- 어떤 evidence_state / claim_boundary로 닫았는가

## Example

`분리배출 도우미`를 예로 들면:

1. `urban-prototyping-coach`가 자취생의 분리배출 혼란을 학습 질문으로 줄입니다.
2. `cogarch`가 `자취생 / 배출 직전 / 집 앞 배출 지점`으로 상황을 줄입니다.
3. `urban-prototyping-coach`가 `Wizard of Oz` 또는 `Tiny Functional Prototype`을 고릅니다.
4. `vector-language-cognition`이 `실제 입력`, `재질문`, `다시 사용`은 관찰 신호로 두고, `도시 전체 수요`는 미검증 claim으로 남깁니다.
5. `generate-skill`은 이 흐름이 패키지 안에서 재사용 가능하게 문서와 검증 구조로 닫습니다.
